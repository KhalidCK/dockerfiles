# README

## Usage

Set aliase on fish shell

```bash
alias mylab='docker run --rm -it -p 8888:8888 -v (pwd):/opt/app/data -v /datalake:/mnt/data -v $HOME/.aws:/home/jovyan/.aws khalidck/jupyterlab'
```

You can customize the image at runtime (e.g. to use [sudo within container](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/recipes.html#using-sudo-within-a-container))
