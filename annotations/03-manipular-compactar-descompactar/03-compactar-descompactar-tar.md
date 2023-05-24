# Compactar com TAR
Por default o os comandos tar ja são recursivos

~~~ bash
$ tar -cz <dir/arq> > name-tar.tar.gz
~~~
**tar** usado para compactar/descompactar arquivos
1. [arg1, arg2] onde arg1 é o dir/arq que desejamos compactar usando o '>' para direcionar essa compactação para o arg2,
que é o nome do nosso arquivo de saída

2. -c parâmetro que informa que esta mos criando
3. -z parâmetro que informa que estamos zipando para o formato gz.

No caso tar -cz significa que estamos criando ao mesmo tempo que queremos zipar em tar.gz

4. -x extract. usamos para extrair um arquivo tar.gz

~~~ bash
$ tar -xz < name-arq-tar
~~~
Usamos o '>' para Saida/escrever e o '<' para ler/

## Formas sem usar os operadores de desvio '<','>'

compactar
~~~ bash
tar -czf arq.tar.gz arq-name
~~~

descompactar
~~~ bash
tar -xzf arq.tar.gz
~~~
5. -v verbose, usamos para printar os steps dos processos


## Resumo

Compacta
~~~ bash
tar -cz arquivo > arquivo.tar.gz
~~~
Descompacta
~~~ bash
tar -xz < arquivo.tar.gz
~~~

## Compactar para bzip2 com o tar

**compactar**
tar: base command
    -c: create
    -j: manejar bzip2 format

arq.ext: arquivo a compactar
\>: direcionando para o output no formato bz2
cmp.tar.bz2: nome do arquivo de saída no formato **bzip2** 

~~~ bash
tar -cj arq.ext > cmp.tar.bz2
~~~

**ler**
Para ler um arquivo tar
~~~ bash
tar -vtjf comp.tar.bz2
~~~
 -v: verbose
 -t: listar
 -f: não pode faltar, indica o uso do arquivo de argumento da leitura


**descompactar**

~~~ bash
tar -xj < cmp.tar.bz2
~~~
 -x: extract

**sem uso do '>'**

**compactar**
~~~ bash
tar -cjf cmp.tar.bz2 arq.ext
~~~
 -f: add '-f' não precisamos usar o '>' porém, é informado o output e depois o arquivo a se compactar

**descompactar**

~~~ bash
tar -xjf cmp.tar.bz2
~~~