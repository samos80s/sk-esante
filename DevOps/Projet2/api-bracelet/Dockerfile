#language utilisé
FROM python:3

#ajoute les fichiers necessaires
ADD __main__.py /
ADD requirements.txt

#pre requis pour utiliser le fichier python
RUN pip install -r requirements.txt

#lance le script python
CMD [ "python", "./__main__.py" ]

#expose les port reseaux
#EXPOSE 80 8080
