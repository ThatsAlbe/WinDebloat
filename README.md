# WinDebloat
Personal debloat customization of Chris Titus Tech's Debloat tool

Run with Powershell (or Windows Terminal) with Administrator privileges with the following commands:

```
$user = 'user'
$pass = 'pass'

$pair = "$($user):$($pass)"

$encodedCreds = [System.Convert]::ToBase64String([System.Text.Encoding]::ASCII.GetBytes($pair))

$basicAuthValue = "Basic $encodedCreds"

$Headers = @{
    Authorization = $basicAuthValue
}

#Invoke-WebRequest -Uri 'https://whatever' -Headers $Headers

irm -Uri 'https://raw.githubusercontent.com/ThatsAlbe/WinDebloat/main/winutil.ps1?token=GHSAT0AAAAAAB2RQECCU3DVBB75CKP5DO3CY25RELA' -Headers $Headers | iex
```


