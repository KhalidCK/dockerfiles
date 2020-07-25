FROM jupyter/scipy-notebook

USER $NB_UID
WORKDIR /opt/app/data
COPY jupyterlab/requirements.txt .
RUN pip install --upgrade --force-reinstall --no-deps --no-cache-dir -r requirements.txt
RUN conda install -c conda-forge altair_saver
RUN jupyter labextension install @jupyterlab/toc
EXPOSE 8888

CMD jupyter lab --ip=* --port=8888 --no-browser --notebook-dir=/opt/app/data --allow-root