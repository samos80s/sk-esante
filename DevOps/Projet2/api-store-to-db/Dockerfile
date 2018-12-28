#language utilisé
FROM python:3

#ajoute le fichier python contenant l'api
ADD __main__.py /
ADD requirements.txt /

#ajoute les authorisation sur le script python
RUN chmod 777 /__main__.py

#pre requis pour utiliser le fichier python
RUN pip install -r requirements.txt

#lance le script python
CMD [ "python", "./__main__.py -H 146.148.21.137 -P 27017 -D db-esante -u admsk -p unPasswordQuiVaBien -A 146.148.21.137" ]

#expose les port reseaux
#EXPOSE 80 8080
