#language utilisé
FROM python:3

#creer un repertoire et l'affecte
RUN mkdir -p /api-store-to-db
WORKDIR /api-store-to-db

#ajoute les fichiers necessaires
ADD __main__.py /api-store-to-db/
ADD _version.py /api-store-to-db/
ADD requirements.txt /api-store-to-db/

#ajoute les authorisation sur le script python
RUN chmod +x /api-store-to-db/__main__.py

#pre requis pour utiliser le fichier python
RUN pip install -r /api-store-to-db/requirements.txt

#lance le script python
ENTRYPOINT [ "python", ".__main__.py -H db-sam -P 27017 -D db-sam -u "admsk" -p "unPasswordQuiVaBien" -A api-bracelet-skd" ]

#expose le port reseaux mongodb
EXPOSE 27017
