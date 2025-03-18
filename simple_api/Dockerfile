# 1️⃣ Image de base 
FROM python:3.8-buster

# 2️⃣ Mainteneur
LABEL maintainer="Cheikh Fall KHOUMA"

# 3️⃣ Copier le code source de l'API dans le conteneur à la racine du chemin "/"
COPY student_age.py /

# 4️⃣ L'API utilise le moteur FLASK, installation d'un package
RUN apt update -y && apt install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y

# 5️⃣ Copie et installation des dépendances Python
COPY requirements.txt /
RUN pip3 install -r /requirements.txt

# 6️⃣ Création du volume pour les données persistantes
VOLUME /data

# 7️⃣ Exposition du port 5000
EXPOSE 5000

# 8️⃣ Commande d’exécution
CMD [ "python3", "./student_age.py" ]