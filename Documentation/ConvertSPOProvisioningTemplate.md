#Convert-SPOProvisioningTemplate
Converts a provisioning template to a web
##Syntax
```powershell
Convert-SPOProvisioningTemplate [-Out <String>] [-Encoding <Encoding>] [-Force [<SwitchParameter>]] -Path <String> [-ToSchema <XMLPnPSchemaVersion>]
```


##Parameters
Parameter|Type|Required|Description
---------|----|--------|-----------
|Encoding|Encoding|False||
|Force|SwitchParameter|False|Overwrites the output file if it exists|
|Out|String|False|Filename to write to, optionally including full path|
|Path|String|True|Path to the xml file containing the provisioning template|
|ToSchema|XMLPnPSchemaVersion|False|The schema of the output to use, defaults to the latest schema|
##Examples

###Example 1
```powershell
PS:> Convert-SPOProvisioningTemplate -Path template.xml
```
Converts a provisioning template to the latest schema and outputs the result to current console.

###Example 2
```powershell
PS:> Convert-SPOPRovisioningTemplate -Path template.xml -Out newtemplate.xml
```
Converts a provisioning template to the latest schema and outputs the result the newtemplate.xml file.

###Example 3
```powershell
PS:> Convert-SPOPRovisioningTemplate -Path template.xml -Out newtemplate.xml -ToSchema V201512
```
Converts a provisioning template to the latest schema using the 201512 schema and outputs the result the newtemplate.xml file.
