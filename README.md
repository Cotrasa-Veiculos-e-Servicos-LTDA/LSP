# LSP - Linguagem Sênior de Programação - Exemplos de códigos

- Documentação da Linguagem LSP - https://documentacao.senior.com.br/tecnologia/6.2.35/index.htm#lsp/sintaxe-de-comandos-e-operadores.htm

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
EnviaEMail("Joao","joao@senior.com.br", "", "", "Teste","\"\\\\Servidor\\teste.txt\"", "");

Como pode ser visto no exemplo acima, está sendo passado um endereço de um arquivo que normalmente seria: \\Servidor\teste.txt. Entretanto ao passar literalmente nas regras é necessário colocar uma \ (barra) antes das "" (aspas) e da \ (barra) para que estes caracteres não funcionem como caracteres especiais.

Se a barra não fosse adicionada antes destes caracteres, eles funcionariam de forma especial, ou seja, a \ (barra) é usada para quebra de linha quando o texto é muito extenso para ser visualizado em tela e as "" (aspas) são usadas para passar (entre as mesmas) expressões literais.
