#language utilisé
FROM python:3

#ajoute les fichiers necessaires
ADD __main__.py /
ADD _version.py /
ADD requirements.txt /

#ajoute les authorisation sur le script python
RUN chmod 777 /*.py

#pre requis pour utiliser le fichier python
RUN pip install -r requirements.txt

#lance le script python
ENTRYPOINT [ "python", "./__main__.py -H 146.148.21.137 -P 27017 -D db-sam -u admsk -p unPasswordQuiVaBien -A 146.148.21.137" ]

#expose le port reseaux mongodb
EXPOSE 27017
