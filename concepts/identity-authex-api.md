# Authentication flows policy

The self service sign up experience in regular AAD tenants (colloquially known as ExtId/ExId/BYOI) enables the users to initiate a self service sign up flow. The tenant admin or the workflow admin can approve or deny user's request to sign up in their tenant. This can be compared with the current experience in a regular AAD tenant, where a user has to be invited or created manually by the tenant admin. 

Currently this api is to enable/disable the self service sign up experience at a tenant level. We are designing the api so that it can be used for other similar settings for all authentication flows.

The policy/api is named 'authentication flows' because the settings here will refer to the flow of user when they use identity. For example sign up is a flow, sign in is a flow, profile update, progressive profiling etc are the various authentication flows a user can go through. We'll pull in more and more settings on a case by case basis. 


## Scenarios and personas

1. Enable/Disable the self service sign up experience
1. Future use: enable/disable progressive profiling in the tenant 


## Details and schema changes

### New entity types

#### AuthenticationFlowPolicy

AuthenticationFlowPolicy allows tenant admins to manage features related to Authentication experience at tenant level. Tenant admins can enable/disable the self service sign up settings.

An entity type for authentication flow policies that contains settings for each authentication flow. Each tenant has exactly one authenticationFlowPolicy that is created at the time of tenant creation, so the policy may only be read and changed, but not created or deleted.

The entity inherits from base entity graph.policyBase.

##### Properties

|Property|Type|Description|Key|Required|ReadOnly|
|-|-|-|-|-|-|
|`id`|`Edm.string`| Inherited property. The ID of the authentication flows policy|Yes|No|Yes|
|`displayName`|`Edm.string`| Inherited property.The human-readable name of the policy, "Authentication flows policy"|No|No|Yes|
|`description`|`Edm.string`|Inherited property. A description of the policy|No|No|Yes|
|`selfServiceSignUp`|`microsoft.graph.selfServiceSignUpAuthenticationFlowConfiguration`|Self service sign up configuration |No|No|No|


##### Supported functionality

|Operation|Supported|Method        |Success   |Notes               |
|---------|:-------:|--------------|--------|--------------------|
|List     |X        |`GET`         |`200`   | Singleton, so a list is not supported. |
|Get      |✓        |`GET`         |`200`   | Allows to read the policy |
|Create   |X        |`POST`        |        |                    |
|Update   |✓        |`PATCH`       | `204`  | Update the policy  |
|Delete   |X        |`DELETE`      |        |                    |

##### CSDL

```xml
<EntityType Name="authenticationFlowPolicy" baseType="microsoft.graph.policyBase">
      <Property Name="selfServiceSignUp" Type="microsoft.graph.selfServiceSignUpAuthenticationFlowConfiguration"/>
</EntityType>
```

### New complex types

#### selfServiceSignUpAuthenticationFlowConfiguration

Represents the configurations related to self service signup.

##### Properties

|Property|Type|Description|Key|Required|ReadOnly|
|-|-|-|-|-|-|
|`isEnabled`|`Edm.boolean`|Is self service sign up flow enabled or disabled. The default value is false. |No|Yes|No|

##### Supported functionality

|Operation|Supported|Method        |Success   |Notes               |
|---------|:-------:|--------------|----------|--------------------|
|Get      |✓        |`GET`         |`200`     |                    |
|Update   |✓         |`PATCH`       |`204`     |                   |

##### CSDL

```xml
<ComplexType Name="selfServiceSignUpAuthenticationFlowConfiguration" baseType="microsoft.graph.entity">
  <Property Name="isEnabled" Type="Edm.boolean" />  
</ComplexType>
```
## Error conditions and messages

|Scenario|Method|Code|Message|
|-|-|-|-|
|The tenant is an AAD B2C tenant. These apis are not available for B2C tenants. |All|400|The tenant is an AAD B2C tenant. These apis are not available for B2C tenants.|
|User or application doesn't have appropriate permision scope and/or role|All|401|Your account does not have access to this policy. Please contact your global administrator to request access.|

## Permissions scopes

### API re-uses existing Graph permissions

|Permissions|Type|Entities/APIs Covered|
|-|-|-|
|`Policy.Read.All`|Delegated|Read authentication flow apis - GET calls|
|`Policy.Read.All`|Application-only|Read authentication flow apis - GET calls|

### New permission scopes

|ScopeName|DisplayName|Description|Type|Admin Consent?|Entities/APIs covered|
|-|-|-|-|-|-|
|`Policy.ReadWrite.AuthenticationFlows`|Read and write authentication flow policies|This permissions can read and write authentication flow policies that determine which authentication flows are enabled in the tenant and other authentication-flow-related tasks.|Delegated|Yes|All|
|`Policy.ReadWrite.AuthenticationFlows`|Read and write authentication flow policies|This permissions can read and write authentication flow policies that determine which authentication flows are enabled in the tenant and other authentication-flow-related tasks.|Application-only|Yes|All|

### RBAC
Only tenant admins will be able to read/modify these settings. 

## Example REST operations

### Use case:  Get policy

```HTTP
GET https://graph.microsoft.com/v1.0/policies/authenticationFlowPolicy

HTTP/1.1 200 OK
{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#authenticationFlowPolicy",
    "id": "authenticationFlowPolicy",
    "displayName": "Authentication flows Policy",
    "description": null,
    "selfServiceSignUp" : 
        {
            "isEnabled": "true"
        }    
}
```

### Use case: Enable self service sign up

```HTTP
PATCH https://graph.microsoft.com/v1.0/policies/authenticationFlowPolicy
{
    "selfServiceSignUp" : 
        {
            "isEnabled": "false"
        }
}

HTTP/1.1 204 NO CONTENT

GET now returns
HTTP/1.1 200 OK
{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#authenticationFlowPolicy",
    "id": "authenticationFlowPolicy",
    "displayName": "Authentication flows Policy",
    "description": null,
    "selfServiceSignUp" : 
        {
            "isEnabled": "false"
        }    
}
```


## CLI and PowerShell

### General information

We'll add below new cmdlets to Get and Set the policies described above:

```Powershell
Get-AzureADMSAuthenticationFlowPolicy

Set-AzureADMSAuthenticationFlow
    -enableSelfServiceSignUp boolean
    
### Detailed information

These cmdlets will call MS Graph Beta when the API hits prod beta, then v1.0 when the API goes to GA.


