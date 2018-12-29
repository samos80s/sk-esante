#language utilisé
FROM python:3

#ajoute les fichiers necessaires
ADD __main__.py /api-store-to-db/
ADD _version.py /api-store-to-db/
ADD requirements.txt /api-store-to-db/

#ajoute les authorisation sur le script python
RUN chmod 777 /api-store-to-db/*.py

#pre requis pour utiliser le fichier python
RUN pip install -r /api-store-to-db/requirements.txt

#lance le script python
ENTRYPOINT [ "python", "/api-store-to-db/__main__.py -H 146.148.21.137 -P 27017 -D db-sam -u admsk -p unPasswordQuiVaBien -A 146.148.21.137" ]

#expose le port reseaux mongodb
EXPOSE 27017
