FROM jupyter/scipy-notebook

USER $NB_UID
WORKDIR /opt/app/data
COPY requirements.txt .
RUN pip install --upgrade --force-reinstall --no-deps --no-cache-dir -r requirements.txt
RUN jupyter labextension install @jupyterlab/toc
EXPOSE 8888

CMD jupyter lab --ip=* --port=8888 --no-browser --notebook-dir=/opt/app/data --allow-root