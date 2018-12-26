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
CMD [ "python", "./__main__.py -H localhost -P 27017 -D db-esante -u esante -p Lenovo10 -A localhost" ]

#expose les port reseaux
#EXPOSE 80 8080
