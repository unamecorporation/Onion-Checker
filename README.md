## Onion Checker

<pre>
Be welcome to the ...

.d88888b.            d8b
d88P" "Y88b          Y8P
888     888
888     888 88888b.  888  .d88b.  88888b.
888     888 888 "88b 888 d88""88b 888 "88b
888     888 888  888 888 888  888 888  888
Y88b. .d88P 888  888 888 Y88..88P 888  888
 "Y88888P"  888  888 888  "Y88P"  888  888


                                                                 888
 .d8888b.  888                        888                        888
d88P  Y88b 888                        888                        888
888    888 888                        888                        888
888        88888b.   .d88b.   .d8888b 888  888  .d88b.  888d888  888
888        888  88b d8P  Y8b d88P"    888 .88P d8P  Y8b 888P     888
888    888 888  888 88888888 888      888888K  88888888 888 
Y88b  d88P 888  888 Y8b.     Y88b.    888 "88b Y8b.     888      d8p
 "Y8888P"  888  888  "Y8888   "Y8888P 888  888  "Y8888  888      Y8P
 </pre>

O Onion Checker é um testador de links da rede do Tor. Além de testar, ele cataloga os títulos dos sites que estiverem online, bem como agrupa outra lista com os links que estiverem offline, com base no conteúdo do arquivo de links passado para o testador.

**Utilidade:** Faz-se útil quando o usuário navega na rede Onion e não quer testar cada site que encontra um por um, manualmente. O programa faz o teste desses links pra você, e os agrupa permitindo-o saber previamente do que se trata.

Ele pode ainda ser usado para pegar links de arquivos, seja ele o tipo de for, como uma página HTML, ou um texto, um livro, ou qualquer arquivo em texto plano que contenha links. Pode ainda agrupar diferentes listas de links em um único arquivo, removendo duplicatas e removendo também links que não sejam da rede Onion.

Esse programa funciona em qualquer computador que contenha o **Bash v4.0+**, seja ele Linux, MAC ou Windows. Pode ainda ser instalado ou usado diretamente do script.

Ele é parte da categoria de Anonimato existente no Kurupira, para mais informações, procure essa parte na documentação do sistema ou no nosso site.
<p style="page-break-before: always">

## Help

Abaixo você pode conferir o menu help da ferramenta:

<pre>
Olá! Seja bem-vindo(a) ao tópico de ajuda do Onion Checker.
Com esse software você poderá checar se links onion estão 
funcionando. Abaixo você pode ver a lista de comandos dis-
poníveis.
Se algum comando precisar de argumento e não for dado, o  
mesmo apresentará a mensagem do uso correto.

-h ou --help            Mostra essa mensagem de ajuda;
-l ou --link-org        Organiza os links de um arquivo;
-b ou --banner          Exibe o banner e sai;
-t ou --tor-check       Checa a existência do Tor no computador;
-c ou --check-link      Checa por links online e manda criar
arquivo linkson.txt com os títulos e links online, caso
nenhum nome destino seja dado.
-j ou --join-lists      Une arquivos contendo links ou outro
conteúdo;
--install          Transfere o programa para o diretório /usr/bin
  permitindo sua execução de forma global;
--uninstall         Remove completamente o software do computador. 
</pre>

## Exemplo de uso

Para usar a funcionalidade de teste de links online, necessitamos de um ***arquivo*** contendo os *links a serem testados*. Nesse exemplo utilizarei o arquivo *link.txt*, contendo o link `http://gjobqjj7wyczbqie.onion/`

Para usar a ferramenta, basta digitar `onion-checker -c <nomedoarquivo>`. No nosso caso, troquemos *<nomedoarquivo\>* por *link.txt*, resultando em `onion-checker -c links.txt`.

Vale lembrar que esse programa tem como dependência os pacotes ` tor torsocks curl coreutils `. Na primeira vez que for usar, ele irá buscar pelo tor rodando, se não estiver, ele o iniciará automaticamente. Iniciado o *tor daemon*, o banner será apresentado, depois é questionado quanto ao timeout que o usuário deseja, e então os links começarão a ser testados. No exemplo ele resulta:

<pre>
Nome destino mantido padrão, escrevendo para arquivo /home/jesus/linkson.txt

Inicializando a checagem dos links...

Que timeout você quer para que os links sejam dados como offline?
Pressione enter para o valor padrão (20s).
Ex: [10 | 20s | 30m | 1h | 3d] para segundo, minuto, hora e dia. 
Segundo é a unidade padrão, caso omitida a letra.

Valor padrão para timeout: 20

Iniciando a checagem dos links...

[1] O link http://gjobqjj7wyczbqie.onion/ está funcionando...
</pre>

Onde o caminho para o arquivo será sempre sua `$HOME`, caso omitido o arquivo de destino. Vale lembrar que ele cria um arquivo separado par aos arquivos offline.


**Autor:** Jesus Santos

**Colaboradores:** Equipe de desenvolvimento de ferramentas daUnameCorporation

**Licensa**: GPLv3

**GitHub:** https://github.com/unamecorporation/Onion-Checker
