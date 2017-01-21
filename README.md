# Onion-Checker
### (Em Desenvolvimento)

##### Script para testar se hidden services no Tor estão em fucionamento, bem como catalogá-los de forma simples. (Funções adicionais sendo implementadas).

# Funcionalidades

[+] **_Implementadas Totalmente:_**

- [x] *Link Organization - Impressão em arquivo ou tela;*

- [x] *Check Tor Installation;*

- [x] *Check Link with timeout set by user;*

- [x] *Unir arquivos de texto em um só - Impressão em arquivo ou tela;*

- [x] *Instalar/Desinstalar o script*.

[+] **_Implementadas Parcialmente:_**



#### Especificações de uso contidas no --help do arquivo:
Olá! Seja bem-vindo(a) ao tópico de ajuda do Onion Checker.
Com esse software você poderá checar se links onion estão  funcionando. Abaixo você pode ver a lista de comandos disponíveis.
Se algum comando precisar de argumento e não for dado, o mesmo apresentará a mensagem do uso correto.

>-h ou --help            Mostra essa mensagem de ajuda;

>-l ou --link-org        Organiza os links de um arquivo;

>-b ou --banner          Exibe o banner e sai;

>-t ou --tor-check       Checa a existência do Tor no computador;

>-c ou --check-link      Checa por links online e manda cria arquivo linkson.txt com os títulos e links online, caso nenhum nome destino seja dado .

>-j ou --join-lists      Une arquivos contendo links ou outro conteúdo;

> --install              Transfere o script para o `PATH` dos executáveis (`/usr/bin/`);

> --uninstall            Apaga qualquer versão instalada do programa.

### Compatível apenas com bash 3+. Disponível para Linux, MAC e Windows 10.

#### Dependências:
*tor   torsocks  curl    coreutils*


# History 

*21/01/2017 -* Adicionadas as funções de Instalar e Desinstalar o script, que transferem o mesmo para o diretório `/usr/bin`. Adicionado suporte ao bash_autocompletion, possibilitando ao usuário auto-completar suas flags ou arquivos dados como argumentos ao programa. Correção de textos imprimidos ao usuário. Adicionados mais textos para maior entendimento dos processos no decorrer do uso.

*17/01/2017 -* Corrigida função de união de arquivos que estava sem a funcionalidade de impressão do conteúdo na tela. Trocada a flag que faz a impressão na tela de -t para -st para não haver confusão com a flag [-t| --tor-check].

*17/01/2017 -* Adicionada função para união de vários arquivos de texto em um único, ou imprime o resultado na tela. Adicionado suporte à função de organização que aceita qualquer quantidade de arquivos de entrada e manda para um de destino, ou imprime o conteúdo todo na tela. Mudada a forma com que o timeout é setado para o link-check, tendo valor default (ao pressionar enter sem nada) de 20 segundos.

*16/01/2017 -* Função de checagem de links totalmente implementada com timeout escolhido pelo próprio usuário. Teste feito com base em função if-else com regex, bem documentada no source code; Novas implementações nos comandos de limpeza para organização de links, abrangendo gama maior nos arquivos filtrados; Documentação das novas/editadas funções.

*14/01/2017 -* Função de organização de links totalmente implementada e simplificada pro usuário final. Função pra checagem da existência do Tor simplificada e adiciona retorno para exibição ao usuário. Código totalmente comentado à partir de agora.

*13/01/2017 -* Função implementada parcialmente: Filtragem de lista de links onion passada pelo programa. Criação de menu de ajuda e suporte à flags e argumentos de flags. Funções ainda sendo implementadas, link-org é a primeira a estar quase finalizada.

*05/01/2017 -* Começado o trabalho de elaboração do script e estudo de casos para decidir com base em que ferramentas ele trabalhará e a complexidade do mesmo. Decidido até o momento: Será feito em shell.
