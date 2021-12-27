# Layout
 Understand folder structure of template and what everything contains

## Core Layout
```
project
│
│   readme.md
│   
│── master-src
│          templates
│           │
│           └──layouts
│               │
│               └──layout[x]
│                     layout[x].pug

```

> inside layout[x].pug you will find header and footer, those header and footer are in "shared" folder

```shell

## PUG

src: master-src/templates  
Dist: customer-src/layout[x]/dist

- Layouts
  - contains all the layout files (e.g. layout1, layout1-rtl & so on)
- src-pages
  - contains pages. We should add/edit pages here
- dist--extended-pages (Don't touch this folder and files, this are auto generated files)

```
