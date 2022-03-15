# Déploiement

Ce répertoire contient plusieurs fichiers qui permettront de déployer une machine virtuelle de type Debian avec des paramètres spécifiques :
* Le fichier template.json = Il est le fichier principal sous format JSON où se trouvent toutes les informations de la future machine virtuelle (à savoir la VM et ses caractéristiques, un groupe de sécurité, un réseau virtuel et un sous-réseau à l'intéireur, une interface réseau virtuelle ainsi qu'un disque).
* Le fichier parameters.json = Il contient toutes les informations citées ci-dessus (le premier fichier ne faisant qu'un appel aux paramètres afin de le rendre moins long et plus clair).

Pour déployer la ressource, il vous suffit d'apporter une modification au fichier principal "debian-logistic-deployment.yml", situé dans le dossier .gitflow, pour déclencher le workflow et créer la ressource sur Azure. Le déclencheur est mis sur "delete" pour éviter de déployer la ressource à chaque modification. Il suffit de moidifier ce déclencheur et de le mettre sur push pour déployer la ressource.
