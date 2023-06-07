# Comandos de arquivo 

- **pwd** retorna o path local onde estamos localizados no terminal

- **ls** retorna a lista de conteúdos/diretorias do path onde estamos
    1. -l
    retorna mais detalhes na listagem: caso não inicia com letra 'd' significa que não é um diretório

    2. -la
    retorna os detalhes de na listagem incluindo arquivos ocultos

    3. .
    o '.' representa o diretório atual, caso rodarmos [ls .] listaremos os dados do dir atual. Podemos ver ele com o comando ls -la

    4. '..' representa o dir antecessor na hierarquia, caso rodarmos [ls ..] listaremos os dados do dir anterior na hierarquia. Também
    podemos ver sua referencia no comando ls -la

    5. /
    comando [cd /] ou [cd] direciona para o user dir

- **echo**
    - [args]
    o comando echo reproduz o arg no console. Caso eu digite: Bem Vindo. O echo entenderá 2 args [Bem, Vindo], caso informar
    "Bem Vindo" com as aspas duplas. Estou informando um arg apenas
    1. >
    o caractere '>' redireciona o content do echo, podendo inseri-lo por exemplo em um arquivo .txt
    Caso ja exista um arquivo com o nome definido o comando sobrescreverá o conteúdo do arquivo

    2. >>
    o caractere '>>' concatena o arg com os dados ja existentes no arquivo de redirecionamento
    
~~~ bash
$ echo 'Ola Mundo' > ola-mundo.txt    
~~~

- **cat**
    1. [arg]
    pode ser um arquivo de any extensão, o sistema vai ler e printar o conteúdo do arquivo informando como arg
~~~ bash
$ cat ola-mundo.txt
~~~
é possível ler pegar vários arquivos, caso eu tenha os arquivos teste1.txt, teste2.txt, teste3.txt
posso rodar
~~~ bash
$ cat teste*.txt
~~~
assim printa todos os dados de todos arquivos que iniciam com nome teste
também posso printar todo arquivos que tem extensão txt, funcionando para qualquer extensão
~~~ bash
$ cat *.txt
~~~

- **man** 
    1. [arg] O arg é um comando, no qual vai retorna o manual sobre o comando informado como argumento 
    
- **whoami** comando retorna o nome do user

- **clear** | **control+l** limpar o terminal

- **touch** toca no arquivo. Caso verificarmos os detalhes do arquivo veremos que ele terá a data de atualização atualizada. Mesmo
sem modificar nada com o touch
1. [arg] o arquivo a ser tocado


- **head** ler por default as 10 primeiras linhas de  arq
1.  [arg] o arquivo a ser lido
 -n [n] podemos informar a  quantidade de linhas que o head retornará


 - **tail** ler por default as 10 ultimas linhas de  arq
1.  [arg] o arquivo a ser lido
 -n [n] podemos informar a  quantidade de linhas que o tail retornará
 
 - **less** retorna o arquivo lido com um scroll para a navegação da leitura
 1.[arg] o arquivo que sera lido