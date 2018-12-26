#language utilisé
FROM python:3

#ajoute les fichiers necessaires
ADD __main__.py /
ADD _version.py /
ADD requirements.txt /

#ajoute les authorisation sur les scripts python
RUN chmod 777 /*

#pre requis pour utiliser le fichier python
RUN pip install -r requirements.txt

#lance le script python
CMD [ "python", "./__main__.py" ]
