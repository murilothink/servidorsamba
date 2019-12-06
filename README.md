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


![Legenda](https://github.com/murilothink/servidorsamba/blob/master/Capturara.PNG?raw=true)
