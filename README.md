# dwca2parquet
converts darwin core archive to apache parquet

## dependencies

1. singularity v3.0 https://www.sylabs.io/guides/3.0/user-guide/
2. debian / ubuntu 


## build

run ```sudo singularity build dwca2parquet.sif dwca2parquet.def```

## install

run ```sudo cp dwca2parquet.sif /usr/local/bin/dwca2parquet```

## usage 

dwca2parquet [dwc meta.xml url] ...

## example

```console
$ wget -O dwca.zip https://deeplinker.bio/5cba2f513fee9e1811fe023d54e074df2d562b4169b801f15abacd772e7528f8 
$ unzip dwca.zip
$ ls -1 
...
meta.xml
...
taxa.txt
...
$ dwca2parquet meta.xml
...
$ ls -1
...
meta.xml
...
taxa.txt
taxa.txt.parquet  <--- core table parquet dir generated by dwca2parquet 
...
