# Compactar com TAR
Por default o os comandos tar ja são recursivos

~~~ bash
$ tar -cz <dir/arq> > name-tar.tar.gz
~~~
**tar** usado para compactar/descompactar arquivos
1. [arg1, arg2] onde arg1 é o dir/arq que desejamos compactar usando o '>' para direcionar essa compactação para o arg2,
que é o nome do nosso arquivo de saída

2. -c parâmetro que informa que esta mos criando
3. -z parâmetro que informa que estamos zipando

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


se
