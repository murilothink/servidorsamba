# Configurações do Servidor Samba


Criar um diretorio na pasta /home/ chamado "arquivos" 
  Comando para criar: mkdir arquivos
  
Permissão da pasta.
root@usuario: chmod -R 777 /home/caminho/da_pasta ou chmod -R 770 /home/caminho/da_pasta
 
Obs: 777 vai ser para diretorios publicos na rede. Ou seja todos irão ter permissão, mas isso deve ser definido no arquivo Global /etc/samba/smb.conf conforme esta no artigo github. Faça um clone dos diretorios.

### Criando Usuario no sistema
root@usuario: sudo adduser -a teste

### Criando uma senha do mesmo usuario no Samba. 

Iremos colocar a senha quando fomos acessar a pasta na rede.

root@usuario: smbpasswd -a teste

### Veja se o usuario foi criado.

root@usuario: pdbedit -L -v | grep username

Ou para vizualizar melhor:  

root@usuario: pdbedit -L -v  


### Arquivo do pdbedit -L -v 


Unix username:        caio

NT username:

Account Flags:        [U          ]

User SID:             S-1-5-21-1238916857-924684260-3818580937-1011

Primary Group SID:    S-1-5-21-1238916857-924684260-3818580937-513 

Full Name:

Home Directory:       \\fsmerenda\caio

HomeDir Drive:

Logon Script:

Profile Path:         \\fsmerenda\caio\profile

Domain:               FSMERENDA

Account desc:

Workstations:

Munged dial:

Logon time:           0

Logoff time:          never

Kickoff time:         never

Password last set:    Qua, 04 Dez 2019 15:35:58 -03

Password can change:  Qua, 04 Dez 2019 15:35:58 -03

Password must change: never

Last bad password   : 0

Bad password count  : 0

Logon hours         : FFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF


[GitHub](http://github.com - automatic!
[GitHub](https://raw.githubusercontent.com/murilothink/servidorsamba/master/Capturar.PNG)
