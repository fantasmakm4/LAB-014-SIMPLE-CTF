# RECONOCIMIENTO

## Objetivo
10.67.146.11

## Escaneo de servicios
Nmap -sV -Pn identificó:
- 21/tcp FTP vsftpd 3.0.3
- 80/tcp HTTP Apache 2.4.18
- 2222/tcp SSH OpenSSH 7.2p2

## FTP
Nmap confirmó autenticación anónima (código 230). El listado de archivos presentó timeout.

## Enumeración web
Gobuster encontró /simple/, /robots.txt e /index.html.

## CMS
CMS Made Simple 2.2.8, identificado en el HTML mediante su versión publicada en el pie de página.

## Conclusión
La aplicación CMS fue seleccionada para investigación de vulnerabilidades.
