
# LSP - Linguagem Sênior de Programação - Exemplos de códigos

- Documentação da Linguagem LSP - <https://documentacao.senior.com.br/tecnologia/6.2.35/index.htm#lsp/sintaxe-de-comandos-e-operadores.htm>

# Sintaxe de comandos e operadores

## Operadores Lógicos

| Sinal | Descrição |
| --- | --- |
| = | Sinal Igual: Utilizado em comparações/operações aritméticas. |
| > | Maior que. |
| < | Menor que. |
| <> | Diferente de. |
| >= | Maior ou igual a. |
| <= | Menor ou igual a. |
| e | E. Utilizado com o comando "Se" para ligar várias condições, em que todas devem ser verdadeiras para que o resultado da comparação seja verdadeira. |
| ou | OU. Utilizado com o comando "Se" para ligar várias condições, devendo apenas uma condição ser verdadeira para que o resultado da comparação seja verdadeiro. |

## Operadores aritméticos

| Sinal | Descrição |
| --- | --- |
| = | Sinal Igual: Utilizado em comparações/operações aritméticas. |
| > | Maior que. |
| < | Menor que. |
| <> | Diferente de. |
| >= | Maior ou igual a. |
| <= | Menor ou igual a. |
| e | E. Utilizado com o comando "Se" para ligar várias condições, em que todas devem ser verdadeiras para que o resultado da comparação seja verdadeira. |
| ou | OU. Utilizado com o comando "Se" para ligar várias condições, devendo apenas uma condição ser verdadeira para que o resultado da comparação seja verdadeiro. |

## Operadores Extras

| Sinal | Descrição |
| --- | --- |
| /* | Inicio de comentário |
| */ | Final de Comentário |
| @ | Comentário de uma linha |

## Definição de variáveis

O nome das variáveis declaradas na LSP devem ter no máximo 100 caracteres, estes nomes podem ser separados por _ (sublinhado). Não é permitido usar acentuação no nome das variáveis.

Como melhor prática para as variáveis serem inicializadas, se atribui o valor no evento Inicialização, sendo o primeiro a ser chamado.

## Caracteres com Comportamento Especial

Existem determinados caracteres que, quando inseridos eu uma expressão literal nas regras, devem ser precedidos do caractere \ (barra) para indicar que estes caracteres serão usados literalmente e não como caracteres especiais. Estes caracteres são: "" (aspas) e \ (barra).

> Exemplo
> 
> ~~~LSP
> EnviaEMail("Joao","joao@senior.com.br", "", "", "Teste","\"\\\\Servidor\\teste.txt\"", "");
> ~~~
> 
> Como pode ser visto no exemplo acima, está sendo passado um endereço de um arquivo que normalmente seria: \\Servidor\teste.txt. Entretanto ao passar literalmente nas > regras é necessário colocar uma \ (barra) antes das "" (aspas) e da \ (barra) para que estes caracteres não funcionem como caracteres especiais.
> 
> Se a barra não fosse adicionada antes destes caracteres, eles funcionariam de forma especial, ou seja, a \ (barra) é usada para quebra de linha quando o texto é > muito extenso para ser visualizado em tela e as "" (aspas) são usadas para passar (entre as mesmas) expressões literais.

## Palavras Reservadas

A LSP não faz distinção de letras maiúsculas e minúsculas. Portanto, a LSP possui 51 (cinquenta e uma) palavras reservadas que não poderão ser usadas pelo programador para outros fins.

Válida para todos os locais de definição de regras ou fórmulas, traz a relação dos comandos permitidos nas regras. Podemos então selecionar o comando desejado com as setas e pressionar ENTER para que este seja deslocado para o texto da regra, na posição do cursor, sendo que também é possível digitá-las.

| Comando | Descrição |
| --- | --- |
| Se ( ) | Comando de comparação/pergunta, com resposta verdadeiro ou falso. |
| Senao | É a saída da pergunta (Se) quando a resposta for falsa. |
| e | Liga duas ou mais condições, devendo todas serem verdadeiras para o resultado ser verdadeiro. |
| ou | Liga duas ou mais condições, bastando uma ser verdadeira para o resultado ser verdadeiro. |
| Inicio | Marcador utilizado para iniciar um bloco. |
| Fim; | Marcador utilizado para finalizar um bloco. |
| Para | Comando utilzado para se fazer um loop de comandos. Ou seja, fazer com que um bloco de comandos seja executado determinado número de vezes. Indica-se um \<valor inicial\> e esse valor é incrementado pelo valor do \<contador\> até que a \<condicao\> seja falsa. Sintaxe: Para (\<valor inicial\>; \<condicao\>; \<contador\>); |
| Enquanto | Comando utilizado para se fazer um loop de comandos. Ou seja, fazer com que um bloco de comandos seja executado determinado número de vezes até que a \<condição>, seja falsa. Sintaxe: Enquanto (\<condicao\>); |
| Pare | Interrompe a execução de um bloco do comando Para ou Enquanto. O Pare, simplesmente faz com que o sistema abandone o bloco de comandos e continue a execução do restante das regras. Sintaxe: Pare;|
| Cancel (1) | Se for utilizado em uma regra do evento "Antes de Imprimir" de uma seção, cancela a impressão da seção. Se for usado no evento "Na Impressão" de um campo, cancela a impressão deste campo. Sintaxe: Cancel (1); |
| Cancel (2) | Deve ser usado em conjunto com as variáveis de sistema ValStr ou ValRet e somente no Evento "Na Impressão". O valor alfa atribuído para ValStr seguido de Cancel (2) será impresso no campo em que foi implementada a regra. Sintaxe: Cancel (2); |
| Mensagem | Exibe uma mensagem para o usuário durante a execução da regra. Sintaxe: Mensagem (\<tipo_da_mensagem\>,"\<mensagem\>"); |
| Vapara | Desvia a execução da regra para o \<rótulo\> determinado. Sintaxe: Vapara \<rótulo\>; |
| Regra | Chama uma outra regra, identificada pelo \<número da regra\>. Sintaxe: Regra (\<numero_da_regra\>); |
| Continue | Continua a execução de um loop feito pelo comando Para. Ou seja, se quiser que o loop não seja executado em determinado caso, faça o teste da condição e com ela use o comando. Sintaxe: Continue; |
| End | Usado na definição de uma função, para indicar qual parâmetro retornará valor. Sintaxe: Funcao Teste (end \<tipo do parâmetro\> \<nome do parâmetro\>); |
| Abrir |	Abre o \<arquivo informado\>, no \<modo de abertura\> desejado. Se o arquivo não existir ele é criado. Ele retorna um manipulador de arquivos. Sintaxe: Manipulador_de_Arquivo = Abrir (“\<nome_do_arquivo\>”,\<modo_de_abertura\>); Onde o Modo de Abertura pode ser: Ler ou Gravar. |
| Fechar |	Fecha o arquivo aberto pela função Abrir. Sintaxe: Fechar (\<manipulador_de_arquivo\>); |
| Ler |	Lê uma \<quantidade de caracteres\> do arquivo especificado no \<manipulador de arquivo\> e joga o valor lido em uma \<variável\>. Sintaxe: Ler (\<manipulador_de_arquivos\>, \<variavel\>,\<tamanho\>); |
| Gravar |	Grava o valor de uma \<variável ou de uma constante> no \<manipulador de arquivos\>. Sintaxe: Gravar (\<manipulador_de_arquivos\>,\<variável ou constante>,\<tamanho\>); |
| Lernl |	Lê uma linha no arquivo indicado pelo \<manipulador de arquivos\> e joga o valor lido em uma \<variável\>. Sintaxe: Lernl (\<manipulador_de_arquivos\>,\<variável\>); |
| Gravarnl |	Grava uma linha no arquivo indicado pelo \<manipulador de arquivos\> com o valor contido na variável especificada. Sintaxe: Gravarnl (\<manipulador_de_arquivos\>,\<variável ou constante\>); |
| Inserir |	Faz com que o sistema, insira um arquivo na regra atual, em tempo de execução/compilação. Sintaxe: Inserir “\<nome_arquivo\>”; |
| ValStr |	Usado apenas no gerador, para alterar a descrição de um campo tipo Descrição. O texto passada para ValStr será impresso no lugar da descrição original do campo. ValStr = Teste; Cancel(2);	|
| Cursor |	Os cursores nada mais são que um SELECT em uma regra, retornando registros que satisfaçam a condição informada na propriedade SQL de um Cursor. Observações: O SELECT utilizado no cursor não possui relacionamento direto com o SELECT utilizado pelo gerador de relatórios, por exemplo. |

## Funções

- Abrir (Open)
Abre o arquivo informado em nome do arquivo para o modo de abertura informado (Ler/Gravar). Se o arquivo não existir, ele é criado. Ele retorna um manipulador de arquivos.

Sintaxe: Abrir ("\<nome do arquivo\>",\<modo de abertura\>);

Exemplo
~~~LSP
arq = Abrir ("Teste.txt",Ler);
~~~
