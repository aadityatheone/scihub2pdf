# SciHub to PDF(Beta)

![](https://raw.githubusercontent.com/bibcure/logo/master/gifs/scihub.gif) 
## Description

scihub2pdf is a module of [bibcure](https://github.com/bibcure/bibcure)

Downloads pdfs via a DOI number, article title or a bibtex file, using the
database of libgen,  Sci-Hub and Arxiv.

## Install

```
$ sudo python /usr/bin/pip install scihub2pdf
```
If you want  to download files from scihub you will need to get  PhantomJS

### OSX
```
$ npm install -g phantomjs
```
### Linux Using npm

```
$ sudo apt-get install npm
$ sudo npm install -g phantomjs
```



## Features and how to use

Given a bibtex file
```
$ scihub2pdf -i input.bib
```

Given a DOI number...
```
$ scihub2pdf 10.1038/s41524-017-0032-0
```

Given a title...
```
$ scihub2pdf --title An useful paper
```

Arxiv...
```
$ scihub2pdf arxiv:0901.2686
$ scihub2pdf --title arxiv:Periodic table for topological insulators
```

Location folder as argument
```
$ scihub2pdf -i input.bib -l somefoler/
```

Use libgen instead sci-hub

```
$ scihub2pdf -i input.bib --uselibgen
```

## Sci-hub:

- Stable
- Annoying CAPTCHA
- Fast


## Libgen

- Unstalbe
- No CAPTCHA
- Slow

## Download from list of items

Given a text file like

```
10.1038/s41524-017-0032-0
10.1063/1.3149495
.....
```
download all pdf's
```
$ scihub2pdf -i dois.txt --txt
```
Given a text file like

```
Some Title 1
Some Title 2
.....
```
download all pdf's
```
$ scihub2pdf -i titles.txt --txt --title
```
Given a text file like

```
arXiv:1708.06891
arXiv:1708.06071
arXiv:1708.05948
.....
```
download all pdf's
```
$ scihub2pdf -i arxiv_ids.txt --txt
```
