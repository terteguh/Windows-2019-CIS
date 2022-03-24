PS C:\Users\Administrator> Enable-WSManCredSSP -Role Server -Force


cfg               : http://schemas.microsoft.com/wbem/wsman/1/config/service/auth
lang              : en-US
Basic             : true
Kerberos          : true
Negotiate         : true
Certificate       : false
CredSSP           : true
CbtHardeningLevel : Relaxed



PS C:\Users\Administrator>

```ini
---
# ansible_user: Username
# ansible_password: Password
ansible_connection: winrm
ansible_winrm_transport: credssp
ansible_winrm_server_cert_validation: ignore
```


PS C:\Users\Administrator> SecEdit.exe /export /cfg C:\temp\output.ini

The task has completed successfully.
See log %windir%\security\logs\scesrv.log for detail info.
