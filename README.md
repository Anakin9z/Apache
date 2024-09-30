# Apache
PREMIÈRE PARTIE – CRÉATION D’UN SITE WEB (5 POINTS)
1. Installation et configuration du serveur Apache pour qu’il lise les pages Web dans le
répertoire « /var/www/html_tp1 ».
➢ Vous devez copier le fichier httpd.conf vers httpd.conf.original.
➢ Vous devez renommer votre serveur « serveurX » (où xx = # votre poste).
➢ Utiliser l’adresse 192.168.1.1 pour accéder au site web de votre serveur.
➢ Démarrer de façon permanente le service httpd.
2. Créez une nouvelle page d’accueil nommée index.html dans le répertoire
/var/www/html_tp1.
3. La page doit contenir toutes les balises suivantes (chaque balise doit être utilisée au
moins une fois):
➢ <html>, <head>, <title>, <body>, <p>, <hr>, <a href>, <img>, <br>, <b>, <i> et
<u>.
➢ Le titre de la page doit être Page d’accueil TP1
➢ Vous devez ajouter un lien vers chaque page Web de ce TP à l’intérieur de la
page index.html. Ce lien devrait ouvrir la page Web qui correspond à la
question permettant ainsi d’en tester son fonctionnement. Voir exemple à la
dernière page de ce TP.
DEUXIÈME PARTIE – SITE WEB DES UTILISATEURS (10 POINTS)
1. Créer un nouvel utilisateur tp1.
2. Les pages Web de l’utilisateur tp1 devront être placées dans le répertoire:
/home/tp1/www.
3. Créer une page web simple, que vous appellerez tp1.html dans le répertoire de
l’usager /home/tp1/www.
4. Modifier les permissions sur le répertoire tp1 et dans selinux, en utilisant ces deux
commandes :
sudo chmod -R 755 /home
sudo setsebool -P httpd_enable_homedirs true
5. Configurer le serveur Apache pour permettre l’accès aux répertoires des
utilisateurs. Astuce : Configurer le fichier userdir.conf.
6. Configurer le serveur Apache pour qu’il prenne la page tp1.html en plus de
index.html comme pages de défaut.
TROISIÈME PARTIE – AUTHENTIFICATION (20 POINTS)
Les questions de cette partie se font dans le répertoire /var/www/html_tp1.
Pour chaque numéro, vos tests doivent démontrer que votre site Web respecte
chacune des conditions de la question.
1. Créez un répertoire secure1 et configurez Apache en utilisant la directive
<Directory> afin que seulement l’utilisateur toto qui utilise le mot de passe secret
puisse y avoir accès. Tous les autres utilisateurs ne pourront pas y accéder. Ne
placez pas le fichier des mots de passes (ex: .htpasswd) dans un répertoire
accessible par un utilisateur normal (utilisez le répertoire suggéré en classe lors de
la présentation du sujet).
2. Créez un répertoire secure2 et configurez Apache en utilisant la directive
<Location> pour permettre les mêmes accès que la question précédente.
3. Créez un répertoire secure3 et configurez Apache pour que seulement
l’utilisateur toto de l’exemple précédent puisse y avoir accès s’il se connecte à partir
du sous réseau 192.168.1.0/24
4. Créez un répertoire secure4 et configurez Apache pour seulement l’utilisateur
toto OU tout utilisateur provenant du sous réseau 192.168.1 puissent avoir accès.
4. Créez un répertoire secure5 et configurez-le comme secure1 mais l'accès doit être
autorisé à l'utilisateur tata seulement.
5. Créez un répertoire secure6 et placez-y un fichier .htaccess pour définir que
seulement l’utilisateur toto a accès aux pages Web de ce répertoire.
6. Créez un répertoire secure7 et placez-y un fichier .htaccess pour définir que
seulement l’utilisateur toto de l’exemple précédent puisse y avoir accès s’il se
connecte à partir du sous réseau 192.168.1
7. Créez un répertoire secure8 et placez-y un fichier .htaccess pour définir que
seulement l’utilisateur « toto » ou tout utilisateur provenant du sous réseau
192.168.1 puissent avoir accès.
