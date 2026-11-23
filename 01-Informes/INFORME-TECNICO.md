# INFORME TÉCNICO — LAB-014 SIMPLE CTF

## Resumen ejecutivo
Se consiguió acceso inicial al usuario mitch mediante una vulnerabilidad SQL Injection en CMS Made Simple 2.2.8. Posteriormente se recuperó su contraseña mediante Hashcat y se obtuvo acceso remoto por SSH. La escalada a ROOT fue posible por permisos sudo inseguros sobre Vim.

## Metodología
1. Reconocimiento de puertos.
2. Enumeración de servicios.
3. Enumeración web.
4. Identificación del CMS y versión.
5. Investigación de CVE-2019-9053.
6. Extracción de información mediante SQL Injection.
7. Recuperación local del hash.
8. Acceso SSH.
9. Enumeración de sudo.
10. Escalada y verificación ROOT.

## Evidencias principales
- Nmap: puertos 21, 80 y 2222.
- Gobuster: directorio /simple/.
- CMS: versión 2.2.8.
- Hashcat: hash recuperado.
- SSH: sesión mitch.
- sudo -l: Vim permitido como ROOT sin contraseña.
- id: UID 0 confirmado.

## Resultado
Dos banderas recuperadas. Laboratorio completado.
