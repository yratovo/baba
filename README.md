# github1
# baba

ls -lart
pwd
## A cause du shell /bin/false du user jenkins, on est obligé de mettre une empreinte( pour 192.168.1.156) dans le fichier ~/.ssh/known_hosts <==> /var/lib/jenkins/.ssh/known_hosts
ssh-keyscan  -t rsa 192.168.1.156 >> ~/.ssh/known_hosts  2>/dev/null  

##Pour tester , je fais un ssh
ssh   root@192.168.1.156 ls -lart 

ansible-playbook  playbook.yml -i inventory --private-key ~jenkins/.ssh/id_rsa --tags "morondava_tomcat_tag"

