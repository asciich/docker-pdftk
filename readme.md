# pdftk container

Dockerized pdftk to manipulate PDF documents. To use pdftk start the container:

```
docker run --rm -u $(id -u):$(id -g) -v $(pwd):/working_dir/ -it asciich/pdftk
# Inside the container
cd /working_dir
pdftk ... # See examples below
```

## pdftk examples

Split a multipage PDF into single page PDFs:

```
pdftk input.pdf burst output output_%02d.pdf compress
```