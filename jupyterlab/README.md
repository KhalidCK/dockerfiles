# README

## Usage

Set aliase on fish shell

```bash
alias mylab='docker run --rm -it -p 8888:8888 -v (pwd):/opt/app/data -v /datalake:/mnt/data -v $HOME/.aws:/home/jovyan/.aws khalidck/jupyterlab'
```