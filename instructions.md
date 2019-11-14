# PowerShell and Azure Functions Workshop 

Author : Olivier Miossec 
[FRPSUG](https://frpsug.com/) / [Paris PowerShell & WinOps](https://www.meetup.com/fr-FR/PowerShell-Paris/)

Befor starting be sure to check requirements 


## Step 1, Create the function App

First we need to create a Resource Group

```powershell
New-AzResourceGroup -Name AzFunctionLab -Location NorthEurope -Tag @{"env"="Lab"}
``` 

Generate an unique name for the Azure Function App

```powershell
$FunctionAppName = -join (Get-Random -InputObject ("abcdefghijkmnopqrstuvwxyz0123456789".ToCharArray()) -Count 25)
```

Deploy the function App

```powershell 
New-AzResourceGroupDeployment -ResourceGroupName AzFunctionLab -TemplateFile .\1-install-function\function.json -functionAppName $FunctionAppName
```


## Step 2, Download the App localy



## Step 3, Create a module

## Step 4, Create an HTTP function

## Step 5, Upload the function

## Step 6, Create a Queue function

## Step 7, Update the Http function

