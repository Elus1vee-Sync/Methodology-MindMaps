<h1 align="center">User Account Control (UAC) Cheat Sheet</h1>

<p align="center">
  Comprehensive reference guide for Windows User Account Control, elevation prompts, integrity levels, privileges, and security configuration.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/-WINDOWS-111827?style=for-the-badge&logo=windows&logoColor=0078D6" alt="Windows">
  <img src="https://img.shields.io/badge/-UAC-111827?style=for-the-badge&logo=microsoft&logoColor=00A4EF" alt="User Account Control">
  <img src="https://img.shields.io/badge/-SECURITY-111827?style=for-the-badge&logo=owasp&logoColor=00A4EF" alt="Security">
  <img src="https://img.shields.io/badge/-PRIVILEGES-111827?style=for-the-badge&logoColor=FF003C" alt="Privileges">
</p>

```
 whoami /user
```

```
 whoami /priv
```

```
net localgroup administrators
```

- Confirmacion del UAC habilitado.

```
REG QUERY HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Policies\System\ /v EnableLUA
```

- Nivel de UAC del 1 al 5

```
REG QUERY HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Policies\System\ /v ConsentPromptBehaviorAdmin
```

```
environment]::OSVersion.Version
```

```
cmd /c echo %PATH%
```

