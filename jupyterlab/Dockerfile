FROM jupyter/pyspark-notebook:584f43f06586

RUN conda install --quiet --yes \
    'turbodbc' && \
    conda clean --all -f -y && \
    fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"
USER $NB_UID
RUN pip install --upgrade --no-cache-dir \
    "jupyterlab-git>=0.30.*" \
    "jupyter-resource-usage==0.5.1" \
    "jupyterlab-code-formatter>=1.4.*" \
    # needed by code-formatter
    "black==20.8b1" \
    "isort==5.8.0"  \
    #ploting
    "plotly==5.0.0rc1" \
    "altair>= 4.1.*" 
