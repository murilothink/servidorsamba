# Configurações do Servidor Samba


Criar um diretorio na pasta /home/ chamado "arquivos" 
  Comando para criar: mkdir arquivos
  
Permissão da pasta.
chmod -R 777 /home/caminho/da_pasta ou chmod -R 770 /home/caminho/da_pasta
 
Obs: 777 vai ser para diretorios publicos na rede. Ou seja todos irão ter permissão, mas isso deve ser devido no arquivo Global /etc/samba/smb.conf. conforme esta no artigo github. Faça um clone 
