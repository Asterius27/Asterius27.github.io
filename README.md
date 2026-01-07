Personal Website

To test the website locally:

```
sudo docker run --rm -it -p 4000:4000 -v "$PWD":/srv/jekyll jekyll/jekyll jekyll serve
```