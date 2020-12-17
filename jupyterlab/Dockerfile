FROM jupyter/scipy-notebook

USER $NB_UID
VOLUME /opt/app/data
WORKDIR /opt/app/data
COPY requirements.txt .
RUN pip install --upgrade --no-cache-dir -r requirements.txt
RUN jupyter labextension install @jupyterlab/toc