# EXPLOTACIÓN Y ESCALADA

## CVE-2019-9053
SQL Injection basada en tiempo en CMS Made Simple anterior a 2.2.10.

## Exploit-DB
Identificador: 46635.

Se examinó el código antes de utilizarlo. La copia se convirtió de Python 2 a Python 3 mediante Fissix.

## Información recuperada
Usuario mitch, correo admin@admin.com, salt 1dac0d92e9fa6bb2 y hash 0c01f4468bd75d7a84c7eb73846e8d96.

## Hashcat
Modo 20: md5($salt.$pass).
Resultado: contraseña secret.

## Acceso SSH
Usuario mitch en el puerto 2222.

## Escalada
sudo -l reveló:
(root) NOPASSWD: /usr/bin/vim

Vim permitió iniciar Bash con los privilegios del proceso administrador.

## Verificación
whoami: root
id: uid=0(root) gid=0(root)

## Banderas
USER: G00d j0b, keep up!
ROOT: W3ll d0n3. You made it!
