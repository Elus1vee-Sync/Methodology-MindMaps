<h1 align="center">Vulnerable Services Cheat Sheet</h1>

<p align="center">
  Comprehensive reference guide for Windows service enumeration, misconfigurations, weak permissions, insecure service configurations, and security assessment.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/-WINDOWS-111827?style=for-the-badge&logo=windows&logoColor=0078D6" alt="Windows">
  <img src="https://img.shields.io/badge/-SERVICES-111827?style=for-the-badge&logoColor=00A4EF" alt="Services">
  <img src="https://img.shields.io/badge/-PRIVILEGES-111827?style=for-the-badge&logoColor=FF003C" alt="Privileges">
  <img src="https://img.shields.io/badge/-ENUMERATION-111827?style=for-the-badge&logo=owasp&logoColor=00A4EF" alt="Enumeration">
  <img src="https://img.shields.io/badge/-SECURITY-111827?style=for-the-badge&logo=owasp&logoColor=00FFFF" alt="Security">
</p>


```
wmic product get name
```

```
get-process -Id 3324
```


```
netstat -ano | findstr 6064
```



```
get-service | ? {$_.DisplayName -like 'Druva*'}
```


