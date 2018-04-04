# Disable Windows server services
GPO definition for disabling per-user and unneeded services in Windows Server 2012 R2 and up

Use this definition to be able to stop Windows from creating per-user services (like SyncHost_xxxxxx) or trying to start the maps broker service.

**Detailed description coming soon...**

## Howto
1. Copy the **.admx** and **eu-US/*.adml** to the policy store of your Windows domain controller (*central store* under `%windir%\sysvol\...` or server store under `%windir%\PolicyDefinitions`).
2. Import the ***.mof** file as WMI filter in your group policy management tool
3. Create a new GPO and use the settings under `Computer Configuration/Policies/Administrative Templates/Disable Services` to disable the desired services
4. Apply the WMI Filter `Windows Server 2012 R2 and up` to apply the settings only to appropriate systems
