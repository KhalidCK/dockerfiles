# cmdBOX

My favorite command line tools dockerized 

## Usage

```sh
docker run --rm -it khalidck/cmdbox
```

Override `home` (useful for custom dotfiles)

```sh
docker run --rm -it --mount type=bind,source=$(pwd),target=/home/kh khalidck/cmdbox
```
