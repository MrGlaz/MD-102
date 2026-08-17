
|Operator|Description|Example|
|---|---|---|
|-eq|Equals|user.department -eq "IT"|
|-ne|Not equals|user.department -ne null|
|-startsWith|Starts with|user.userPrincipalName -startsWith "admin"|
|-notStartsWith|Doesn't start with|user.mailNickname -notStartsWith "test"|
|-endsWith|Ends with|user.mail -endsWith "@contoso.com"|
|-notEndsWith|Doesn't end with|user.mail -notEndsWith "@vendor.com"|
|-contains|Contains|user.jobTitle -contains "Manager"|
|-notContains|Doesn't contain|user.department -notContains "Temp"|
|-in|Matches any value in list|user.department -in ["Sales","Marketing","Support"]|
|-notIn|Doesn't match any value in list|user.usageLocation -notIn ["CA","MX"]|
