Here I will be saving usefull PowerShell commands

To create a file:
New-Item

To find a file somewhere(if we know just a name or type of extencions):
Get-ChildItem -Path "C:\" -Filter "*.md" -Recourse
Operator -Recourse, saing to look in subfolders as well

To cut file from to:
Move-Item -Path "C:\" -Destination "C:\TargetFolder\"


