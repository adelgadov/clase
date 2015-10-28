SSH
=====
 
Comandos
----------

 * apt-get install open_ssh-server: Instalación servidor ssh
 * Who(W): Para saber quienes están en nuestro servidor ssh.
 * ll /etc/ssh/: Para saber el algoritmo que tenemos en el pc (DSA/RSA).
 * ssh-keygen -l -f ssh_host_key: Es para saber la huella de nuestra clave pública, tienes que estar en /etc/ssh para ejecutarlo.
 
 ```bash
     root@teide-System-Product-Name:/home/teide# cd /etc/ssh
     root@teide-System-Product-Name:/etc/ssh# ssh-keygen -l -f ssh_host_rsa_key
     2048 17:9f:a0:d3:f5:3f:ab:91:f6:a4:2d:e4:07:7d:9a:c6  root@teide-System-Product-Name (RSA)
 ```
 
 * ssh-keygen -t rsa: Sirve para generar nuestras claves.

 ```bash
     root@teide-System-Product-Name:~/.ssh# ssh-keygen -t rsa
     Generating public/private rsa key pair.
     Enter file in which to save the key (/root/.ssh/id_rsa): /etc/ssh/ClaveGabrielRsaOct2015
     Enter passphrase (empty for no passphrase):
     Enter same passphrase again:
     Your identification has been saved in /etc/ssh/ClaveGabrielRsaOct2015.
     Your public key has been saved in /etc/ssh/ClaveGabrielRsaOct2015.pub.
     The key fingerprint is:
     5c:92:f4:9a:a3:bb:cf:42:cd:14:ac:b4:d8:fb:69:24 root@teide-System-Product-Name
     The key's randomart image is:
     +--[ RSA 2048]----+
     |       ..         |
     |      ..oo        |
     |     + oo.o       |
     |    . +..=        |
     |       =S         |
     |      E.+.        |
     |     ..+ .        |
     |      .o+         |
     |      o=o         |
     +-----------------+
 ```
 
###Habilitar conexiones 

Para que el cliente con putty pueda conectarse, primero nuestro servidor tiene que reconocer que esta contraseña es la nueva contraseña, por lo tanto debemos decírselo en el archivo de configuración.

* gedit /etc/ssh/sshd_config: Hacemos las siguientes modificaciones:
    - Añadimos: HostKey /etc/ssh/ClaveGabrielRsaOct2015
    - Borramos:
     - \#HostKey /etc/ssh/ssh_host_dsa_key
     - \#HostKey /etc/ssh/ssh_host_ecdsa_key
     - \#HostKey /etc/ssh/ssh_host_ed25519_key


 * /etc/init.d/ssh restart: Reiniciamos el servicio para que aceptes los cambios producidos en el archivo de configuración.

###Para desconectar usuarios
 
* Usamos el comando who para ver que usuarios están conectados. Vemos que el usuario diego está conectado con la terminal 16.
 
 ```bash
    root@teide-System-Product-Name:/home/teide# w
     16:43:26 up  1:31,  4 users,  load average: 0,01, 0,04, 0,05
    USUARIO             TTY              DE               LOGIN@       IDLE     JCPU    PCPU WHAT
    teide    :0        :0               15:14              ?xdm?      3:19      0.16s   init --user
    teide    pts/0     :0               16:42              6.00s      0.07s     0.53s   gnome-terminal
    teide    pts/16    diego.teide.iv   16:40              46.00s     0.06s     0.06s   -bash
    teide    pts/24    profesor.teide.i 16:21              14.00s     0.06s     0.06s   -bash
    ```
    
* Buscamos en los procesos para echarle, para ello filtramos por ssh. Matamos el proceso 5017 ya que es la terminal que está usando Diego.
    
    ```bash
    root@teide-System-Product-Name:/etc/ssh# ps aux | grep ssh
    teide     1863  0.0  0.0  10616   316 ?        Ss   15:14   0:00 ssh-agent -s
    root      4660  0.0  0.1 105648  4044 ?        Ss   16:21   0:00 sshd: teide [priv]  
    teide     4718  0.0  0.0 105648  1940 ?        S    16:21   0:00 sshd: teide@pts/24  
    root      4976  0.0  0.0  61364  2884 ?        Ss   16:35   0:00 /usr/sbin/sshd -D
    root      4978  0.0  0.1 105648  4040 ?        Ss   16:35   0:00 sshd: teide [priv]  
    teide     5017  0.0  0.0 105648  1936 ?        S    16:36   0:00 sshd: teide@pts/16
    root      5118  0.0  0.0  15964  920 pts/0     S+   16:39   0:00 grep --color=auto ssh
    root@teide-System-Product-Name:/etc/ssh# kill 5017
 ```
 
Ubicaciones
--------------
 
  * Clave pública: /etc/ssh/SSH_HOST_DSA_KEY.PUB
  * Clave privada: /etc/ssh/SSH_HOST_DSA_KEY
  
Cliente
---------

* Para conectarte a un servidor tienes que logearte con una cuenta existente en él. Podemos conectarnos de dos formas:
 * ssh -l usuario IP
 * ssh usuario@ip
* Si el servidor ha cambiado la clave pública, el cliente tiene que borrar su caché de claves para poder conectarse.
 
 * rm /root/.ssh/known_hosts: Borra todas las claves de todos los servidores que hemos almacenado
 * ssh-keygen -R “ip del host": Borra la clave de un servidor en concreto.

