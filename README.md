# DNS-profe

Configuració servidor BIND9 per classe

Aquest repositori conté la configuració d'un servidor DNS utilitzant BIND9 definint dos dominis per treballar reenviadors condicionals i zones secundàries.

Dominis configurats:
- waytoit.test
- northwind.lan

En tots dos casos, es permet la transferència a la xarxa de classe.

## Procediment

- Disposar d'un VM Linux amb el servei `bind9` instal·lat, si cal instal·lar-lo `sudo apt update && sudo apt install bind9 -y`

- Clonar repositori en local a la màquina virtual.

  ```bash
  git clone https://github.com/carlesalonso/DNS-profe.git
  ```

- Copiar els arxius i la carpeta `zones`a la ruta /etc/bind

  ```bash
  cp DNS-profe/named.conf.* /etc/bind
  cp -r DNS-profe/zones /etc/bind
  ```
  - Editar els arxius per configuar-los per l'escenari (xarxa i IP de la VM) i reiniciar el servei
