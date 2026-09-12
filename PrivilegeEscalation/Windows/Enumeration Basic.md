<h1 align="center">Windows Post-Exploitation Enumeration Cheat Sheet</h1>

<p align="center">
  Comprehensive reference guide for Windows host enumeration, users, privileges,
  services, processes, networking, scheduled tasks, and domain environment discovery.
</p>

<p align="center">
  <img src="https://cdn.simpleicons.org/windows/0078D6" width="28" alt="Windows">
  &nbsp;&nbsp;
  <img src="https://cdn.simpleicons.org/powershell/5391FE" width="28" alt="PowerShell">
  &nbsp;&nbsp;
  <img src="https://cdn.simpleicons.org/microsoft/00A4EF" width="28" alt="Microsoft">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/WINDOWS-111827?style=for-the-badge" alt="Windows">
  <img src="https://img.shields.io/badge/POWERSHELL-111827?style=for-the-badge" alt="PowerShell">
  <img src="https://img.shields.io/badge/ACTIVE%20DIRECTORY-111827?style=for-the-badge" alt="Active Directory">
  <img src="https://img.shields.io/badge/POST--EXPLOITATION-111827?style=for-the-badge" alt="Post-Exploitation">
  <img src="https://img.shields.io/badge/ENUMERATION-111827?style=for-the-badge" alt="Enumeration">
</p>

<hr>

<h2>📋 Table of Contents</h2>

<ul>
  <li><a href="#system-information">System Information</a></li>
  <li><a href="#users--groups">Users & Groups</a></li>
  <li><a href="#privileges">Privileges</a></li>
  <li><a href="#processes">Processes</a></li>
  <li><a href="#services">Services</a></li>
  <li><a href="#scheduled-tasks">Scheduled Tasks</a></li>
  <li><a href="#network-enumeration">Network Enumeration</a></li>
  <li><a href="#files--permissions">Files & Permissions</a></li>
  <li><a href="#environment">Environment</a></li>
  <li><a href="#active-directory">Active Directory</a></li>
  <li><a href="#security-products">Security Products</a></li>
  <li><a href="#automated-enumeration">Automated Enumeration</a></li>
</ul>

<hr>

<h2 id="system-information">🖥️ System Information</h2>

```cmd
hostname
systeminfo
ver
wmic os get Caption,Version,BuildNumber,OSArchitecture

