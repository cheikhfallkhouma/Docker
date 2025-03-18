FROM python:3.8-buster
LABEL maintainer="cheikhfallkhouma"
COPY student_age.py /
RUN apt update -y && apt install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
COPY requirements.txt /
RUN pip3 install -r /requirements.txt
VOLUME /data
EXPOSE 5000
CMD [ "python3", "./student_age.py" ]


# # 1️⃣ Image de base
# FROM python:3.8-buster

# # 2️⃣ Mainteneur
# LABEL maintainer="cheikhfallkhouma"

# # 3️⃣ Installation des dépendances système
# RUN apt update -y && apt install -y \
#     python-dev python3-dev libsasl2-dev \
#     libldap2-dev libssl-dev 

# # 4️⃣ Copie du code source dans le conteneur
# # Copie tout le projet dans la racine
# WORKDIR /
# COPY . /  

# # 5️⃣ Copie et installation des dépendances Python
# COPY requirements.txt /requirements.txt
# RUN pip3 install -r /requirements.txt

# # 6️⃣ Création du volume pour les données persistantes
# VOLUME [ "/data" ]

# # 7️⃣ Exposition du port 5000
# EXPOSE 5000

# # 8️⃣ Commande d’exécution
# CMD [ "python3", "./student_age.py" ]
