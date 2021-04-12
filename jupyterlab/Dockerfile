FROM jupyter/pyspark-notebook:aec555e49be6

USER $NB_UID
WORKDIR $HOME
COPY requirements.txt .
RUN pip install --upgrade --no-cache-dir jupyterlab-git 
#-r requirements.txt
RUN jupyter lab build 