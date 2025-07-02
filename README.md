# Documentação da Linguagem LSP - Linguagem Sênior de Programação

Sênior Sistemas

- Documentação da Linguagem LSP - <https://documentacao.senior.com.br/tecnologia>

## Índice

- [Introdução](#introdução)
- [Sintaxe e Estrutura](#sintaxe-e-estrutura)
  * [Estrutura Básica](#estrutura-básica)
  * [Case Sensitivity](#case-sensitivity)
  * [Identação e Espaçamento](#identação-e-espaçamento)
  * [Estruturas de Bloco](#estruturas-de-bloco)
- [Caracteres com Comportamento Especial](#caracteres-com-comportamento-especial)
- [Comentários](#comentários)
- [Palavras Reservadas](#palavras-reservadas)
- [Variáveis de Sistema](#variáveis-de-sistema)
- [Operadores](#operadores)
  * [Operadores Lógicos](#operadores-lógicos)
  * [Operadores Aritméticos](#operadores-aritméticos)
  * [Operadores Extras](#operadores-extras)
    + [Observação sobre o operador %](#observação-sobre-o-operador-%)
  * [Comportamentos Especiais](#comportamentos-especiais)
- [Tipo de Dados e Variáveis](#tipo-de-dados-e-variáveis)
  * [Tipos de Dados](#tipos-de-dados)
  * [Declaração ou Definição de Variáveis](#declaração-ou-definição-de-variáveis)
  * [Declaração ou Definição de Variáveis com Tamanho](#declaração-ou-definição-de-variáveis-com-tamanho)
  * [Forma de Acesso](#forma-de-acesso)
  * [Regras](#regras)
- [Manipulação Avançada de Strings](#manipulação-avançada-de-strings)
  * [Conceitos Fundamentais](#conceitos-fundamentais)
    + [Concatenação de Strings](#concatenação-de-strings)
    + [Quebra de Linha](#quebra-de-linha)
  * [Funções Básicas de Manipulação](#funções-básicas-de-manipulação)
    + [CopiarAlfa e CopiarStr](#copiaralfa-e-copiarstr)
    + [TamanhoAlfa e TamanhoStr](#tamanhoalfa-e-tamanhostr)
    + [PosicaoAlfa e PosicaoStr](#posicaoalfa-e-posicaostr)
    + [SubstAlfa e SubstAlfaUmaVez](#substalfa-e-substalfaumavez)
    + [Concatenar](#concatenar)
  * [Funções Avançadas de Manipulação](#funções-avançadas-de-manipulação)
    + [DeletarAlfa](#deletaralfa)
    + [ConverteParaMaiusculo e ConverteParaMinusculo](#converteparamaiusculo-e-converteparaminusculo)
    + [TrocaString](#trocastring)
    + [LerPosicaoAlfa](#lerposicaoalfa)
  * [Funções de Lista e Separação](#funções-de-lista-e-separação)
    + [ListaItem](#listaitem)
    + [ListaQuantidade](#listaquantidade)
  * [Funções de Codificação](#funções-de-codificação)
    + [ConverteCodificacaoString](#converteccodificacaostring)
    + [ConverteTexto](#convertetexto)
- [Criptografia e Segurança](#criptografia-e-segurança)
  * [Funções de Hash](#funções-de-hash)
    + [GeraHash](#gerahash)
  * [Criptografia de Dados](#criptografia-de-dados)
    + [Encriptar](#encriptar)
    + [Desencriptar](#desencriptar)
  * [Geração de Tokens e Nonces](#geração-de-tokens-e-nonces)
    + [GerarNonce](#gerarnonce)
    + [GeraToken](#geratoken)
    + [GeraSenha](#gerasenha)
  * [WS-Security e Digest](#ws-security-e-digest)
    + [GerarPwdDigest](#gerarpwddigest)
  * [Codificação Base64](#codificação-base64)
    + [Base64Encode](#base64encode)
    + [Base64Decode](#base64decode)
- [Cast de Variável](#cast-de-variável)
  * [AlfaParaData](#alfaparadata)
  * [AlfaParaDecimal](#alfaparadecimal)
  * [AlfaParaInt](#alfaparaint)
  * [IntParaAlfa](#intparaalfa)
  * [ConverteMascara](#convertemascara)
- [Manipulação Avançada de Datas](#manipulação-avançada-de-datas)
  * [Funções de Data Atual](#funções-de-data-atual)
    + [DataHoje](#datahoje)
    + [DataHora](#datahora)
    + [DataHoraUTC](#datahorautc)
  * [Construção e Decomposição de Datas](#construção-e-decomposição-de-datas)
    + [CodData](#coddata)
    + [DecodData](#decoddata)
  * [Operações Aritméticas com Datas](#operações-aritméticas-com-datas)
    + [AdicionarDias](#adicionardias)
  * [Formatação Avançada de Datas](#formatação-avançada-de-datas)
    + [FormatarData](#formatardata)
  * [Validação e Comparação de Datas](#validação-e-comparação-de-datas)
- [Validação e Verificação](#validação-e-verificação)
  * [Verificação de Abrangências](#verificação-de-abrangências)
    + [VrfAbrA](#vrfabra)
    + [VrfAbrN](#vrfabrn)
  * [Validação de Arquivos](#validação-de-arquivos)
    + [ArqExiste](#arqexiste)
  * [Validação de Dados Estruturados](#validação-de-dados-estruturados)
    + [RemoveExpressoesProibidas](#removeexpressoesproibidas)
  * [Verificação de Abas Ativas](#verificação-de-abas-ativas)
    + [VerificaAbaAtiva](#verificaabaativa)
- [Operações Numéricas Avançadas](#operações-numéricas-avançadas)
  * [Arredondamento e Truncamento](#arredondamento-e-truncamento)
    + [Arredondar](#arredondar)
    + [Truncar](#truncar)
  * [Operações Especiais](#operações-especiais)
    + [Dividir](#dividir)
    + [RestoDivisao](#restodivisao)
- [Interface e Feedback do Usuário](#interface-e-feedback-do-usuário)
  * [Barra de Progresso](#barra-de-progresso)
    + [IniciaBarraProgresso](#iniciabarraprogresso)
    + [AtualizaBarraProgresso](#atualizabarraprogresso)
    + [FinalizaBarraProgresso](#finalizabarraprogresso)
    + [OcultaBarraProgressoRelatorio](#ocultabarraprogressorelatorio)
  * [Controle de Interface](#controle-de-interface)
    + [ObterVersaoSistema](#obterversaosistema)
    + [ObtemIdiomaAtivo](#obtemidiomaativo)
    + [sleep](#sleep)
  * [Gerenciamento de Configuração](#gerenciamento-de-configuração)
    + [RetornaValorCFG](#retornavalorcfg)
- [Gerenciamento Avançado de Arquivos](#gerenciamento-avançado-de-arquivos)
  * [Criação e Exclusão de Arquivos Temporários](#criação-e-exclusão-de-arquivos-temporários)
    + [CriarArquivoTemporario](#criararquivotemporario)
    + [ExcluirArquivoTemporario](#excluirarquivotemporario)
    + [LinhasArquivo](#linhasarquivo)
  * [Execução de Programas Externos](#execução-de-programas-externos)
    + [ExecProg](#execprog)
  * [Abrir (Open)](#abrir-open)
  * [Ler (Read)](#ler-read)
  * [Lernl (ReadLn)](#lernl-readln)
  * [Gravar (Write)](#gravar-write)
  * [Gravarnl (WriteLn)](#gravarnl-writeln)
  * [Fechar (Close)](#fechar-close)
- [Mensagens](#mensagens)
- [Cancel](#cancel)
- [Padrões e Boas Práticas](#padrões-e-boas-práticas)
  * [Boas Práticas e Regras Gerais](#boas-práticas-e-regras-gerais)
  * [Declaração de Variáveis](#declaração-de-variáveis)
  * [Padrão de Nomenclatura de Variáveis](#padrão-de-nomenclatura-de-variáveis)
  * [Identação e Espaçamento](#identação-e-espaçamento-1)
  * [Estruturas de Bloco](#estruturas-de-bloco-1)
  * [Comentários](#comentários-1)
- [Controle de Fluxo](#controle-de-fluxo)
  * [Condicionais](#condicionais)
  * [Estrutura de Repetição](#estrutura-de-repetição)
  * [Pare](#pare)
  * [VaPara](#vapara)
  * [Recursividade](#recursividade)
- [Definição de Arrays](#definição-de-arrays)
  * [Declaração de Arrays](#declaração-de-arrays)
  * [Atribuição de Valores](#atribuição-de-valores)
  * [Acesso aos Valores](#acesso-aos-valores)
  * [Iteração sobre Arrays](#iteração-sobre-arrays)
  * [Exemplo Completo](#exemplo-completo)
- [Definição de Listas](#definição-de-listas)
  * [Comandos para Definição de Listas](#comandos-para-definição-de-listas)
  * [Acesso aos Campos](#acesso-aos-campos)
  * [Comandos para Manipulação de Registros](#comandos-para-manipulação-de-registros)
  * [Comandos para Posicionamento de Listas](#comandos-para-posicionamento-de-listas)
  * [Comandos para Procura de Registros](#comandos-para-procura-de-registros)
  * [Comandos para Posicionamento Absoluto](#comandos-para-posicionamento-absoluto)
  * [Comandos Diversos de Listas](#comandos-diversos-de-listas)
  * [Exemplo](#exemplo)
  * [Atribuição de Valores para a Lista](#atribuição-de-valores-para-a-lista)
  * [Utilização de Dados de uma Lista](#utilização-de-dados-de-uma-lista)
  * [Exclusão de Dados da Lista](#exclusão-de-dados-da-lista)
  * [Algoritmos de Leitura de Dados da Lista](#algoritmos-de-leitura-de-dados-da-lista)
    + [Utilizando o Retorno das Funções](#utilizando-o-retorno-das-funções)
    + [Utilizando Propriedade Indicadora de Fim de Arquivo (FDA)](#utilizando-propriedade-indicadora-de-fim-de-arquivo-fda)
    + [Utilizando Diretamente o Retorno das Funções de Movimentação](#utilizando-diretamente-o-retorno-das-funções-de-movimentação)
- [Definição de Tabelas](#definição-de-tabelas)
  * [Sintaxe](#sintaxe)
  * [Exemplo](#exemplo-1)
  * [Forma de Acesso à Variável](#forma-de-acesso-à-variável)
- [Definição de Cursor](#definição-de-cursor)
  * [Cursor Simples](#cursor-simples)
  * [Cursor Completo](#cursor-completo)
  * [Vantagens e Desvantagens dos Cursores](#vantagens-e-desvantagens-dos-cursores)
    + [Cursor Simples](#cursor-simples-1)
    + [Cursor Completo](#cursor-completo-1)
- [Definição de Funções](#definição-de-funções)
  * [Exemplos de Funções](#exemplos-de-funções)
    + [Função Simples](#função-simples)
    + [Função com Parâmetro Numérico](#função-com-parâmetro-numérico)
    + [Função com Parâmetro Numérico e Retorno no Mesmo Parâmetro](#função-com-parâmetro-numérico-e-retorno-no-mesmo-parâmetro)
    + [Função com Dois Parâmetros Numéricos e Retorno em uma Variável Específica](#função-com-dois-parâmetros-numéricos-e-retorno-em-uma-variável-específica)
  * [Organização das Funções](#organização-das-funções)
- [Retorno para Aplicação](#retorno-para-aplicação)
  * [ValRet](#valret)
  * [ValStr](#valstr)
- [Funções Gerais](#funções-gerais)
- [Funções SQL](#funções-sql)
  * [SQL Senior 2](#sql-senior-2)
    + [Ativação da Linguagem](#ativação-da-linguagem)
    + [Restrições](#restrições)
  * [Exemplos](#exemplos)
    + [Utilização de INSERT](#utilização-de-insert)
    + [Utilização de SELECT](#utilização-de-select)
    + [Utilização de UPDATE](#utilização-de-update)
  * [Passagem de Parâmetros](#passagem-de-parâmetros)
    + [Exemplo com `__inserir`](#exemplo-com-inserir)
    + [Exemplo com `SQL_Definir<tipo_variavel>`](#exemplo-com-sql_definirtipo_variavel)
- [Manipulação de Arquivos](#manipulação-de-arquivos)
- [Chamada de Web Service](#chamada-de-web-service)
  * [Modos de Execução](#modos-de-execução)
  * [WS-Security](#ws-security)
  * [Autenticação](#autenticação)
- [Chamada HTTP](#chamada-http)
  * [Visão Geral das Funções HTTP](#visão-geral-das-funções-http)
  * [Configuração Inicial](#configuração-inicial)
  * [HttpGet](#httpget)
  * [HttpPost](#httppost)
  * [HttpPut](#httpput)
  * [HttpDelete](#httpdelete)
  * [HttpDeleteBody](#httpdeletebody)
  * [HttpDownload](#httpdownload)
  * [HttpSetaTimeout](#httpsetatimeout)
  * [HttpPatch](#httppatch)
  * [HttpSetAttachment](#httpsetattachment)
  * [Base64Encode / Base64Decode](#base64encode--base64decode)
    + [Base64Encode](#base64encode-1)
    + [Base64Decode](#base64decode-1)
  * [Funções de Configuração Avançada](#funções-de-configuração-avançada)
    + [HttpAlteraCabecalhoRequisicao](#httpAlteracabecalhorequisicao)
    + [HttpAlteraCodifCaracPadrao](#httpAlteracodifcaracpadrao)
    + [HttpAlteraRedirecionamento](#httpAlteraredirecionamento)
  * [Funções de Gerenciamento de Cookies](#funções-de-gerenciamento-de-cookies)
    + [HttpHabilitarCookies / HttpDesabilitarCookies](#httphabilitarcookies--httpdesabilitarcookies)
  * [Funções de Leitura de Respostas](#funções-de-leitura-de-respostas)
    + [HttpLeCabecalhoResposta](#httplecabecalhoresposta)
    + [HttpNormalizaRetorno](#httpnormalizaretorno)
  * [Configuração de Proxy](#configuração-de-proxy)
    + [HttpAlteraConfiguracaoProxy](#httpAlteraconfiguracaoproxy)
    + [HttpLeConfiguracaoProxy](#httpleconfiguracaoproxy)
    + [HttpAlteraAutenticacaoProxy / HttpLeAutenticacaoProxy](#httpAlteraautenticacaoproxy--httpleautenticacaoproxy)
    + [Gerenciamento de Exceções de Proxy](#gerenciamento-de-exceções-de-proxy)
  * [Configuração SSL](#configuração-ssl)
    + [HttpAlteraConfiguracaoSSL / HttpLeConfiguracaoSSL](#httpAlteraconfiguracaossl--httpleconfiguracaossl)
  * [Configuração de Progresso de Download](#configuração-de-progresso-de-download)
    + [HttpAlteraMostrarProgresso / HttpLeMostrarProgresso](#httpAlteramostrarprogresso--httplemostrarprogresso)
  * [Configuração SNI (Server Name Indication)](#configuração-sni-server-name-indication)
    + [HttpHabilitaSNI / HttpDesabilitaSNI](#httphabilitasni--httpdesabilitasni)
  * [Funções Auxiliares Importantes](#funções-auxiliares-importantes)
  * [Exemplo Completo: Configuração Corporativa](#exemplo-completo-configuração-corporativa)
  * [Boas Práticas](#boas-práticas)
  * [Códigos de Status HTTP Comuns](#códigos-de-status-http-comuns)
  * [Observações Importantes](#observações-importantes)
  * [🚀 Exemplos Práticos de APIs](#-exemplos-práticos-de-apis)
    + [Exemplo 1: Busca CEP na API ViaCEP](#exemplo-1-busca-cep-na-api-viacep)
    + [Exemplo 2: Busca Cidade na API IBGE](#exemplo-2-busca-cidade-na-api-ibge)
    + [🔧 CRUD Básico - ReqRes API](#-crud-básico---reqres-api)
    + [🔐 Autenticação Basic Auth - HTTPBin](#-autenticação-basic-auth---httpbin)
    + [🎫 Autenticação Bearer Token - HTTPBin](#-autenticação-bearer-token---httpbin)
    + [🔑 Fluxo Completo: Login + Token + CRUD](#-fluxo-completo-login--token--crud)

## Introdução

A Linguagem Senior de Programação (LSP) é uma linguagem proprietária utilizada nos sistemas da Senior para a customização e extensão de funcionalidades. Ela permite a manipulação de dados, a criação de regras de negócio personalizadas e a automação de processos dentro do ambiente Senior.

Diferente de linguagens tradicionais como Java, C# ou Python, a LSP foi projetada especificamente para interagir com os sistemas Senior, possuindo sintaxe e estrutura próprias. Seu uso é essencial para desenvolvedores que desejam criar soluções personalizadas dentro da plataforma.

Nesta documentação, abordaremos a sintaxe, estrutura, operadores, controle de fluxo, manipulação de arquivos, chamadas de web service e outros aspectos da linguagem, sempre com exemplos práticos para facilitar a compreensão.

## Sintaxe e Estrutura

A linguagem LSP possui uma sintaxe própria, estruturada para facilitar a criação de regras de negócio dentro do ecossistema da Senior. Os comandos são escritos de forma sequencial e utilizam palavras-chave específicas para definir ações e estruturas de controle.

### Estrutura Básica

Cada comando na LSP deve ser finalizado com um ponto e vírgula (`;`). O código deve seguir uma ordem lógica para garantir a execução correta.

Exemplo de um código básico na LSP:

```lsp
Definir Numero vnX;
Definir Numero vnY;
Definir Numero vnResultado;
vnX = 10;
vnY = 20;
vnResultado = vnX + vnY;
Mensagem(Retorna, vnResultado);
```

### Case Sensitivity

A LSP **não** diferencia maiúsculas de minúsculas na declaração de variáveis. Isso significa que os seguintes exemplos são equivalentes:

```lsp
Definir Alfa vaNomeVariavel;
Definir Alfa VANOMEVARIAVEL;
```

### Identação e Espaçamento

A identação padrão na LSP é de **2 espaços** ao invés de 4. 

```lsp
Definir Numero vnX;
Definir Numero vnY;
Definir Numero vnSoma;
vnX = 5;
vnY = 15;

Se (vnX < vnY) { 
  vnSoma = vnX + vnY;
}
```

### Estruturas de Bloco

Regras:

   - Se o bloco contiver apenas uma linha, não é necessário informar `{ }` ou `inicio;` e `fim;`, basta adicionar identado na linha de baixo e identado.
   - Os blocos de código em LSP devem ser delimitados com `{ }`, ou alternativamente com `inicio;` e `fim;` (menos comum). 
   - Todas as condições ou estruturas de repetições devem estar entre parênteses `()`.

Exemplo de estrutura de bloco com apenas uma linha:

```lsp
Se (<Condição>) 
  vn = 1; @ Estrutura do bloco em uma linha @
```

Exemplo de estrutura de bloco com `{ }`:

```lsp
Se (<Condição>) {
  @ Estrutura do bloco @
}
```

Exemplo de estrutura de bloco com `inicio;` e `fim;`:

```lsp
Se (<Condição>) 
Inicio
  @ Estrutura do bloco @
Fim;
```

Exemplo de estrutura de bloco Incorreto:

```lsp
Se vnX < vnY {
  @ Estrutura do bloco @
}

@ OU @

Se vnX < vnY 
Inicio
  @ Estrutura do bloco @
Fim;
```

## Caracteres com Comportamento Especial

Existem determinados caracteres que, quando inseridos em uma expressão literal nas regras, devem ser precedidos do caractere `\` (barra) para indicar que estes caracteres serão usados literalmente e não como caracteres especiais. Estes caracteres são: `"` (aspas) e `\` (barra).

Exemplo:

```lsp
EnviaEMail("Joao","joao@senior.com.br", "", "", "Teste","\"\\\\Servidor\\teste.txt\"", "");
```

## Comentários

Comentários são utilizados para explicar o código e são ignorados pelo compilador. Existem três tipos de comentários na LSP:

- Comentário de uma linha: Utiliza o símbolo `@`.
- Comentário de múltiplas linhas: Inicia com `/*` e termina com `*/`.

Exemplo de comentário de uma linha:

```lsp
@ Este é um comentário de uma linha
Definir Numero vnX;
```

Exemplo de comentário de múltiplas linhas:

```lsp
/*
  Este é um comentário
  de múltiplas linhas
*/
Definir Numero vnX;
```

## Palavras Reservadas

A LSP não faz distinção de letras maiúsculas e minúsculas. Portanto, a LSP possui 51 (cinquenta e uma) palavras reservadas que não poderão ser usadas pelo programador para outros fins.

- Definir
- Se
- Senao
- Enquanto
- Para
- Funcao
- Fim
- Inicio
- Mensagem
- Cancel
- ValRet
- ValStr
- VaPara

| Comando | Descrição |
| --- | --- |
| Se (If) | Comando de comparação/pergunta, com resposta verdadeiro ou falso. |
| Senao (Else) | É a saída da pergunta (Se) quando a resposta for falsa. |
| e (And) | Liga duas ou mais condições, devendo todas serem verdadeiras para o resultado ser verdadeiro. |
| ou (Or) | Liga duas ou mais condições, bastando uma ser verdadeira para o resultado ser verdadeiro. |
| Inicio (Begin ou "{" - abre chaves) | Marcador utilizado para iniciar um bloco. |
| Fim; (End ou "}" - fecha chaves) | Marcador utilizado para finalizar um bloco. |
| Para (For) | Comando utilzado para se fazer um loop de comandos. Ou seja, fazer com que um bloco de comandos seja executado determinado número de vezes. Indica-se um \<valor inicial\> e esse valor é incrementado pelo valor do \<contador\> até que a \<condicao\> seja falsa. Sintaxe: Para (\<valor inicial\>; \<condicao\>; \<contador\>); |
| Enquanto (While) | Comando utilizado para se fazer um loop de comandos. Ou seja, fazer com que um bloco de comandos seja executado determinado número de vezes até que a \<condição>, seja falsa. Sintaxe: Enquanto (\<condicao\>); |
| Pare (Break) | Interrompe a execução de um bloco do comando Para ou Enquanto. O Pare, simplesmente faz com que o sistema abandone o bloco de comandos e continue a execução do restante das regras. Sintaxe: Pare;|
| Cancel (1) | Se for utilizado em uma regra do evento "Antes de Imprimir" de uma seção, cancela a impressão da seção. Se for usado no evento "Na Impressão" de um campo, cancela a impressão deste campo. Sintaxe: Cancel (1); |
| Cancel (2) | Deve ser usado em conjunto com as variáveis de sistema ValStr ou ValRet e somente no Evento "Na Impressão". O valor alfa atribuído para ValStr seguido de Cancel (2) será impresso no campo em que foi implementada a regra. Sintaxe: Cancel (2); |
| Cancel (3) | Utilizado apenas em controles do tipo fórmula (na ordenação por fórmula) para excluir o registro atual do relatório (semelhante a executar o Cancel(1) nas regras: Definição\Seleção, Detalhe\Antes_de_Imprimir e Detalhe\Depois_de_Imprimir) |
| Mensagem (Printf) | Exibe uma mensagem para o usuário durante a execução da regra. Sintaxe: Mensagem (\<tipo_da_mensagem\>,"\<mensagem\>"); |
| Vapara (Goto) | Desvia a execução da regra para o \<rótulo\> determinado. Sintaxe: Vapara \<rótulo\>; |
| Regra (Rule) | Chama uma outra regra, identificada pelo \<número da regra\>. Sintaxe: Regra (\<numero_da_regra\>); |
| Continue | Continua a execução de um loop feito pelo comando Para. Ou seja, se quiser que o loop não seja executado em determinado caso, faça o teste da condição e com ela use o comando. Sintaxe: Continue; |
| End (Var) | Usado na definição de uma função, para indicar qual parâmetro retornará valor. Sintaxe: Funcao Teste (end \<tipo do parâmetro\> \<nome do parâmetro\>); |
| Abrir (Open) |	Abre o \<arquivo informado\>, no \<modo de abertura\> desejado. Se o arquivo não existir ele é criado. Ele retorna um manipulador de arquivos. Sintaxe: Manipulador_de_Arquivo = Abrir (“\<nome_do_arquivo\>”,\<modo_de_abertura\>); Onde o Modo de Abertura pode ser: Ler ou Gravar. |
| Fechar (Close) |	Fecha o arquivo aberto pela função Abrir. Sintaxe: Fechar (\<manipulador_de_arquivo\>); |
| Ler (Read) |	Lê uma \<quantidade de caracteres\> do arquivo especificado no \<manipulador de arquivo\> e joga o valor lido em uma \<variável\>. Sintaxe: Ler (\<manipulador_de_arquivos\>, \<variavel\>,\<tamanho\>); |
| Gravar (Write) |	Grava o valor de uma \<variável ou de uma constante> no \<manipulador de arquivos\>. Sintaxe: Gravar (\<manipulador_de_arquivos\>,\<variável ou constante>,\<tamanho\>); |
| Lernl (ReadLn) |	Lê uma linha no arquivo indicado pelo \<manipulador de arquivos\> e joga o valor lido em uma \<variável\>. Sintaxe: Lernl (\<manipulador_de_arquivos\>,\<variável\>); |
| Gravarnl (WriteLn) |	Grava uma linha no arquivo indicado pelo \<manipulador de arquivos\> com o valor contido na variável especificada. Sintaxe: Gravarnl (\<manipulador_de_arquivos\>,\<variável ou constante\>); |
| Inserir (Include) |	Faz com que o sistema, insira um arquivo na regra atual, em tempo de execução/compilação. Sintaxe: Inserir "\<nome_arquivo\>"; ou Inserir "Header.lsp"; |
| ValStr |	Usado apenas no gerador, para alterar a descrição de um campo tipo Descrição. O texto passada para ValStr será impresso no lugar da descrição original do campo. ValStr = "Teste"; Cancel(2);	|
| Cursor |	Os cursores nada mais são que um SELECT em uma regra, retornando registros que satisfaçam a condição informada na propriedade SQL de um Cursor. Observações: O SELECT utilizado no cursor não possui relacionamento direto com o SELECT utilizado pelo gerador de relatórios, por exemplo. |

## Variáveis de Sistema

As variáveis de sistema são utilizadas para obter informações do ambiente de execução, como data, hora, usuário, entre outros. Abaixo estão algumas das principais variáveis de sistema disponíveis no Gerador de Relatórios:

| Variável       | Descrição                                                |
|----------------|----------------------------------------------------------|
| AnoSis         | Ano do sistema operacional                               |
| CodEmp         | Código da empresa                                        |
| CodFil         | Código da Filial                                         |
| CodUsu         | Código do usuário                                        |
| DatSis         | Data do sistema operacional                              |
| DBNomeUsuario  | Nome do usuário do banco de dados                        |
| DBTipo         | Banco de dados utilizado (ORACLE/SQLSERVER/POSTGRESQL/OUTRO) |
| DesRodape      | Descrição para rodapé                                    |
| DiaSis         | Dia do sistema operacional                               |
| Empresa        | Nome da empresa                                          |
| ExtSis         | Data por extenso do sistema operacional                  |
| Filial         | Nome da filial                                           |
| GerTabAlf      | Variável alfanumérica com 2000 ocorrências               |
| GerTabNum      | Variável numérica flutuante com 999 ocorrências          |
| HorSis         | Hora do sistema operacional                              |
| MesSis         | Mês do sistema operacional                               |
| NomUsu         | Nome do usuário                                          |
| NumPag         | Número da página                                         |
| QtdDupPag      | Quantidade de duplicatas impressas por página - Utilizado no modelo FRCR002 |

## Operadores

### Operadores Lógicos

Os operadores lógicos são utilizados para realizar comparações e operações lógicas. Os principais operadores lógicos são:

- `=`: Igual
- `<>`: Diferente
- `>`: Maior que
- `<`: Menor que
- `>=`: Maior ou igual a
- `<=`: Menor ou igual a
- `e`: E lógico
- `ou`: Ou lógico

### Operadores Aritméticos

Os operadores aritméticos são utilizados para realizar operações matemáticas. Os principais operadores aritméticos são:

- `+`: Adição
- `-`: Subtração
- `*`: Multiplicação
- `/`: Divisão
- `++`: Incremento de 1
- `--`: Decremento de 1

### Operadores Extras

Os operadores extras são utilizados para outras operações específicas. Alguns dos operadores extras são:

- `/*`: Início de comentário de múltiplas linhas
- `*/`: Fim de comentário de múltiplas linhas
- `@`: Comentário de uma linha

#### Observação sobre o operador %

O operador % (módulo) não existe na LSP. Para obter o resto da divisão, deve-se utilizar a função `RestoDivisao`.

Exemplo de uso da função RestoDivisao:
```lsp
Definir Numero vnDividendo;
Definir Numero vnDivisor;
Definir Numero vnResto;

vnDividendo = 1500;
vnDivisor = 400;

RestoDivisao(vnDividendo, vnDivisor, vnResto);
@ vnResto será 300 @
```

A função RestoDivisao retorna o resto da divisão de um número por outro. Os valores de entrada devem ser obrigatoriamente inteiros iguais ou maiores que 1. Por exemplo: ao informar 0.2, será considerado somente 0. Ao informar 1.1 será considerado 1.

Sintaxe: RestoDivisao(Dividendo, Divisor, Resto);

Parâmetros:
- Dividendo: Campo/Variável que será dividido
- Divisor: Campo/Variável pelo qual o Dividendo será dividido
- Resto: Variável que receberá o resto da divisão 

### Comportamentos Especiais

Existem determinados caracteres que, quando inseridos em uma expressão literal nas regras, devem ser precedidos do caractere `\` (barra) para indicar que estes caracteres serão usados literalmente e não como caracteres especiais. Estes caracteres são: `"` (aspas) e `\` (barra).

Exemplo:

```lsp
EnviaEMail("Joao","joao@senior.com.br", "", "", "Teste","\"\\\\Servidor\\teste.txt\"", "");
```

## Tipo de Dados e Variáveis

### Tipos de Dados

Os tipos de dados suportados pela LSP são:

- **Alfa**: Cadeia de caracteres.
- **Numero**: Números inteiros ou decimais.
- **Data**: Datas.
- **Lista**: Lista dinâmica nas regras.
- **Tabela**: Estrutura semelhante a um objeto em JavaScript.
- **Grid**: Estrutura de grade.
- **Cursor**: Estrutura para manipulação de consultas SQL.
- **Funcao**: Funções definidas pelo usuário.

### Declaração ou Definição de Variáveis

As variáveis na LSP são declaradas utilizando o comando `Definir`. O nome das variáveis deve ter no máximo 100 caracteres e pode conter `_` (sublinhado). Não é permitido usar acentuação no nome das variáveis. Caso a variável não seja definida, esta será considerada como tipo Numero.

Exemplo de declaração de variáveis:

Sintaxe

Definir <Tipo> <Nome_da_Variável>;

```lsp
Definir Alfa vaNome;
Definir Numero vnIdade;
Definir Data vdNascimento;
```

### Declaração ou Definição de Variáveis com Tamanho

Para variáveis do tipo `Alfa`, é possível definir o tamanho máximo da cadeia de caracteres.

Exemplo:

```lsp
Definir Alfa vaNome[30];
```

### Forma de Acesso

As variáveis são acessadas diretamente pelo seu nome.

Exemplo:

```lsp
vaNome = "João";
vnIdade = 25;
```

As variáveis com tamanhos(Arrays) são acessadas diretamente pelo seu índice.

   - O Índice pode conter um valor fixo, uma variável ou uma formula

<Nome_da_Variável>[<índice>] = <valor_atribuído>;

Exemplo:

```lsp
Definir Alfa vaNome[30];
Definir Numero vnIndice;

vnIndice = 1;

@ Valor Fixo @
vaNome[1] = "Nome";

@ Valor Variável @
vaNome[vnIndice] = "Nome";

@ Valor Formula @
vaNome[vnIndice + 1 * 2 ] = "Nome";
```

### Regras

- Variaveis do tipo Data deve-se usar a função MontaData(dd,mm,yyyy,vdData); para atribuir uma data ou atribuir a variável de sistema DatSis
- O nome das variáveis não pode ser igual ao nome dos parâmetros de funções. 
- O nome das variáveis não pode ser igual ao nome dos campos de listas.


## Manipulação Avançada de Strings

As funções de manipulação de strings na LSP permitem realizar operações complexas de processamento de texto, desde operações básicas até transformações avançadas e limpeza de dados.

### Conceitos Fundamentais

#### Concatenação de Strings

Na LSP, não é possível concatenar diretamente uma variável do tipo Numero com uma variável do tipo Alfa. Para realizar essa operação, é necessário:

1. Definir uma variável Alfa com o mesmo nome da variável numérica, mudando apenas o prefixo de `vn` para `va`
2. Utilizar a função `IntParaAlfa()` para converter o valor numérico em string

**Exemplo:**
```lsp
Definir Numero vnNumero;
Definir Alfa vaNumero;
Definir Alfa vaResultado;

vnNumero = 10;
IntParaAlfa(vnNumero, vaNumero);
vaResultado = "O número é " + vaNumero;
```

#### Quebra de Linha

Na LSP, não existe o caractere `\n` para quebra de linha. Para realizar a quebra de linha em uma string, deve-se:

1. Definir uma variável Alfa para armazenar o caractere de quebra de linha
2. Utilizar a função `CaracterParaAlfa(13, vaEnter)` para obter o caractere de quebra de linha (13 na tabela ASCII)
3. Concatenar essa variável na string onde se deseja a quebra de linha

**Exemplo:**
```lsp
Definir Alfa vaEnter;
Definir Alfa vaMensagem;

CaracterParaAlfa(13, vaEnter);
vaMensagem = "Primeira linha" + vaEnter + "Segunda linha";
``` 

### Funções Básicas de Manipulação

#### CopiarAlfa e CopiarStr

Copiam parte do conteúdo de uma variável/campo alfanumérico para outra variável alfanumérica.

**Sintaxe:**

```lsp
CopiarAlfa(<origem>, <destino>, <posicao>, <tamanho>);
CopiarStr(<origem>, <destino>, <posicao>, <tamanho>);
```

**Parâmetros:**
- `origem`: Texto de origem
- `destino`: Variável que receberá o texto copiado
- `posicao`: Posição inicial (baseada em 1)
- `tamanho`: Quantidade de caracteres a copiar

**Exemplo Prático:**

```lsp
Definir Alfa vaOrigem;
Definir Alfa vaNome;
Definir Alfa vaSobrenome;

vaOrigem = "João Silva Santos";
CopiarAlfa(vaOrigem, vaNome, 1, 4); @ vaNome será "João" @
CopiarAlfa(vaOrigem, vaSobrenome, 6, 5); @ vaSobrenome será "Silva" @
```

#### TamanhoAlfa e TamanhoStr

Retornam o tamanho de uma variável/campo alfanumérico.

**Sintaxe:**

```lsp
vnTamanho = TamanhoAlfa(<origem>);
vnTamanho = TamanhoStr(<origem>);
```

**Exemplo de Validação:**

```lsp
Definir Alfa vaSenha;
Definir Numero vnTamanho;
Definir Alfa vaMensagem;
Definir Alfa vaNumeroStr;

vaSenha = "minhasenha123";
vnTamanho = TamanhoAlfa(vaSenha);

Se (vnTamanho < 8) {
  vaMensagem = "Senha deve ter pelo menos 8 caracteres";
  Mensagem(Erro, vaMensagem);
} Senao {
  IntParaAlfa(vnTamanho, vaNumeroStr);
  vaMensagem = "Senha válida com " + vaNumeroStr + " caracteres";
  Mensagem(Retorna, vaMensagem);
}
```

#### PosicaoAlfa e PosicaoStr

Procuram por uma parte de texto dentro de um campo/variável, retornando a posição inicial.

**Sintaxe:**

```lsp
vnPosicao = PosicaoAlfa(<texto>, <subtexto>);
vnPosicao = PosicaoStr(<texto>, <subtexto>);
```

**Exemplo de Validação de Email:**

```lsp
Definir Alfa vaEmail;
Definir Numero vnPosArroba;
Definir Numero vnPosPonto;

vaEmail = "usuario@empresa.com.br";
vnPosArroba = PosicaoAlfa(vaEmail, "@");
vnPosPonto = PosicaoAlfa(vaEmail, ".");

Se (vnPosArroba = 0) {
  Mensagem(Erro, "Email inválido: falta @");
} Senao Se (vnPosPonto = 0) {
  Mensagem(Erro, "Email inválido: falta domínio");
} Senao {
  Mensagem(Retorna, "Email válido!");
}
```

#### SubstAlfa e SubstAlfaUmaVez

Substituem trechos específicos dentro de um texto por outro texto.

**Sintaxe:**

```lsp
SubstAlfa(<texto>, <subtexto>, <novoTexto>);      @ Substitui todas as ocorrências @
SubstAlfaUmaVez(<texto>, <subtexto>, <novoTexto>); @ Substitui apenas a primeira @
```

**Exemplo de Limpeza de Dados:**

```lsp
Definir Alfa vaTexto;
Definir Alfa vaTextoLimpo;

vaTexto = "João--Silva--Santos";
vaTextoLimpo = vaTexto;

@ Substitui todos os traços duplos por espaço simples @
SubstAlfa(vaTextoLimpo, "--", " ");
@ vaTextoLimpo será "João Silva Santos" @

@ Exemplo com SubstAlfaUmaVez @
vaTexto = "teste teste teste";
SubstAlfaUmaVez(vaTexto, "teste", "TESTE");
@ vaTexto será "TESTE teste teste" (apenas o primeiro) @
```

#### Concatenar

Concatena duas ou mais strings.

**Sintaxe:**

```lsp
vaResultado = Concatenar(<texto1>, <texto2>, ...);
```

**Exemplo:**

```lsp
Definir Alfa vaTexto1;
Definir Alfa vaTexto2;
Definir Alfa vaResultado;

vaTexto1 = "Exemplo";
vaTexto2 = " de string";
vaResultado = Concatenar(vaTexto1, vaTexto2); @ vaResultado será "Exemplo de string" @
```

### Funções Avançadas de Manipulação

#### DeletarAlfa

Remove uma quantidade específica de caracteres de uma posição determinada.

**Sintaxe:**

```lsp
DeletarAlfa(<texto>, <posicao>, <quantidade>);
```

**Exemplo de Formatação de CPF:**

```lsp
Definir Alfa vaCPF;

vaCPF = "123.456.789-10";

@ Remove formatação do CPF @
DeletarAlfa(vaCPF, 4, 1);  @ Remove primeiro ponto @
DeletarAlfa(vaCPF, 7, 1);  @ Remove segundo ponto @
DeletarAlfa(vaCPF, 10, 1); @ Remove traço @
@ vaCPF será "12345678910" @
```

#### ConverteParaMaiusculo e ConverteParaMinusculo

Convertem o conteúdo de uma variável para maiúsculo ou minúsculo.

**Sintaxe:**

```lsp
ConverteParaMaiusculo(<texto>);
ConverteParaMinusculo(<texto>);
```

**Exemplo de Padronização:**

```lsp
Definir Alfa vaNome;
Definir Alfa vaEmail;

vaNome = "joão SILVA santos";
vaEmail = "USUARIO@EMPRESA.COM.BR";

@ Padroniza email (tudo minúsculo) @
ConverteParaMinusculo(vaEmail);
@ vaEmail será "usuario@empresa.com.br" @

@ Para nome próprio @
ConverteParaMaiusculo(vaNome); @ Vira "JOÃO SILVA SANTOS" @
```

#### TrocaString

Função avançada de substituição com mais opções de controle.

**Sintaxe:**

```lsp
TrocaString(<texto>, <textoAntigo>, <textoNovo>);
```

**Exemplo de Template:**

```lsp
Definir Alfa vaTemplate;
Definir Alfa vaNomeUsuario;
Definir Alfa vaEmpresa;
Definir Alfa vaMensagemFinal;

vaTemplate = "Olá __NOME__, bem-vindo à __EMPRESA__!";
vaNomeUsuario = "João Silva";
vaEmpresa = "Senior Sistemas";

vaMensagemFinal = vaTemplate;
TrocaString(vaMensagemFinal, "__NOME__", vaNomeUsuario);
TrocaString(vaMensagemFinal, "__EMPRESA__", vaEmpresa);
@ vaMensagemFinal será "Olá João Silva, bem-vindo à Senior Sistemas!" @
```

#### LerPosicaoAlfa

Identifica qual caractere está em uma posição específica.

**Sintaxe:**

```lsp
LerPosicaoAlfa(<texto>, <posicao>, <caractere>);
```

**Exemplo de Validação:**

```lsp
Definir Alfa vaTexto;
Definir Alfa vaCaractere;
Definir Numero vnPosicao;
Definir Alfa vaPosicaoStr;

vaTexto = "ABC123XYZ";
vnPosicao = 4;

LerPosicaoAlfa(vaTexto, vnPosicao, vaCaractere);
@ vaCaractere será "1" @

@ Validação se é número @
Se ((vaCaractere >= "0") e (vaCaractere <= "9")) {
  IntParaAlfa(vnPosicao, vaPosicaoStr);
  Mensagem(Retorna, "Posição " + vaPosicaoStr + " é um número");
}
```

### Funções de Lista e Separação

#### ListaItem

Retorna um item específico de uma lista concatenada.

**Sintaxe:**

```lsp
ListaItem(<texto>, <separador>, <indice>, <item>);
```

**Exemplo de Processamento CSV:**

```lsp
Definir Alfa vaLinhaCsv;
Definir Alfa vaNome;
Definir Alfa vaIdade;
Definir Alfa vaCargo;

vaLinhaCsv = "João Silva;30;Desenvolvedor;São Paulo";

ListaItem(vaLinhaCsv, ";", 1, vaNome);    @ vaNome = "João Silva" @
ListaItem(vaLinhaCsv, ";", 2, vaIdade);   @ vaIdade = "30" @
ListaItem(vaLinhaCsv, ";", 3, vaCargo);   @ vaCargo = "Desenvolvedor" @
```

#### ListaQuantidade

Retorna a quantidade de itens em uma lista concatenada.

**Sintaxe:**

```lsp
vnQuantidade = ListaQuantidade(<texto>, <separador>);
```

**Exemplo de Contagem:**

```lsp
Definir Alfa vaEmails;
Definir Numero vnQuantidade;
Definir Alfa vaMensagem;
Definir Alfa vaQuantidadeStr;

vaEmails = "user1@teste.com,user2@teste.com,user3@teste.com";
vnQuantidade = ListaQuantidade(vaEmails, ",");

IntParaAlfa(vnQuantidade, vaQuantidadeStr);
vaMensagem = "Total de emails: " + vaQuantidadeStr;
Mensagem(Retorna, vaMensagem); @ "Total de emails: 3" @
```

### Funções de Codificação

#### ConverteCodificacaoString

Converte a codificação de um texto entre diferentes formatos.

**Sintaxe:**

```lsp
ConverteCodificacaoString(<textoOrigem>, <textoDestino>, <codificacaoOrigem>, <codificacaoDestino>);
```

**Exemplo de Conversão UTF-8:**

```lsp
Definir Alfa vaTextoWindows;
Definir Alfa vaTextoUTF8;

vaTextoWindows = "Acentuação especial";

@ Converte de windows-1252 para UTF-8 @
ConverteCodificacaoString(vaTextoWindows, vaTextoUTF8, "windows-1252", "utf-8");
```

#### ConverteTexto

Substitui caracteres especiais de acordo com a codificação especificada.

**Sintaxe:**

```lsp
ConverteTexto(<textoOrigem>, <textoDestino>, <tipoCodificacao>);
```

**Parâmetros de Codificação:**
- `1`: Remove acentos
- `2`: Converte para ASCII
- `3`: Normaliza caracteres especiais

**Exemplo de Normalização:**

```lsp
Definir Alfa vaTextoOriginal;
Definir Alfa vaTextoSemAcento;
Definir Alfa vaTextoASCII;

vaTextoOriginal = "João José da Conceição";

@ Remove acentos @
ConverteTexto(vaTextoOriginal, vaTextoSemAcento, 1);
@ vaTextoSemAcento será "Joao Jose da Conceicao" @

@ Converte para ASCII puro @
ConverteTexto(vaTextoOriginal, vaTextoASCII, 2);
@ Remove caracteres não-ASCII @
```

## Criptografia e Segurança

A LSP oferece um conjunto robusto de funções para operações criptográficas, geração de tokens seguros e proteção de dados sensíveis.

### Funções de Hash

#### GeraHash

Gera um hash criptográfico de um texto usando diferentes algoritmos.

**Sintaxe:**

```lsp
GeraHash(<texto>, <algoritmo>, <hash>);
```

**Algoritmos Suportados:**
- `1`: MD5 (128 bits)
- `2`: SHA-1 (160 bits)
- `3`: SHA-256 (256 bits)
- `4`: SHA-512 (512 bits)

**Exemplo de Verificação de Integridade:**

```lsp
Definir Alfa vaTextoOriginal;
Definir Alfa vaHashMD5;
Definir Alfa vaHashSHA256;
Definir Alfa vaMensagem;

vaTextoOriginal = "dados importantes do sistema";

@ Gera hash MD5 @
GeraHash(vaTextoOriginal, 1, vaHashMD5);

@ Gera hash SHA-256 (recomendado) @
GeraHash(vaTextoOriginal, 3, vaHashSHA256);

vaMensagem = "Hash SHA-256: " + vaHashSHA256;
Mensagem(Retorna, vaMensagem);
```

### Criptografia de Dados

#### Encriptar

Criptografa uma cadeia de caracteres usando algoritmo interno da Senior.

**Sintaxe:**

```lsp
Encriptar(<textoOriginal>, <textoCriptografado>);
```

#### Desencriptar

Descriptografa uma cadeia de caracteres previamente criptografada.

**Sintaxe:**

```lsp
Desencriptar(<textoCriptografado>, <textoOriginal>);
```

**Exemplo de Proteção de Dados:**

```lsp
Definir Funcao protegerDadosSensiveis();

@ Variáveis globais @
Definir Alfa vaDadosSensiveis;
Definir Alfa vaDadosCriptografados;
Definir Alfa vaDadosRecuperados;

vaDadosSensiveis = "CPF:12345678901;SENHA:minhasenha123";

protegerDadosSensiveis();

Funcao protegerDadosSensiveis(); {
  @ Criptografa dados @
  Encriptar(vaDadosSensiveis, vaDadosCriptografados);
  Mensagem(Retorna, "Dados criptografados: " + vaDadosCriptografados);

  @ Descriptografa para uso @
  Desencriptar(vaDadosCriptografados, vaDadosRecuperados);
  
  @ Verifica integridade @
  Se (vaDadosRecuperados = vaDadosSensiveis) {
    Mensagem(Retorna, "✅ Dados recuperados com sucesso!");
  } Senao {
    Mensagem(Erro, "❌ Erro na integridade dos dados!");
  }
}
```

### Geração de Tokens e Nonces

#### GerarNonce

Gera um valor Nonce (número aleatório usado uma única vez).

**Sintaxe:**

```lsp
GerarNonce(<nonce>);
```

#### GeraToken

Gera um token criptográfico seguro.

**Sintaxe:**

```lsp
GeraToken(<tamanho>, <token>);
```

#### GeraSenha

Gera uma senha aleatória com caracteres alfanuméricos.

**Sintaxe:**

```lsp
GeraSenha(<tamanho>, <senha>);
```

**Exemplo de Sistema de Autenticação:**

```lsp
Definir Funcao criarSessaoSegura();

@ Variáveis globais @
Definir Alfa vaUsuario;
Definir Alfa vaNonce;
Definir Alfa vaTokenSessao;
Definir Alfa vaSenhaTemporaria;
Definir Alfa vaChaveSeguranca;

vaUsuario = "joao.silva";

criarSessaoSegura();

Funcao criarSessaoSegura(); {
  @ 1. Gera nonce para a sessão @
  GerarNonce(vaNonce);

  @ 2. Gera token de sessão @
  GeraToken(32, vaTokenSessao);

  @ 3. Gera senha temporária @
  GeraSenha(12, vaSenhaTemporaria);

  @ 4. Cria chave de segurança combinada @
  vaChaveSeguranca = vaUsuario + ":" + vaNonce + ":" + vaTokenSessao;
  
  @ 5. Registra sessão @
  Mensagem(Retorna, "Sessão criada para: " + vaUsuario);
  Mensagem(Retorna, "Token: " + vaTokenSessao);
  Mensagem(Retorna, "Senha temporária: " + vaSenhaTemporaria);
}
```

### WS-Security e Digest

#### GerarPwdDigest

Gera o Digest da senha para autenticação WS-Security.

**Sintaxe:**

```lsp
GerarPwdDigest(<nonce>, <created>, <senha>, <digest>);
```

**Exemplo de Autenticação WS-Security:**

```lsp
Definir Funcao autenticacaoWSecurity();

@ Variáveis globais @
Definir Alfa vaNonce;
Definir Alfa vaCreated;
Definir Alfa vaSenha;
Definir Alfa vaDigest;
Definir Alfa vaXMLSecurity;

vaSenha = "minhasenhasecreta";

autenticacaoWSecurity();

Funcao autenticacaoWSecurity(); {
  @ 1. Gera nonce @
  GerarNonce(vaNonce);

  @ 2. Data/hora atual @
  DataHora(vaCreated);
  FormatarData(vaCreated, "yyyy-MM-ddTHH:mm:ssZ", vaCreated);

  @ 3. Gera digest @
  GerarPwdDigest(vaNonce, vaCreated, vaSenha, vaDigest);

  @ 4. Monta XML de segurança @
  vaXMLSecurity = "<wsse:Security>";
  vaXMLSecurity = vaXMLSecurity + "<wsse:UsernameToken>";
  vaXMLSecurity = vaXMLSecurity + "<wsse:Username>usuario</wsse:Username>";
  vaXMLSecurity = vaXMLSecurity + "<wsse:Password Type=\"PasswordDigest\">";
  vaXMLSecurity = vaXMLSecurity + vaDigest + "</wsse:Password>";
  vaXMLSecurity = vaXMLSecurity + "<wsse:Nonce>" + vaNonce + "</wsse:Nonce>";
  vaXMLSecurity = vaXMLSecurity + "<wsu:Created>" + vaCreated + "</wsu:Created>";
  vaXMLSecurity = vaXMLSecurity + "</wsse:UsernameToken>";
  vaXMLSecurity = vaXMLSecurity + "</wsse:Security>";

  Mensagem(Retorna, "XML WS-Security gerado com sucesso!");
}
```

### Codificação Base64

#### Base64Encode

Codifica uma string em Base64.

**Sintaxe:**

```lsp
Base64Encode(<textoOriginal>, <textoBase64>);
```

#### Base64Decode

Decodifica uma string Base64.

**Sintaxe:**

```lsp
Base64Decode(<textoBase64>, <textoOriginal>);
```

**Exemplo de Transmissão Segura:**

```lsp
Definir Funcao transmitirDadosSeguro();

@ Variáveis globais @
Definir Alfa vaDados;
Definir Alfa vaDadosCriptografados;
Definir Alfa vaDadosBase64;
Definir Alfa vaDadosRecebidos;
Definir Alfa vaDadosOriginais;

vaDados = "Informação confidencial da empresa";

transmitirDadosSeguro();

Funcao transmitirDadosSeguro(); {
  @ 1. Criptografa os dados @
  Encriptar(vaDados, vaDadosCriptografados);

  @ 2. Codifica em Base64 para transmissão @
  Base64Encode(vaDadosCriptografados, vaDadosBase64);
  Mensagem(Retorna, "Dados preparados para transmissão");

  @ Simulação de recebimento @
  @ 3. Decodifica Base64 @
  Base64Decode(vaDadosBase64, vaDadosRecebidos);

  @ 4. Descriptografa @
  Desencriptar(vaDadosRecebidos, vaDadosOriginais);

  @ 5. Verifica integridade @
  Se (vaDadosOriginais = vaDados) {
    Mensagem(Retorna, "✅ Transmissão segura concluída!");
  } Senao {
    Mensagem(Erro, "❌ Falha na integridade dos dados!");
  }
}
```

## Cast de Variável

As funções de cast de variável na LSP permitem converter valores entre diferentes tipos de dados.

### AlfaParaData

Converte um valor alfanumérico para o tipo Data.

**Sintaxe:**

```lsp
AlfaParaData(<texto>, <data>);
```

**Exemplo:**

```lsp
Definir Alfa vaTexto;
Definir Data vdData;

vaTexto = "01/01/2020";
AlfaParaData(vaTexto, vdData); @ vdData será 01/01/2020 @
```

### AlfaParaDecimal

Converte um valor alfanumérico para o tipo Decimal.

**Sintaxe:**

```lsp
AlfaParaDecimal(<texto>, <decimal>);
```

**Exemplo:**

```lsp
Definir Alfa vaTexto;
Definir Decimal vdDecimal;

vaTexto = "123.45";
AlfaParaDecimal(vaTexto, vdDecimal); @ vdDecimal será 123.45 @
```

### AlfaParaInt

Converte um valor alfanumérico para o tipo Inteiro.

**Sintaxe:**

```lsp
AlfaParaInt(<texto>, <inteiro>);
```

**Exemplo:**

```lsp
Definir Alfa vaTexto;
Definir Numero vnInteiro;

vaTexto = "123";
AlfaParaInt(vaTexto, vnInteiro); @ vnInteiro será 123 @
```

### IntParaAlfa

Converte um valor inteiro para o tipo Alfanumérico.

**Sintaxe:**

```lsp
IntParaAlfa(<inteiro>, <texto>);
```

**Exemplo:**

```lsp
Definir Numero vnInteiro;
Definir Alfa vaTexto;

vnInteiro = 123;
IntParaAlfa(vnInteiro, vaTexto); @ vaTexto será "123" @
```

### ConverteMascara

Converte um valor de entrada (numérico, data, hora ou cadeia de caracteres) para o tipo de dado cadeia de caracteres.

**Sintaxe:**

```lsp
ConverteMascara(<tipo>, <valor>, <texto>, <mascara>);
```

**Exemplo:**

```lsp
Definir Numero vnNumero;
Definir Alfa vaTexto;

vnNumero = 123456;
ConverteMascara(1, vnNumero, vaTexto, "999.999"); @ vaTexto será "123.456" @
```

## Manipulação Avançada de Datas

As funções de manipulação de datas na LSP permitem realizar operações complexas com datas, incluindo obtenção de datas atuais, cálculos de diferenças, formatação personalizada e validação.

### Funções de Data Atual

#### DataHoje

Obtém a data atual do sistema operacional (apenas data, sem hora).

**Sintaxe:**

```lsp
DataHoje(<data>);
```

#### DataHora

Obtém a data e hora atual do sistema operacional.

**Sintaxe:**

```lsp
DataHora(<dataHora>);
```

#### DataHoraUTC

Obtém a data e hora atual em UTC (Tempo Universal Coordenado).

**Sintaxe:**

```lsp
DataHoraUTC(<dataHoraUTC>);
```

**Exemplo Completo de Obtenção de Datas:**

```lsp
Definir Funcao obterDatasAtuais();

@ Variáveis globais @
Definir Data vdDataAtual;
Definir Data vdDataHoraAtual;
Definir Data vdDataHoraUTC;
Definir Alfa vaDataFormatada;
Definir Alfa vaHoraFormatada;
Definir Alfa vaUTCFormatada;

obterDatasAtuais();

Funcao obterDatasAtuais(); {
  @ 1. Obtém apenas a data @
  DataHoje(vdDataAtual);
  FormatarData(vdDataAtual, "dd/MM/yyyy", vaDataFormatada);
  
  @ 2. Obtém data e hora local @
  DataHora(vdDataHoraAtual);
  FormatarData(vdDataHoraAtual, "dd/MM/yyyy HH:mm:ss", vaHoraFormatada);
  
  @ 3. Obtém data e hora UTC @
  DataHoraUTC(vdDataHoraUTC);
  FormatarData(vdDataHoraUTC, "yyyy-MM-ddTHH:mm:ssZ", vaUTCFormatada);
  
  @ 4. Exibe resultados @
  Mensagem(Retorna, "Data atual: " + vaDataFormatada);
  Mensagem(Retorna, "Data/Hora local: " + vaHoraFormatada);
  Mensagem(Retorna, "Data/Hora UTC: " + vaUTCFormatada);
}
```

### Construção e Decomposição de Datas

#### CodData

Monta uma data a partir de dia, mês e ano.

**Sintaxe:**

```lsp
CodData(<dia>, <mes>, <ano>, <data>);
```

#### DecodData

Decompõe uma data em dia, mês e ano separadamente.

**Sintaxe:**

```lsp
DecodData(<data>, <dia>, <mes>, <ano>);
```

**Exemplo de Validação de Data:**

```lsp
Definir Funcao validarDataNascimento();

@ Variáveis globais @
Definir Numero vnDia;
Definir Numero vnMes;
Definir Numero vnAno;
Definir Data vdDataNascimento;
Definir Data vdDataAtual;
Definir Numero vnIdade;

vnDia = 15;
vnMes = 8;
vnAno = 1990;

validarDataNascimento();

Funcao validarDataNascimento(); {
  @ 1. Monta a data @
  CodData(vnDia, vnMes, vnAno, vdDataNascimento);
  
  @ 2. Obtém data atual para validação @
  DataHoje(vdDataAtual);
  
  @ 3. Verifica se a data é válida (não futura) @
  Se (vdDataNascimento > vdDataAtual) {
    Mensagem(Erro, "Data de nascimento não pode ser futura!");
  } Senao {
    @ 4. Calcula idade aproximada @
    vnIdade = vnAno - 2024; @ Simplificado para exemplo @
    Se (vnIdade < 0) {
      vnIdade = vnIdade * -1;
    }
    
    Mensagem(Retorna, "Data válida! Idade aproximada: " + IntParaAlfa(vnIdade));
  }
}
```

### Operações Aritméticas com Datas

#### AdicionarDias

Adiciona ou subtrai dias de uma data.

**Sintaxe:**

```lsp
AdicionarDias(<data>, <dias>, <novaData>);
```

**Exemplo de Cálculo de Prazos:**

```lsp
Definir Funcao calcularPrazos();

@ Variáveis globais @
Definir Data vdDataBase;
Definir Data vdDataVencimento;
Definir Data vdDataLimite;
Definir Alfa vaDataVencimentoStr;
Definir Alfa vaDataLimiteStr;

DataHoje(vdDataBase);

calcularPrazos();

Funcao calcularPrazos(); {
  @ Calcula vencimento (30 dias) @
  AdicionarDias(vdDataBase, 30, vdDataVencimento);
  FormatarData(vdDataVencimento, "dd/MM/yyyy", vaDataVencimentoStr);
  
  @ Calcula limite (60 dias) @
  AdicionarDias(vdDataBase, 60, vdDataLimite);
  FormatarData(vdDataLimite, "dd/MM/yyyy", vaDataLimiteStr);
  
  Mensagem(Retorna, "Vencimento: " + vaDataVencimentoStr);
  Mensagem(Retorna, "Limite: " + vaDataLimiteStr);
  
  @ Exemplo com subtração (data passada) @
  AdicionarDias(vdDataBase, -15, vdDataBase);
  FormatarData(vdDataBase, "dd/MM/yyyy", vaDataVencimentoStr);
  Mensagem(Retorna, "15 dias atrás: " + vaDataVencimentoStr);
}
```

### Formatação Avançada de Datas

#### FormatarData

Formata uma data usando máscaras personalizadas.

**Sintaxe:**

```lsp
FormatarData(<data>, <mascara>, <textoFormatado>);
```

**Máscaras Suportadas:**
- `dd`: Dia (01-31)
- `MM`: Mês (01-12)
- `yyyy`: Ano com 4 dígitos
- `yy`: Ano com 2 dígitos
- `HH`: Hora (00-23)
- `mm`: Minuto (00-59)
- `ss`: Segundo (00-59)

**Exemplo de Formatações Diversas:**

```lsp
Definir Funcao exemploFormatacoes();

@ Variáveis globais @
Definir Data vdDataHora;
Definir Alfa vaFormatoBR;
Definir Alfa vaFormatoUS;
Definir Alfa vaFormatoISO;
Definir Alfa vaFormatoCompleto;
Definir Alfa vaApenasHora;

DataHora(vdDataHora);

exemploFormatacoes();

Funcao exemploFormatacoes(); {
  @ Formato brasileiro @
  FormatarData(vdDataHora, "dd/MM/yyyy", vaFormatoBR);
  
  @ Formato americano @
  FormatarData(vdDataHora, "MM/dd/yyyy", vaFormatoUS);
  
  @ Formato ISO 8601 @
  FormatarData(vdDataHora, "yyyy-MM-dd", vaFormatoISO);
  
  @ Formato completo @
  FormatarData(vdDataHora, "dd/MM/yyyy HH:mm:ss", vaFormatoCompleto);
  
  @ Apenas hora @
  FormatarData(vdDataHora, "HH:mm", vaApenasHora);
  
  @ Exibe resultados @
  Mensagem(Retorna, "Brasileiro: " + vaFormatoBR);
  Mensagem(Retorna, "Americano: " + vaFormatoUS);
  Mensagem(Retorna, "ISO 8601: " + vaFormatoISO);
  Mensagem(Retorna, "Completo: " + vaFormatoCompleto);
  Mensagem(Retorna, "Hora: " + vaApenasHora);
}
```

### Validação e Comparação de Datas

**Exemplo de Sistema de Validação:**

```lsp
Definir Funcao validarPeriodo();

@ Variáveis globais @
Definir Data vdDataInicio;
Definir Data vdDataFim;
Definir Data vdDataAtual;
Definir Numero vnDiaInicio;
Definir Numero vnMesInicio;
Definir Numero vnAnoInicio;
Definir Numero vnDiaFim;
Definir Numero vnMesFim;
Definir Numero vnAnoFim;

@ Período de exemplo @
vnDiaInicio = 1;
vnMesInicio = 1;
vnAnoInicio = 2024;
vnDiaFim = 31;
vnMesFim = 12;
vnAnoFim = 2024;

validarPeriodo();

Funcao validarPeriodo(); {
  @ 1. Monta as datas @
  CodData(vnDiaInicio, vnMesInicio, vnAnoInicio, vdDataInicio);
  CodData(vnDiaFim, vnMesFim, vnAnoFim, vdDataFim);
  DataHoje(vdDataAtual);
  
  @ 2. Validações @
  Se (vdDataInicio > vdDataFim) {
    Mensagem(Erro, "Data inicial não pode ser maior que a final!");
  } Senao Se (vdDataFim < vdDataAtual) {
    Mensagem(Erro, "Período já expirado!");
  } Senao Se (vdDataInicio > vdDataAtual) {
    Mensagem(Retorna, "⏳ Período ainda não iniciado");
  } Senao Se ((vdDataAtual >= vdDataInicio) e (vdDataAtual <= vdDataFim)) {
    Mensagem(Retorna, "✅ Período ativo");
  } Senao {
    Mensagem(Retorna, "❌ Fora do período");
  }
}
```

## Validação e Verificação

A LSP oferece funções especializadas para validação de dados, verificação de abrangências e controle de qualidade de informações.

### Verificação de Abrangências

#### VrfAbrA

Verifica se um valor alfanumérico está dentro de uma abrangência especificada.

**Sintaxe:**

```lsp
VrfAbrA(<valor>, <abrangencia>);
```

#### VrfAbrN

Verifica se um valor numérico está dentro de uma abrangência especificada.

**Sintaxe:**

```lsp
VrfAbrN(<valor>, <abrangencia>);
```

**Exemplo de Validação de Códigos:**

```lsp
Definir Funcao validarCodigos();

@ Variáveis globais @
Definir Alfa vaCodigo;
Definir Numero vnNumero;
Definir Alfa vaAbrangenciaAlfa;
Definir Alfa vaAbrangenciaNum;
Definir Numero vnResultadoAlfa;
Definir Numero vnResultadoNum;

vaCodigo = "B";
vnNumero = 150;
vaAbrangenciaAlfa = "A..Z";
vaAbrangenciaNum = "100..200";

validarCodigos();

Funcao validarCodigos(); {
  @ Verifica abrangência alfanumérica @
  vnResultadoAlfa = VrfAbrA(vaCodigo, vaAbrangenciaAlfa);
  Se (vnResultadoAlfa = 1) {
    Mensagem(Retorna, "✅ Código '" + vaCodigo + "' válido na abrangência " + vaAbrangenciaAlfa);
  } Senao {
    Mensagem(Erro, "❌ Código '" + vaCodigo + "' fora da abrangência " + vaAbrangenciaAlfa);
  }
  
  @ Verifica abrangência numérica @
  vnResultadoNum = VrfAbrN(vnNumero, vaAbrangenciaNum);
  Se (vnResultadoNum = 1) {
    Mensagem(Retorna, "✅ Número " + IntParaAlfa(vnNumero) + " válido na abrangência " + vaAbrangenciaNum);
  } Senao {
    Mensagem(Erro, "❌ Número " + IntParaAlfa(vnNumero) + " fora da abrangência " + vaAbrangenciaNum);
  }
}
```

### Validação de Arquivos

#### ArqExiste

Verifica se um arquivo físico existe no local especificado.

**Sintaxe:**

```lsp
vnExiste = ArqExiste(<caminhoArquivo>);
```

**Exemplo de Verificação de Arquivos:**

```lsp
Definir Funcao verificarArquivos();

@ Variáveis globais @
Definir Alfa vaCaminhoArquivo;
Definir Alfa vaCaminhoConfig;
Definir Alfa vaCaminhoLog;
Definir Numero vnExisteArquivo;
Definir Numero vnExisteConfig;
Definir Numero vnExisteLog;

vaCaminhoArquivo = "C:\\temp\\dados.txt";
vaCaminhoConfig = "C:\\config\\app.ini";
vaCaminhoLog = "C:\\logs\\sistema.log";

verificarArquivos();

Funcao verificarArquivos(); {
  @ Verifica arquivo de dados @
  vnExisteArquivo = ArqExiste(vaCaminhoArquivo);
  Se (vnExisteArquivo = 1) {
    Mensagem(Retorna, "✅ Arquivo de dados encontrado");
  } Senao {
    Mensagem(Erro, "❌ Arquivo de dados não encontrado: " + vaCaminhoArquivo);
  }
  
  @ Verifica arquivo de configuração @
  vnExisteConfig = ArqExiste(vaCaminhoConfig);
  Se (vnExisteConfig = 1) {
    Mensagem(Retorna, "✅ Arquivo de configuração encontrado");
  } Senao {
    Mensagem(Retorna, "⚠️ Arquivo de configuração não encontrado, usando padrão");
  }
  
  @ Verifica arquivo de log @
  vnExisteLog = ArqExiste(vaCaminhoLog);
  Se (vnExisteLog = 0) {
    Mensagem(Retorna, "📝 Arquivo de log será criado: " + vaCaminhoLog);
  }
}
```

### Validação de Dados Estruturados

#### RemoveExpressoesProibidas

Remove ou valida expressões que podem representar scripts maliciosos.

**Sintaxe:**

```lsp
RemoveExpressoesProibidas(<textoOriginal>, <textoLimpo>);
```

**Exemplo de Limpeza de Dados:**

```lsp
Definir Funcao limparDadosEntrada();

@ Variáveis globais @
Definir Alfa vaDadosEntrada;
Definir Alfa vaDadosLimpos;
Definir Numero vnTamanhoOriginal;
Definir Numero vnTamanhoLimpo;

vaDadosEntrada = "Nome: João <script>alert('xss')</script> Silva";

limparDadosEntrada();

Funcao limparDadosEntrada(); {
  vnTamanhoOriginal = TamanhoAlfa(vaDadosEntrada);
  
  @ Remove expressões perigosas @
  RemoveExpressoesProibidas(vaDadosEntrada, vaDadosLimpos);
  
  vnTamanhoLimpo = TamanhoAlfa(vaDadosLimpos);
  
  Se (vnTamanhoOriginal <> vnTamanhoLimpo) {
    Mensagem(Retorna, "⚠️ Expressões perigosas removidas!");
    Mensagem(Retorna, "Original: " + vaDadosEntrada);
    Mensagem(Retorna, "Limpo: " + vaDadosLimpos);
  } Senao {
    Mensagem(Retorna, "✅ Dados seguros: " + vaDadosLimpos);
  }
}
```

### Verificação de Abas Ativas

#### VerificaAbaAtiva

Verifica se uma aba específica está ativa na interface.

**Sintaxe:**

```lsp
vnAtiva = VerificaAbaAtiva(<descricaoAba>);
```

**Exemplo de Controle de Interface:**

```lsp
Definir Funcao verificarContextoInterface();

@ Variáveis globais @
Definir Alfa vaAbaClientes;
Definir Alfa vaAbaProdutos;
Definir Numero vnAbaClientesAtiva;
Definir Numero vnAbaProdutosAtiva;

vaAbaClientes = "Clientes";
vaAbaProdutos = "Produtos";

verificarContextoInterface();

Funcao verificarContextoInterface(); {
  @ Verifica qual aba está ativa @
  vnAbaClientesAtiva = VerificaAbaAtiva(vaAbaClientes);
  vnAbaProdutosAtiva = VerificaAbaAtiva(vaAbaProdutos);
  
  Se (vnAbaClientesAtiva = 1) {
    Mensagem(Retorna, "🧑‍💼 Contexto: Gestão de Clientes");
    @ Lógica específica para clientes @
  } Senao Se (vnAbaProdutosAtiva = 1) {
    Mensagem(Retorna, "📦 Contexto: Gestão de Produtos");
    @ Lógica específica para produtos @
  } Senao {
    Mensagem(Retorna, "📋 Contexto: Genérico");
    @ Lógica geral @
  }
}
```

### Exemplo Prático: Sistema de Validação Completo

```lsp
Definir Funcao validacaoCompleta();

@ Variáveis globais @
Definir Alfa vaNomeArquivo;
Definir Alfa vaCodigo;
Definir Numero vnNumero;
Definir Data vdData;
Definir Numero vnValidacaoGeral;

vaNomeArquivo = "C:\\dados\\cliente.txt";
vaCodigo = "CLI001";
vnNumero = 1500;
DataHoje(vdData);

validacaoCompleta();

Funcao validacaoCompleta(); {
  vnValidacaoGeral = 1; @ Assume válido inicialmente @
  
  @ 1. Verifica arquivo @
  Se (ArqExiste(vaNomeArquivo) = 0) {
    Mensagem(Erro, "❌ Arquivo não encontrado: " + vaNomeArquivo);
    vnValidacaoGeral = 0;
  }
  
  @ 2. Verifica código na abrangência @
  Se (VrfAbrA(vaCodigo, "CLI001..CLI999") = 0) {
    Mensagem(Erro, "❌ Código fora da abrangência: " + vaCodigo);
    vnValidacaoGeral = 0;
  }
  
  @ 3. Verifica número na faixa @
  Se (VrfAbrN(vnNumero, "1000..2000") = 0) {
    Mensagem(Erro, "❌ Número fora da faixa: " + IntParaAlfa(vnNumero));
    vnValidacaoGeral = 0;
  }
  
  @ 4. Resultado final @
  Se (vnValidacaoGeral = 1) {
    Mensagem(Retorna, "✅ Todas as validações passaram!");
  } Senao {
    Mensagem(Erro, "❌ Falha na validação geral do sistema");
  }
}
```

## Operações Numéricas Avançadas

As funções numéricas na LSP permitem realizar operações matemáticas complexas, incluindo arredondamentos, divisões especiais e validações numéricas.

### Arredondamento e Truncamento

#### Arredondar

Arredonda um número para um número específico de casas decimais.

**Sintaxe:**

```lsp
Arredondar(<numero>, <casasDecimais>, <resultado>);
```

#### Truncar

Trunca um número para inteiro, removendo a parte fracionária.

**Sintaxe:**

```lsp
Truncar(<numero>, <resultado>);
```

**Exemplo de Cálculos Financeiros:**

```lsp
Definir Funcao calculosFinanceiros();

@ Variáveis globais @
Definir Numero vnValorOriginal;
Definir Numero vnValorArredondado;
Definir Numero vnValorTruncado;
Definir Numero vnPorcentagem;
Definir Numero vnDesconto;
Definir Numero vnValorFinal;

vnValorOriginal = 1234.6789;
vnPorcentagem = 15.5;

calculosFinanceiros();

Funcao calculosFinanceiros(); {
  @ Arredonda para 2 casas decimais (padrão monetário) @
  Arredondar(vnValorOriginal, 2, vnValorArredondado);
  Mensagem(Retorna, "Valor arredondado: R$ " + IntParaAlfa(vnValorArredondado));
  
  @ Trunca para inteiro @
  Truncar(vnValorOriginal, vnValorTruncado);
  Mensagem(Retorna, "Valor truncado: R$ " + IntParaAlfa(vnValorTruncado));
  
  @ Calcula desconto @
  vnDesconto = (vnValorOriginal * vnPorcentagem) / 100;
  Arredondar(vnDesconto, 2, vnDesconto);
  
  @ Valor final @
  vnValorFinal = vnValorOriginal - vnDesconto;
  Arredondar(vnValorFinal, 2, vnValorFinal);
  
  Mensagem(Retorna, "Desconto aplicado: R$ " + IntParaAlfa(vnDesconto));
  Mensagem(Retorna, "Valor final: R$ " + IntParaAlfa(vnValorFinal));
}
```

### Operações Especiais

#### Dividir

Realiza divisão com controle de erro para divisão por zero.

**Sintaxe:**

```lsp
Dividir(<dividendo>, <divisor>, <resultado>);
```

#### RestoDivisao

Calcula o resto da divisão (operação módulo).

**Sintaxe:**

```lsp
RestoDivisao(<dividendo>, <divisor>, <resto>);
```

**Exemplo de Validações Numéricas:**

```lsp
Definir Funcao validacoesNumericas();

@ Variáveis globais @
Definir Numero vnDividendo;
Definir Numero vnDivisor;
Definir Numero vnResultado;
Definir Numero vnResto;
Definir Numero vnNumero;

vnDividendo = 1500;
vnDivisor = 400;
vnNumero = 12345;

validacoesNumericas();

Funcao validacoesNumericas(); {
  @ Divisão segura @
  Se (vnDivisor <> 0) {
    Dividir(vnDividendo, vnDivisor, vnResultado);
    Mensagem(Retorna, "Divisão: " + IntParaAlfa(vnDividendo) + " ÷ " + IntParaAlfa(vnDivisor) + " = " + IntParaAlfa(vnResultado));
    
    @ Resto da divisão @
    RestoDivisao(vnDividendo, vnDivisor, vnResto);
    Mensagem(Retorna, "Resto: " + IntParaAlfa(vnResto));
  } Senao {
    Mensagem(Erro, "❌ Divisão por zero não permitida!");
  }
  
  @ Verificação de número par/ímpar @
  RestoDivisao(vnNumero, 2, vnResto);
  Se (vnResto = 0) {
    Mensagem(Retorna, "✅ " + IntParaAlfa(vnNumero) + " é par");
  } Senao {
    Mensagem(Retorna, "✅ " + IntParaAlfa(vnNumero) + " é ímpar");
  }
}
```

## Interface e Feedback do Usuário

A LSP oferece ferramentas para criar interfaces mais amigáveis e fornecer feedback visual durante operações demoradas.

### Barra de Progresso

#### IniciaBarraProgresso

Inicia uma barra de progresso para mostrar o andamento de processos longos.

**Sintaxe:**

```lsp
IniciaBarraProgresso(<titulo>, <mensagemInicial>);
```

#### AtualizaBarraProgresso

Atualiza o progresso e a mensagem da barra.

**Sintaxe:**

```lsp
AtualizaBarraProgresso(<percentual>, <mensagem>);
```

#### FinalizaBarraProgresso

Finaliza e fecha a barra de progresso.

**Sintaxe:**

```lsp
FinalizaBarraProgresso();
```

#### OcultaBarraProgressoRelatorio

Oculta a barra de progresso padrão durante a execução de relatórios.

**Sintaxe:**

```lsp
OcultaBarraProgressoRelatorio(<ocultar>);
```

**Exemplo de Processamento com Feedback:**

```lsp
Definir Funcao processarDadosComFeedback();

@ Variáveis globais @
Definir Numero vnTotalRegistros;
Definir Numero vnRegistroAtual;
Definir Numero vnPercentual;
Definir Alfa vaMensagem;
Definir Alfa vaRegistroStr;
Definir Alfa vaPercentualStr;

vnTotalRegistros = 100;

processarDadosComFeedback();

Funcao processarDadosComFeedback(); {
  @ Inicia barra de progresso @
  IniciaBarraProgresso("Processamento de Dados", "Iniciando processamento...");
  
  @ Simula processamento @
  Para (vnRegistroAtual = 1; vnRegistroAtual <= vnTotalRegistros; vnRegistroAtual++) {
    @ Calcula percentual @
    vnPercentual = (vnRegistroAtual * 100) / vnTotalRegistros;
    
    @ Monta mensagem @
    IntParaAlfa(vnRegistroAtual, vaRegistroStr);
    IntParaAlfa(vnPercentual, vaPercentualStr);
    vaMensagem = "Processando registro " + vaRegistroStr + " de " + IntParaAlfa(vnTotalRegistros);
    
    @ Atualiza barra @
    AtualizaBarraProgresso(vnPercentual, vaMensagem);
    
    @ Simula tempo de processamento @
    sleep(50); @ Pausa 50ms @
    
    @ Simula erro no meio do processo @
    Se (vnRegistroAtual = 50) {
      AtualizaBarraProgresso(50, "⚠️ Problema detectado, continuando...");
      sleep(1000); @ Pausa 1 segundo @
    }
  }
  
  @ Finaliza @
  AtualizaBarraProgresso(100, "✅ Processamento concluído!");
  sleep(1000);
  FinalizaBarraProgresso();
  
  Mensagem(Retorna, "Processamento de " + IntParaAlfa(vnTotalRegistros) + " registros concluído!");
}
```

### Controle de Interface

#### ObterVersaoSistema

Obtém a versão atual do sistema Senior.

**Sintaxe:**

```lsp
ObterVersaoSistema(<versao>);
```

#### ObtemIdiomaAtivo

Retorna o código do idioma utilizado pelo usuário.

**Sintaxe:**

```lsp
ObtemIdiomaAtivo(<codigoIdioma>);
```

#### sleep

Pausa a execução por um número especificado de milissegundos.

**Sintaxe:**

```lsp
sleep(<milissegundos>);
```

**Exemplo de Informações do Sistema:**

```lsp
Definir Funcao informacoesSistema();

@ Variáveis globais @
Definir Alfa vaVersaoSistema;
Definir Alfa vaIdiomaAtivo;
Definir Alfa vaInformacoes;

informacoesSistema();

Funcao informacoesSistema(); {
  @ Obtém versão do sistema @
  ObterVersaoSistema(vaVersaoSistema);
  
  @ Obtém idioma ativo @
  ObtemIdiomaAtivo(vaIdiomaAtivo);
  
  @ Monta informações @
  vaInformacoes = "=== INFORMAÇÕES DO SISTEMA ===" + CHR(13);
  vaInformacoes = vaInformacoes + "Versão: " + vaVersaoSistema + CHR(13);
  vaInformacoes = vaInformacoes + "Idioma: " + vaIdiomaAtivo + CHR(13);
  vaInformacoes = vaInformacoes + "Usuário: " + NomUsu + CHR(13);
  vaInformacoes = vaInformacoes + "Empresa: " + Empresa + CHR(13);
  vaInformacoes = vaInformacoes + "Data: " + ExtSis;
  
  Mensagem(Retorna, vaInformacoes);
}
```

### Gerenciamento de Configuração

#### RetornaValorCFG

Obtém valores da Central de Configuração Senior.

**Sintaxe:**

```lsp
RetornaValorCFG(<chave>, <valor>);
```

**Exemplo de Configuração Dinâmica:**

```lsp
Definir Funcao carregarConfiguracoes();

@ Variáveis globais @
Definir Alfa vaChaveTimeout;
Definir Alfa vaChaveDebug;
Definir Alfa vaValorTimeout;
Definir Alfa vaValorDebug;
Definir Numero vnTimeout;

vaChaveTimeout = "app.timeout.request";
vaChaveDebug = "app.debug.enabled";

carregarConfiguracoes();

Funcao carregarConfiguracoes(); {
  @ Carrega timeout da requisição @
  RetornaValorCFG(vaChaveTimeout, vaValorTimeout);
  Se (TamanhoAlfa(vaValorTimeout) > 0) {
    AlfaParaInt(vaValorTimeout, vnTimeout);
    Mensagem(Retorna, "⏱️ Timeout configurado: " + vaValorTimeout + "ms");
  } Senao {
    vnTimeout = 30000; @ Padrão: 30 segundos @
    Mensagem(Retorna, "⚠️ Timeout não configurado, usando padrão: 30000ms");
  }
  
  @ Carrega modo debug @
  RetornaValorCFG(vaChaveDebug, vaValorDebug);
  Se (vaValorDebug = "true") {
    Mensagem(Retorna, "🐛 Modo debug ativado");
  } Senao {
    Mensagem(Retorna, "🔒 Modo debug desativado");
  }
}
```

## Gerenciamento Avançado de Arquivos

Expansão das funcionalidades de manipulação de arquivos com recursos avançados.

### Criação e Exclusão de Arquivos Temporários

#### CriarArquivoTemporario

Cria um arquivo temporário com nome único.

**Sintaxe:**

```lsp
CriarArquivoTemporario(<prefixo>, <caminhoArquivo>);
```

#### ExcluirArquivoTemporario

Exclui um arquivo temporário criado anteriormente.

**Sintaxe:**

```lsp
ExcluirArquivoTemporario(<caminhoArquivo>);
```

#### LinhasArquivo

Conta o número de linhas em um arquivo.

**Sintaxe:**

```lsp
vnLinhas = LinhasArquivo(<caminhoArquivo>);
```

**Exemplo de Processamento de Arquivo Temporário:**

```lsp
Definir Funcao processarArquivoTemporario();

@ Variáveis globais @
Definir Alfa vaCaminhoTemp;
Definir Numero vnArquivo;
Definir Numero vnLinhas;
Definir Alfa vaConteudo;
Definir Numero vnContador;

processarArquivoTemporario();

Funcao processarArquivoTemporario(); {
  @ 1. Cria arquivo temporário @
  CriarArquivoTemporario("processamento_", vaCaminhoTemp);
  Mensagem(Retorna, "📄 Arquivo temporário criado: " + vaCaminhoTemp);
  
  @ 2. Escreve dados no arquivo @
  vnArquivo = Abrir(vaCaminhoTemp, Gravarnl);
  Para (vnContador = 1; vnContador <= 10; vnContador++) {
    vaConteudo = "Linha " + IntParaAlfa(vnContador) + " do arquivo temporário";
    Gravarnl(vnArquivo, vaConteudo);
  }
  Fechar(vnArquivo);
  
  @ 3. Verifica o arquivo criado @
  vnLinhas = LinhasArquivo(vaCaminhoTemp);
  Mensagem(Retorna, "📊 Arquivo criado com " + IntParaAlfa(vnLinhas) + " linhas");
  
  @ 4. Processa o arquivo @
  IniciaBarraProgresso("Processando Arquivo", "Lendo linhas...");
  vnArquivo = Abrir(vaCaminhoTemp, Lernl);
  
  Para (vnContador = 1; vnContador <= vnLinhas; vnContador++) {
    Lernl(vnArquivo, vaConteudo);
    AtualizaBarraProgresso((vnContador * 100) / vnLinhas, "Processando: " + vaConteudo);
    sleep(100); @ Simula processamento @
  }
  
  Fechar(vnArquivo);
  FinalizaBarraProgresso();
  
  @ 5. Remove arquivo temporário @
  ExcluirArquivoTemporario(vaCaminhoTemp);
  Mensagem(Retorna, "🗑️ Arquivo temporário removido");
}
```

### Execução de Programas Externos

#### ExecProg

Executa um programa externo a partir da regra LSP.

**Sintaxe:**

```lsp
ExecProg(<comando>, <parametros>, <aguardarTermino>);
```

**Exemplo de Integração com Ferramentas Externas:**

```lsp
Definir Funcao integracaoFerramentasExternas();

@ Variáveis globais @
Definir Alfa vaComando;
Definir Alfa vaParametros;
Definir Alfa vaCaminhoArquivo;

vaCaminhoArquivo = "C:\\temp\\relatorio.txt";

integracaoFerramentasExternas();

Funcao integracaoFerramentasExternas(); {
  @ 1. Abre arquivo no Bloco de Notas @
  vaComando = "notepad.exe";
  vaParametros = vaCaminhoArquivo;
  
  Se (ArqExiste(vaCaminhoArquivo) = 1) {
    ExecProg(vaComando, vaParametros, 0); @ Não aguarda terminar @
    Mensagem(Retorna, "📝 Arquivo aberto no Bloco de Notas");
  } Senao {
    Mensagem(Erro, "❌ Arquivo não encontrado: " + vaCaminhoArquivo);
  }
  
  @ 2. Abre explorador de arquivos @
  vaComando = "explorer.exe";
  vaParametros = "C:\\temp";
  ExecProg(vaComando, vaParametros, 0);
  Mensagem(Retorna, "📁 Explorador de arquivos aberto");
  
  @ 3. Executa comando do sistema @
  vaComando = "cmd.exe";
  vaParametros = "/c dir C:\\temp > C:\\temp\\listagem.txt";
  ExecProg(vaComando, vaParametros, 1); @ Aguarda terminar @
  Mensagem(Retorna, "⚙️ Listagem de arquivos gerada");
}
```

## Mensagens

A função `Mensagem` é utilizada para exibir mensagens ao usuário. Existem diferentes tipos de mensagens, como `Retorna`, `Erro`, e `Refaz`.

1. Não é possível fazer concatenação diretamente no parâmetro da função `Mensagem()`
2. É necessário definir uma variável Alfa antes, fazer as concatenações e atribuir nessa variável
3. A variável Alfa deve ser passada como parâmetro para a função `Mensagem()`

**Sintaxe**

- Mensagem(<tipo da mensagem>,"<mensagem>");

Exibe uma mensagem para o usuário. As mensagens possuem características de acordo com o seu tipo.

   - Retorna: Mostra uma mensagem de aviso, com os botões especificados entre colchetes. O símbolo & indica tecla de aceleração (atalho);
   - Erro: Gera uma exceção, mostrando uma mensagem de erro e abortando a execução da regra;
   - Refaz: Gera uma exceção, mostrando uma mensagem de erro e abortando a execução da regra.

- Exemplo comum, quando a mensagem é uma string literal sem concatenação:

```lsp
Mensagem(Retorna, "Operação concluída com sucesso!");
Mensagem(Erro, "Ocorreu um erro na operação.");
```

- Exemplo quando já temos uma variável Alfa com a mensagem final:

```lsp
Definir Alfa vaResultado;
vaResultado = "Mensagem já formatada";
Mensagem(Retorna, vaResultado);
```
- Exemplo quando precisamos fazer concatenação:

```lsp
Definir Alfa vaMensagem;
vaMensagem = "Aluno: " + vaNome + vaEnter + "Média: " + vaMedia;
Mensagem(Retorna, vaMensagem);
```

- Exemplo com botões especificados entre colchetes:

   - Entre colchetes podem conter 1 ou mais parâmetros, o retorno será de acordo com a sequencia do parâmetro, iniciando com 0

```lsp
Definir Numero vnRetorno;

vnRetorno = Mensagem(retorna,"Processo Concluído [&Ok!!!]"); @ O valor da variável vnRetorno será: 0 @

vnRetorno = Mensagem(retorna,"Deseja Sair ? [&Sim,&Não]"); @ O valor da variável vnRetorno será: 0 para Sim e 1 para Não @

vnRetorno = Mensagem(retorna,"Escolha uma opção ? [&Voltar,&Avançar, $Cancelar]"); @ O valor da variável vnRetorno será: 0 para Voltar, 1 para Avançar e 2 para Cancelar @

```

- Exemplo de uso incorreto:

```lsp
Mensagem(Retorna, "Aluno: " + vaNome + vaEnter + "Média: " + vaMedia); @ Erro: concatenação no parâmetro @
```

## Cancel

A função `Cancel` é utilizada para cancelar a execução de uma regra. Dependendo do valor passado como parâmetro, diferentes ações podem ser tomadas. Ao usar a função Cancel(n) em regras que são executadas por eventos de tela, a única ação tomada será o cancelamento da execução da regra, independentemente do valor passado como parâmetro.

Para que seja gerado um erro, deve-se usar a função **Mensagem(Erro, "mensagem")** ou então a equipe de desenvolvimento do sistema deve tratar via código de sistema o retorno de **Cancel(n)**.

No **Gerador de Relatórios**, o comando **Cancel** pode ser usado das seguintes formas:

   - **Cancel(1)**

     Em controles: Cancela a execução da regra e a impressão do mesmo.
     Nas regras: Definição\Seleção e Detalhe\Antes_de_Imprimir, exclui o registro atual do relatório (detalhe);
     Na regra: Definição\Pré-Seleção cancela a execução do relatório.

   - **Cancel(2)**
     Utilizado para imprimir o conteúdo da variável ValStr em controles do tipo descrição e depois sair da regra;

   - **Cancel(3)**
     Utilizado apenas em controles do tipo fórmula (na ordenação por fórmula) para excluir o registro atual do relatório (semelhante a executar o Cancel(1) nas regras: Definição\Seleção, Detalhe\Antes_de_Imprimir e Detalhe\Depois_de_Imprimir).

Exemplo:

```lsp
Cancel(1); @ Cancela a execução da regra e a impressão do controle @
Cancel(2); @ Imprime o conteúdo da variável ValStr em controles do tipo descrição e depois sai da regra @
Cancel(3); @ Exclui o registro atual do relatório em controles do tipo fórmula @
```

## Padrões e Boas Práticas

### Boas Práticas e Regras Gerais

- Sempre termine uma instrução de código com `;`.
- Evite duplicação de código, reutilize funções sempre que possível.
- Mantenha o código modularizado e organizado em funções.
- Utilize nomes descritivos para funções.
- Teste o código extensivamente para garantir que ele funcione corretamente em todas as situações esperadas.

### Declaração de Variáveis

- Declare as variáveis no início do código ou da função.
- Inicialize as variáveis sempre que possível no início do código ou da função.
- Em relatórios, declare e inicialize variáveis nos eventos de Inicialização ou Pré-Seleção.

### Padrão de Nomenclatura de Variáveis

- Utilize nomes descritivos para as variáveis.
- Utilize o padrão CamelCase nos nomes das variáveis.
- Utilize o padrão "v + inicial do tipo de dado" antes do nome da variável:
  - `va` para variáveis do tipo `Alfa`
  - `vn` para variáveis do tipo `Numero`
  - `vd` para variáveis do tipo `Data`
- Evite usar nomes de variáveis que possam ser confundidos com palavras reservadas ou nomes de funções.

### Identação e Espaçamento

- Utilize 2 espaços para identação.
- Mantenha o código organizado e legível, evitando linhas de código muito longas.

### Estruturas de Bloco

- Utilize `{` para abrir um bloco e `}` para fechar um bloco, delimitando assim os blocos de código.
- Se o bloco contiver apenas uma linha, não é necessário informar `{ }`, basta adicionar o código identado na linha de baixo.

Exemplo de estrutura de bloco com apenas uma linha:

```lsp
Se (<Condição>) 
  vn = 1; @ Estrutura do bloco em uma linha @
```

Exemplo de estrutura de bloco com `{ }`:

```lsp
Se (<Condição>) {
  @ Estrutura do bloco @
}
```

### Comentários

- Utilize comentários para explicar o código e facilitar a manutenção.
- Utilize `@` para comentários de uma linha e `/* */` para comentários de múltiplas linhas.

Exemplo de comentário de uma linha:

```lsp
@ Este é um comentário de uma linha @
Definir Numero vnX;
```

Exemplo de comentário de múltiplas linhas:

```lsp
/*
  Este é um comentário
  de múltiplas linhas
*/
Definir Numero vnX;
```

## Controle de Fluxo

### Condicionais

As estruturas condicionais são utilizadas para executar blocos de código com base em condições.

Exemplo de uso do `Se` e `Senao`:

```lsp
Definir Numero vnIdade;
vnIdade = 20;

Se (vnIdade >= 18) {
  Mensagem(Retorna, "Maior de idade");
} Senao {
  Mensagem(Retorna, "Menor de idade");
}
```

### Estrutura de Repetição

As estruturas de repetição são utilizadas para executar blocos de código repetidamente.

Exemplo de uso do `Enquanto`:

```lsp
Definir Numero vnContador;
vnContador = 0;

Enquanto (vnContador < 10) {
  Mensagem(Retorna, vnContador);
  vnContador++;
}
```

Exemplo de uso do `Para`:

```lsp
Para (i = 0; i < 10; i++) {
  Mensagem(Retorna, i);
}
```

### Pare

O comando `Pare` é utilizado para interromper a execução de um bloco de repetição.

Exemplo de uso do `Pare`:

```lsp
Para (vnContador = 0; vnContador < 10; vnContador++) {
  Se (vnContador = 5) {
    Pare;
  }
  Mensagem(Retorna, vnContador);
}
```

### VaPara

O comando `VaPara` é utilizado para desviar a execução do programa para um ponto específico da regra.

Exemplo de uso do `VaPara`:

```lsp
Definir Numero vnIdade;
vnIdade = 20;

Se (vnIdade < 18) {
  VaPara menorDeIdade;
}

Mensagem(Retorna, "Maior de idade");
VaPara fim;

menorDeIdade:
Mensagem(Retorna, "Menor de idade");

fim:
```

### Recursividade

A recursividade é uma técnica de programação onde uma função chama a si mesma para resolver um problema. Em LSP, a recursividade pode ser implementada seguindo alguns padrões específicos.

#### Estrutura Básica de uma Função Recursiva

Uma função recursiva em LSP geralmente possui:
1. Um ou mais casos base (condições de parada)
2. Um ou mais casos recursivos (chamadas à própria função)

Exemplo de implementação recursiva da sequência de Fibonacci:

```lsp
@ Função recursiva para calcular o n-ésimo termo da sequência de Fibonacci @
Funcao fibonacciRecursivo(Numero vnTermo, Numero vnAnterior, Numero vnAtual, Numero End vnResultado); {
  @ Caso base 1: primeiro termo @
  Se (vnTermo = 0) {
    vnResultado = vnAnterior;
  } 
  @ Caso base 2: segundo termo @
  Senao Se (vnTermo = 1) {
    vnResultado = vnAtual;
  } 
  @ Caso recursivo: termos subsequentes @
  Senao {
    fibonacciRecursivo(vnTermo - 1, vnAtual, vnAnterior + vnAtual, vnResultado);
  }
};
```

#### Características Importantes da Recursividade em LSP

1. **Parâmetros de Entrada e Saída**:
   - Use o parâmetro `End` para retornar valores
   - Passe os valores necessários para a próxima chamada recursiva

2. **Condições de Parada**:
   - Sempre defina casos base claros
   - Evite recursão infinita

3. **Chamada Recursiva**:
   - Modifique os parâmetros para se aproximar do caso base
   - Passe os valores atualizados para a próxima chamada

#### Boas Práticas

1. **Eficiência**:
   - Evite recálculos desnecessários
   - Considere usar parâmetros auxiliares para armazenar resultados intermediários

2. **Legibilidade**:
   - Comente claramente os casos base e recursivos
   - Use nomes descritivos para variáveis e parâmetros

3. **Limitações**:
   - Esteja ciente do limite da pilha de chamadas
   - Considere usar abordagens iterativas para problemas muito grandes

#### Exemplo Completo: Sequência de Fibonacci

```lsp
@ Exercício - Sequência de Fibonacci (versão recursiva) @
Definir Funcao fibonacciRecursivo(Numero vnTermo, Numero vnAnterior, Numero vnAtual, Numero End vnResultado);
Definir Funcao calcularFibonacci();

@ Função principal @
Definir Numero vnTermos;
Definir Alfa vaTermos;
Definir Alfa vaResultado;
Definir Numero vnContador;
Definir Alfa vaTermo;
Definir Numero vnTermoAtual;

vnTermos = 10; @ Número de termos da sequência @

@ Converter número para alfa @
IntParaAlfa(vnTermos, vaTermos);

@ Montar mensagem inicial @
vaResultado = "Sequência de Fibonacci com " + vaTermos + " termos: ";

calcularFibonacci();

@ Exibir sequência completa @
Mensagem(Retorna, vaResultado);

Funcao calcularFibonacci(); {
  @ Calcular e acumular todos os termos @
  Para (vnContador = 0; vnContador < vnTermos; vnContador++) {
    fibonacciRecursivo(vnContador, 0, 1, vnTermoAtual);
    IntParaAlfa(vnTermoAtual, vaTermo);
    Se (vnContador = 0) {
      vaResultado = vaResultado + vaTermo;
    } Senao {
      vaResultado = vaResultado + ", " + vaTermo;
    }
  }
};

Funcao fibonacciRecursivo(Numero vnTermo, Numero vnAnterior, Numero vnAtual, Numero End vnResultado); {
  Se (vnTermo = 0) {
    vnResultado = vnAnterior;
  } Senao Se (vnTermo = 1) {
    vnResultado = vnAtual;
  } Senao {
    fibonacciRecursivo(vnTermo - 1, vnAtual, vnAnterior + vnAtual, vnResultado);
  }
};
```

Este exemplo demonstra:
- Definição clara de casos base
- Passagem de parâmetros para a próxima chamada recursiva
- Uso do parâmetro `End` para retorno de valores
- Acumulação de resultados em uma string
- Formatação adequada da saída

## Definição de Arrays

Arrays são variáveis com tamanhos definidos que permitem armazenar múltiplos valores do mesmo tipo. Eles são úteis para armazenar coleções de dados de tamanho fixo.

### Declaração de Arrays

Para declarar um array, utilize o comando `Definir` seguido do tipo de dado, o nome da variável e o tamanho do array entre colchetes `[]`.

Exemplo de declaração de arrays:

```lsp
Definir Alfa vaNomes[10];
Definir Numero vnIdades[5];
Definir Data vdDatas[3];
```

### Atribuição de Valores

Os valores podem ser atribuídos aos elementos do array utilizando o índice do elemento entre colchetes `[]`.

Exemplo de atribuição de valores:

```lsp
vaNomes[0] = "João";
vaNomes[1] = "Maria";
vaNomes[2] = "Pedro";

vnIdades[0] = 25;
vnIdades[1] = 30;
vnIdades[2] = 35;

vdDatas[0] = "01/01/2020";
vdDatas[1] = "15/03/2021";
vdDatas[2] = "10/10/2022";
```

### Acesso aos Valores

Os valores dos elementos do array podem ser acessados utilizando o índice do elemento entre colchetes `[]`.

Exemplo de acesso aos valores:

```lsp
Mensagem(Retorna, vaNomes[0]); @ Exibe "João" @
Mensagem(Retorna, vnIdades[1]); @ Exibe 30 @
Mensagem(Retorna, vdDatas[2]); @ Exibe "10/10/2022" @
```

### Iteração sobre Arrays

Os arrays podem ser iterados utilizando estruturas de repetição como `Para` ou `Enquanto`.

Exemplo de iteração sobre arrays:

```lsp
Para (i = 0; i < 3; i++) {
  Mensagem(Retorna, vaNomes[i]);
}

Definir Numero j;
j = 0;
Enquanto (j < 3) {
  Mensagem(Retorna, vnIdades[j]);
  j++;
}
```

### Exemplo Completo

Aqui está um exemplo completo de declaração, atribuição, acesso e iteração sobre arrays:

```lsp
Definir Alfa vaNomes[3];
Definir Numero vnIdades[3];
Definir Data vdDatas[3];

vaNomes[0] = "João";
vaNomes[1] = "Maria";
vaNomes[2] = "Pedro";

vnIdades[0] = 25;
vnIdades[1] = 30;
vnIdades[2] = 35;

vdDatas[0] = "01/01/2020";
vdDatas[1] = "15/03/2021";
vdDatas[2] = "10/10/2022";

Para (i = 0; i < 3; i++) {
  Mensagem(Retorna, vaNomes[i]);
}

Definir Numero j;
j = 0;
Enquanto (j < 3) {
  Mensagem(Retorna, vnIdades[j]);
  j++;
}
```

## Definição de Listas

Sempre que é necessária a customização do sistema (mesmo que seja complexa), as regras podem ser usadas com a vantagem de não precisar recompilar o sistema. Ferramentas como Gerador de Relatórios, Importador e Exportador de Arquivos Texto, por exemplo, também permitem a customização através da regra.

O constante aumento de complexidade dos sistemas gerou a necessidade de mais recursos nas regras. Uma destas necessidades era uma lista dinamicamente alocada, flexível para programador/usuário e que fosse de fácil uso e entendimento.

Tendo conhecimento desta necessidade, foi implementado dentro das regras o recurso conhecido daqui por diante como Lista.

O funcionamento consiste em determinar os campos que a lista usará, preencher a lista com valores e usar estes valores de maneira que atenda às necessidades da lógica implementada pelo programador/usuário.

### Comandos para Definição de Listas

São comandos que determinam o formato da lista. Este formato hoje somente é determinado pelos campos que compõem a lista.

| Comando         | Função                                                                                       |
|-----------------|----------------------------------------------------------------------------------------------|
| tipo Lista      | Serve para determinar o tipo de uma variável que será lista. Nenhum parâmetro adicional será necessário para esta definição. |
| DefinirCampos   | Inicia a fase de adição de campos na lista. Somente podem ser adicionados campos durante este período, ou seja, após a chamada deste comando. |
| EfetivarCampos  | Determinará o fim da adição de campos e informará ao compilador/interpretador que a partir deste ponto a lista será usada efetivamente (receberá valores). Também permitirá ao interpretador criar estruturas internas de controle e manipulação desta lista. |
| AdicionarCampo  | Adiciona os campos. Nesta adição também deve ser informado o tipo e o tamanho se necessário. |

Sintaxe:

```lsp
funcao <lista>.AdicionarCampo(alfa NomeCampo, <tipo> TipoInterno, numero Tamanho);
```

Parâmetros:

- **NomeCampo**: Este parâmetro deve ser uma literal alfanumérica (constante). O nome do campo não deve conter espaços, acentos e nem número como primeiro caractere.
- **TipoInterno**: Deve ser um tipo primitivo interno da regra, ou seja, numero, alfa ou data.
- **Tamanho**: Parâmetro opcional que determina o tamanho do campo. Se informado, somente será aceito para campos alfanuméricos. Neste caso, o campo terá um tamanho limitado. Se não for informado, campos do tipo alfa não terão limite (podem ter valores até o limite de memória). Os outros tipos de campos não são afetados.

### Acesso aos Campos

O acesso aos campos que foram definidos dentro da lista deve ser feito digitando-se o nome da lista, seguido do ponto (.) e o nome do campo. Este nome deverá ser definido previamente através do comando AdicionarCampo.

Caso o nome digitado após o ponto não for um nome de procedimento, função, propriedade ou campo definido na lista, um erro de compilação será gerado.

### Comandos para Manipulação de Registros

Estes comandos permitem adicionar, inserir, gravar, excluir, etc. registros das listas para usar todo o potencial dinâmico do recurso.

| Comando  | Função                                                                                       |
|----------|----------------------------------------------------------------------------------------------|
| Adicionar| É o primeiro comando de manipulação de dados do recurso lista. Ele serve para adicionar valores (agrupados em registros) dentro da lista. Ele cria um registro no final dos registros existentes. Este somente respeitará a ordem de adição se não existirem chaves definidas (será visto mais tarde). |
| Inserir  | Tem a mesma função do comando Adicionar, mas ao invés de adicionar um registro no final dos registros existentes, insere-o na posição atual da lista (apontado internamente e acessível pela propriedade NumReg). |
| Editar   | Visa a atualização de registros. Para tal é necessário posicionar a lista no registro que se deseja alterar. Após isto chama-se o comando Editar e então muda-se os valores desejados. |
| Gravar   | Quando se altera os valores dos campos (após a chamada do comando Adicionar, Inserir ou Editar), pode-se efetivar os dados através do comando Gravar. Grava as informações dentro da lista para posterior recuperação. |
| Cancelar | Ao alterar os valores dos campos, mas por algum motivo os mesmos não devem ser efetivados, utilize o comando Cancelar. Os dados que estão sendo alterados ficam em um registro virtual que não é trabalhado até que seja chamado o comando Gravar ou Cancelar. No caso do comando Cancelar este registro virtual é descartado não alterando o conteúdo da lista. |
| Excluir  | Exclui um registro. Para tal é necessário posicionar a lista no registro que deverá ser excluído e então chamar o comando Excluir. Somente o registro atualmente posicionado será excluído. Para excluir mais registros é necessário chamar o comando mais vezes. |

### Comandos para Posicionamento de Listas

Estes comandos existem para que o programador/usuário possa posicionar o registro da lista e permitir uma maior agilidade no uso do recurso.

| Comando  | Função                                                                                       |
|----------|----------------------------------------------------------------------------------------------|
| Primeiro | Posiciona no primeiro registro que estiver na lista. Note que o primeiro registro pode ser o primeiro adicionado ou o primeiro que respeitar a chave que estiver atualmente selecionada. Exemplo: se existir um campo que for o nome do funcionário e a chave estiver configurada para este campo, o primeiro registro provavelmente será um nome que comece por A. O comando retorna 1 se a lista pôde ser posicionada no primeiro registro e 0 (zero) caso contrário. |
| Ultimo   | Posiciona a lista no último registro. Da mesma forma como o comando Primeiro, o último registro pode ser o último registro adicionado ou o registro que estiver obedecendo a chave. No exemplo anterior (nome do funcionário) o último registro poderia ser um nome que começasse com Z. O comando retorna 1 se a lista pôde ser posicionada no final e 0 (zero) caso contrário. |
| Anterior | O comando Anterior posiciona a lista no registro imediatamente anterior ao registro atual. Se não existir registro anterior, será posicionada em IDA. Segue a mesma lógica de chave do comando Primeiro e Ultimo. Se a lista pôde ser posicionada no registro anterior (que não é o IDA), o comando retorna 1, caso contrário retorna 0 (zero). |
| Próximo  | Posiciona a lista no registro imediatamente posterior ao registro atual. Se não existir registro posterior, será posicionada em FDA. A lógica de chave segue o padrão dos comandos de posicionamento anteriores. Retorna 1 se foi possível posicionar no próximo registro e 0 (zero) caso não tenha conseguido. |

### Comandos para Procura de Registros

Estes comandos auxiliam o programador/usuário na procura de registros dentro da lista através de valores previamente conhecidos.

| Comando    | Função                                                                                       |
|------------|----------------------------------------------------------------------------------------------|
| SetarChave | Coloca a lista em estado de edição de chave para que seja possível a manipulação dos valores da chave. Quando configurados estes valores será possível procurar os registros que possuem a chave informada. Isto será feito através do comando VaiParaChave que será visto a seguir. Apaga os valores que estiverem na chave no momento da chamada. Para manter os valores da chave use o comando EditarChave. |
| EditarChave| Tem o mesmo objetivo do comando SetarChave mas sem apagar os valores de chave. Quando este comando for chamado os valores que estiverem contidos na chave neste momento serão mantidos e ainda assim a lista entrará em modo de edição de chave. Serve para procurar por chaves muito parecidas sem que seja necessário informar todos os valores novamente. |
| VaiParaChave | Procura pelo registro que tiver a chave configurada naquele momento. Exemplo: Consideremos que a chave da lista seja o código de cadastro do funcionário e que o mesmo tenha o valor 10 após a chamada do comando SetarChave. Quando o comando VaiParaChave for chamado a lista será posicionada no primeiro registro onde o número do cadastro do funcionário for 10. Se o registro com esta característica não for encontrado, a lista não será reposicionada. Caso o comando encontre o registro procurado, será retornado 1. Caso contrário será retornado 0 (zero). |

### Comandos para Posicionamento Absoluto

Os comandos a seguir informam e configuram a posição absoluta da lista conforme o número do registro.

| Comando    | Função                                                                                       |
|------------|----------------------------------------------------------------------------------------------|
| NumReg     | Esta propriedade retorna o número do registro (baseado em zero) da posição atual da lista. Se a lista estiver posicionada no quarto registro, o valor retornado será 3. Este número de registro é influenciado pela chave que estiver ativa no momento da obtenção deste valor. Exemplo: Existe um registro na lista que não possui chave definida. O número deste registro é 2. Quando atribuímos uma chave para a lista, outro registro pode ter o número 2 e o registro que antes possuía o número 2 pode ter qualquer outro número, dependendo da chave aplicada. |
| SetaNumReg | Este procedimento tem como objetivo posicionar a lista de maneira absoluta. A posição da lista é a ordem do registro menos 1. A ordem do registro é influenciada pela chave que estiver ativa no momento da chamada. |

### Comandos Diversos de Listas

Os comandos a seguir são de categoria geral, mas são utilizados normalmente com os outros comandos aqui apresentados.

| Comando            | Função                                                                                       |
|--------------------|----------------------------------------------------------------------------------------------|
| Propriedade IDA    | Retorna 1 se a lista estiver em IDA (Início De Arquivo) e 0 (zero) caso contrário. |
| Propriedade FDA    | Retorna 1 se a lista estiver em FDA (Fim De Arquivo) e 0 (zero) caso contrário. |
| Propriedade QtdRegistros | Retorna o número de registros que estão retidos na lista naquele momento. |
| Limpar             | Apaga todos os registros da lista. |
| Procedimento Chave | Este procedimento configura a chave que a lista deverá usar do momento da chamada em diante. Esta chave deve conter os nomes dos campos que estiverem configurados na lista separados por ponto-e-vírgula (;). Caso não se queira chave nenhuma, deve-se configurar este valor com vazio (""). |

### Exemplo

Definição de uma lista:

```lsp
/* Definição das variáveis necessárias para a operação. */
definir lista Lst;

/* Definição de campos dentro da lista declarada acima. */
Lst.DefinirCampos();
Lst.AdicionarCampo("Empresa", numero);
Lst.AdicionarCampo("Tipo", alfa);
Lst.AdicionarCampo("Cadastro", numero);
Lst.AdicionarCampo("Nome", alfa, 100);
Lst.AdicionarCampo("Salario", numero);
Lst.AdicionarCampo("Afastamento", data);
Lst.EfetivarCampos();
```

O campo Nome será do tipo alfanumérico mas tem o seu tamanho limitado. Caso seja atribuído um valor cujo tamanho seja maior que 100, um erro em tempo de execução será mostrado ao usuário.

Neste exemplo são usados os comandos DefinirCampos, AdicionarCampo, EfetivarCampos, além da definição de uma variável do tipo Lista.

### Atribuição de Valores para a Lista

Neste exemplo a lista é preenchida com valores trazidos por um cursor.

```lsp
/* Definição de variáveis utilizadas na regra. */
definir cursor Cur;

/* Determinação da chave. Não influi na inserção de registros. */
Lst.Chave("Nome");

/* Preenchimento da lista com os valores do cursor. */
Cur.SQL "select NumEmp, TipCol, NumCad, NomFun, ValSal, DatAfa from R034FUN";
Cur.AbrirCursor();

enquanto (Cur.Achou) {
  Lst.Adicionar();
  Lst.Empresa = Cur.NumEmp;
  se (Cur.TipCol = 1)
    Lst.Tipo = "Colaborador";
  senao se (Cur.TipCol = 2)
    Lst.Tipo = "Parceiro";
  senao se (Cur.TipCol = 3)
    Lst.Tipo = "Terceiro";
  senao
    Lst.Tipo = "<desconhecido>";
  Lst.Cadastro = Cur.NumCad;
  Lst.Nome = Cur.NomFun;
  Lst.Salario = Cur.ValSal;
  Lst.Afastamento = Cur.DatAfa;
  Lst.Gravar();
  Cur.Proximo();
}
```

Neste exemplo são utilizados os comandos Adicionar, Gravar e Chave. Também são acessados os campos através do nome do mesmo.

### Utilização de Dados de uma Lista

Neste exemplo os dados previamente armazenados na lista estão sendo utilizados para a impressão de seções dentro do gerador de relatórios.

```lsp
definir alfa dsValorTipo;
definir alfa dsValorNome;
definir alfa dsValorEspecial2;
definir alfa dsValorEspecial4;

/* Retirar a chave para imprimir os registros na ordem de inserção. */
Lst.Chave("");
/* Obtém a quantidade de registros atualmente retidos na lista. */
frValorTotalReg = Lst.QtdRegistros;

/* Lista a seção dos dados */
ListaSecao("adCabecalho");

/* Navega por todos os registros da lista obtendo os valores dos campos. */
Tem = Lst.Primeiro();
enquanto (Tem = 1) {
  frValorNumReg = Lst.NumReg;
  frValorEmpresa = Lst.Empresa;
  dsValorTipo = Lst.Tipo;
  frValorCadastro = Lst.Cadastro;
  dsValorNome = Lst.Nome;
  frValorSalario = Lst.Salario;
  frValorAfastamento = Lst.Afastamento;
  ListaSecao("adDetalhe");
  Tem = Lst.Proximo();
}

/* Configura a chave do registro para poder proceder com uma procura. */
Lst.Chave("Cadastro;Nome");

/* Configura a chave para a procura do registro com Cadastro 10. */
Lst.SetarChave();
Lst.Cadastro = 10;
se (Lst.VaiParaChave()) {
  frValorEspecial6 = Lst.NumReg;
  frValorEspecial1 = Lst.Empresa;
  dsValorEspecial2 = Lst.Tipo;
  frValorEspecial3 = Lst.Cadastro;
  dsValorEspecial4 = Lst.Nome;
  frValorEspecial5 = Lst.Salario;
  frValorEspecial7 = Lst.Afastamento;
  ListaSecao("adValoresEspeciais");
}

/* Posiciona a lista absolutamente e imprime os dados do registro atual. */
Lst.SetaNumReg(5);
frValorEspecial6 = Lst.NumReg;
frValorEspecial1 = Lst.Empresa;
dsValorEspecial2 = Lst.Tipo;
frValorEspecial3 = Lst.Cadastro;
dsValorEspecial4 = Lst.Nome;
frValorEspecial5 = Lst.Salario;
frValorEspecial7 = Lst.Afastamento;
ListaSecao("adValoresEspeciais");
```

### Exclusão de Dados da Lista

Neste exemplo é mostrado como excluir dados da lista. Neste caso somente serão excluídos os registros cujo campo Salario estiver com um valor menor que 1000.

```lsp
Tem = Lst.Primeiro();
enquanto (Tem = 1) {
  se (Lst.Salario < 1000) {
    Lst.Excluir();
    se (Lst.FDA = 1)
      Tem = 0;
    senao
      Tem = 1;
  } senao
    Tem = Lst.Proximo();
}
```

### Algoritmos de Leitura de Dados da Lista

Para a leitura de dados é possível utilizar algumas lógicas. Basta o programador decidir qual a melhor para ele.

#### Utilizando o Retorno das Funções

Este algoritmo utiliza o retorno provido pelas funções de movimentação para identificar o estado da lista. É o mesmo algoritmo apresentado em exemplos anteriores.

```lsp
Tem = Lst.Primeiro();
enquanto (Tem = 1) {
  frValorNumReg = Lst.NumReg;
  frValorEmpresa = Lst.Empresa;
  dsValorTipo = Lst.Tipo;
  frValorCadastro = Lst.Cadastro;
  dsValorNome = Lst.Nome;
  frValorSalario = Lst.Salario;
  frValorAfastamento = Lst.Afastamento;
  ListaSecao("adDetalhe");
  Tem = Lst.Proximo();
}
```

#### Utilizando Propriedade Indicadora de Fim de Arquivo (FDA)

Este algoritmo utiliza-se da propriedade FDA para identificar o fim dos registros.

```lsp
Lst.Primeiro();
enquanto (Lst.FDA = 0) {
  frValorNumReg = Lst.NumReg;
  frValorEmpresa = Lst.Empresa;
  dsValorTipo = Lst.Tipo;
  frValorCadastro = Lst.Cadastro;
  dsValorNome = Lst.Nome;
  frValorSalario = Lst.Salario;
  frValorAfastamento = Lst.Afastamento;
  ListaSecao("adDetalhe");
  Lst.Proximo();
}
```

#### Utilizando Diretamente o Retorno das Funções de Movimentação

Este algoritmo não é usual mas pode ser utilizado. Consiste em colocar a lista no registro virtual IDA e identificar o fim de arquivo através do retorno da função Proximo diretamente. Neste caso o estado de fim de arquivo é obtido apenas uma vez quando da chamada da função Proximo.

```lsp
Lst.Primeiro();
Lst.Anterior();
enquanto (Lst.Proximo() = 1) {
  frValorNumReg = Lst.NumReg;
  frValorEmpresa = Lst.Empresa;
  dsValorTipo = Lst.Tipo;
  frValorCadastro = Lst.Cadastro;
  dsValorNome = Lst.Nome;
  frValorSalario = Lst.Salario;
  frValorAfastamento = Lst.Afastamento;
  ListaSecao("adDetalhe");
}
```

Da mesma forma, estes algoritmos podem ser utilizados começando pelo último registro e subindo até o primeiro. Para isto basta utilizar as funções Ultimo e Anterior.

## Definição de Tabelas

Usado com o comando definir para declarar uma variável do tipo Tabela, com linhas e colunas. Cada coluna é um nome com um tipo específico de informação e as linhas são indexadas de 1 até N.

### Sintaxe

```lsp
Definir Tabela <nome da tabela>[<número de ocorrências>] = { <tipo da variável> <nome da variável>; ... }
```

### Exemplo

Declaração de uma tabela de 12 ocorrências tendo como nome Acumulador, e como variáveis numéricas Media_Mensal e Movimento ocorrendo 31 vezes uma para cada dia do mês e a alfanumérica Nome_Mes com 14 posições:

```lsp
Definir Tabela Acumulador[12] = {
  Numero Media_Mensal;
  Numero Movimento[31];
  Alfa Nome_Mes[14];
};
```

Os caracteres `{` e `}` podem ser substituídos por `Inicio` e `Fim` respectivamente, indicando que as variáveis Media_Mensal e Movimento pertencem ao bloco "Tabela" ao qual tem nome de Acumulador.

### Forma de Acesso à Variável

```lsp
x1 = Acumulador[1].Media_Mensal + 1;
x1 = Acumulador[x2+1].Movimento[x3+1];
Acumulador[1].Nome_Mes = "Janeiro";
Acumulador[2].Nome_Mes = "Fevereiro";
```

Neste exemplo, estamos acessando e manipulando os dados da tabela Acumulador. Cada linha da tabela é indexada de 1 até N, e cada coluna tem um nome específico com um tipo de dado definido.

## Definição de Cursor

### Cursor Simples

Um cursor simples é utilizado para realizar consultas SQL e iterar sobre os resultados. Ele é definido utilizando o comando `Definir` seguido do tipo `Cursor`.

Exemplo de definição de um cursor simples:

```lsp
Definir Cursor curExemplo;
curExemplo.SQL = "SELECT * FROM Tabela";
curExemplo.AbrirCursor();

Enquanto (curExemplo.Achou) {
  Mensagem(Retorna, curExemplo.Campo);
  curExemplo.Proximo();
}

curExemplo.FecharCursor();
```

### Cursor Completo

Um cursor completo é utilizado para realizar consultas SQL mais complexas e iterar sobre os resultados. Ele é definido utilizando o comando `SQL_Criar` e outras funções SQL específicas.

Exemplo de definição de um cursor completo:

```lsp
Definir Alfa xCursor;
Definir Alfa vSql;
Definir Data xData;

vSql = "SELECT * FROM Tabela WHERE Condicao";

SQL_Criar(xCursor);
SQL_UsarSQLSenior2(xCursor, 0);
SQL_UsarAbrangencia(xCursor, 0);
SQL_DefinirComando(xCursor, vSql);
SQL_DefinirInteiro(xCursor, "xNumero", 1);
SQL_DefinirBoleano(xCursor, "xBoleano", 1);
SQL_DefinirFlutuante(xCursor, "xFlutuante", 1.6);
SQL_DefinirData(xCursor, "xData", xData);
SQL_DefinirAlfa(xCursor, "xAlfa", "João da Silva");

SQL_AbrirCursor(xCursor);
Enquanto (SQL_EOF(xCursor) = 0) {
  SQL_RetornarAlfa(xCursor, "CAMPO", variavelDestino);
  SQL_Proximo(xCursor);
}
SQL_FecharCursor(xCursor);
SQL_Destruir(xCursor);
```

### Vantagens e Desvantagens dos Cursores

#### Cursor Simples

**Vantagens:**
- Simplicidade na definição e uso.
- Menor quantidade de funções necessárias.
- Ideal para consultas simples e rápidas.

**Desvantagens:**
- Menos flexível para consultas complexas.
- Não suporta múltiplos parâmetros ou tipos de dados avançados.
- Não permite o uso de determinadas funções SQL.

#### Cursor Completo

**Vantagens:**
- Permite acesso a dados atualizados.
- Permite filtragem dos dados diretamente no banco de dados.
- Suporta operações complexas com múltiplos parâmetros.
- Pode utilizar ou não a sintaxe SQL Senior 2.

**Desvantagens:**
- A performance de resposta depende da rede e do banco de dados.
- Requer mais funções e configurações em comparação ao cursor simples.

## Definição de Funções

É um conjunto de comandos que tem como objetivo calcular um ou mais valores e retorná-los para uso na regra. Havendo uma operação que se repita, pode-se criar a função e chamá-la em cada regra, sem precisar reimplementá-la.

Nota:
Como boa prática, é recomendável que se reserve a regra 001 apenas para implementar funções.

Uma função pode receber parâmetros e retornar valores.

**⚠️ Importante:**
- Valores alterados dentro da função também serão alterados fora dela.
- **Os parâmetros definidos para as funções devem obrigatoriamente ser Numéricos**
- **Parâmetros do tipo Alfanuméricos (Alfa) NÃO são suportados por funções definidas nas regras**

**❌ Incorreto - NÃO funciona:**
```lsp
Funcao alterarNome(Alfa vaNome); {
   vaNome = "Nome Alterado"; @ ERRO: Parâmetro Alfa não suportado @
}
```

**✅ Correto - Usar variáveis globais:**
```lsp
Definir Alfa vaNome;

vaNome = "João Silva";

Funcao alterarNome(); {
  vaNome = "João da Silva"; @ Correto: variável global @
}
```

### Exemplos de Funções

#### Função Simples

```lsp
Definir Funcao funcaoSimples();

funcaoSimples();

Funcao funcaoSimples(); {  
  @ Corpo da Função @
}
```

#### Função com Parâmetro Numérico

```lsp
Definir Funcao adicionarHoras(Numero vnParametro);
Definir Numero vnHoras;

vnHoras = 2;
adicionarHoras(10);
@ o valor de vnHoras será 12 @

Funcao adicionarHoras(Numero vnParametro) {
  vnHoras = vnHoras + vnParametro;
}
```

#### Função com Parâmetro Numérico e Retorno no Mesmo Parâmetro

```lsp
Definir Funcao incrementar(Numero End vnParametro);
Definir Numero vnValor;

vnValor = 1;
incrementar(vnValor);
@ o valor de vnValor será 2 @

incrementar(vnValor);
@ o valor de vnValor será 3 @

incrementar(vnValor);
@ o valor de vnValor será 4 @

Funcao incrementar(Numero End vnParametro); {
  vnParametro = vnParametro + 1;
}
```

#### Função com Dois Parâmetros Numéricos e Retorno em uma Variável Específica

```lsp
Definir Funcao adicionarQuantidadeHoras(Numero vnHoraAtual, Numero vnQuantidade, Numero End vnRetorno);
Definir Numero vnHorario;
Definir Numero vnNovoHorario;

vnHorario = 2;
adicionarQuantidadeHoras(vnHorario, 2, vnNovoHorario);
@ o valor de vnNovoHorario será 4 @

Funcao adicionarQuantidadeHoras(Numero vnHoraAtual, Numero vnQuantidade, Numero End vnRetorno); {
  vnRetorno = vnHoraAtual + vnQuantidade;
}
```

### Organização das Funções

**⚠️ REGRA OBRIGATÓRIA:** Em LSP, as funções devem ser declaradas **SEMPRE APÓS** o código principal que as chama. A chamada da função deve aparecer ANTES da declaração da função no código.

**❌ Incorreto - NÃO funciona:**
```lsp
Funcao minhaFuncao(); {
  @ Corpo da função @
}

minhaFuncao(); @ ERRO: Chamada após declaração @
```

**✅ Correto - Ordem obrigatória:**
```lsp
@ 1. Variáveis globais @
@ 2. Código principal (chamadas) @
@ 3. Declaração das funções @
```

Para evitar problemas de execução, as funções devem sempre ficar no final do código. Aqui está um exemplo de como organizar o código corretamente:

```lsp
Definir Funcao funcaoSimples();
Definir Funcao adicionarHoras(Numero vnParametro);
Definir Funcao incrementar(Numero End vnParametro);
Definir Funcao adicionarQuantidadeHoras(Numero vnHoraAtual, Numero vnQuantidade, Numero End vnRetorno);

@ Execução da Função Simples @
funcaoSimples();

@ Execução da Função com Parâmetro Numérico @
Definir Numero vnHoras;
vnHoras = 2;
adicionarHoras(10); @ o valor de vnHoras será 12 @

@ Execução da Função com Parâmetro Numérico e Retorno no Mesmo Parâmetro @
Definir Numero vnValor;
vnValor = 1;
incrementar(vnValor);
@ o valor de vnValor será 2 @

incrementar(vnValor);
@ o valor de vnValor será 3 @

incrementar(vnValor);
@ o valor de vnValor será 4 @

@ Execução da Função com Dois Parâmetros Numéricos e Retorno em uma Variável Específica @
Definir Numero vnHorario;
Definir Numero vnNovoHorario;
vnHorario = 2;
adicionarQuantidadeHoras(vnHorario, 2, vnNovoHorario); @ o valor de vnNovoHorario será 4 @

@ ------------------------------------FUNÇÕES----------------------------------@

@ Função Simples @
Funcao funcaoSimples(); {  
  @ Corpo da Função @
}

@ Função com Parâmetro Numérico @
Funcao adicionarHoras(Numero vnParametro); { 
  vnHoras = vnHoras + vnParametro; 
}

@ Função com Parâmetro Numérico e Retorno no Mesmo Parâmetro @
Funcao incrementar(Numero End vnParametro); {  
  vnParametro = vnParametro + 1;
}

@ Função com Dois Parâmetros Numéricos e Retorno em uma Variável Específica @
Funcao adicionarQuantidadeHoras(Numero vnHoraAtual, Numero vnQuantidade, Numero End vnRetorno); {
  vnRetorno = vnHoraAtual + vnQuantidade;
}
```

## Retorno para Aplicação

Usado apenas no gerador de relatórios, para alterar o valor de um campo tipo Descrição ou Numérico. O valor passado para ValRet ou ValStr será impresso no lugar do valor original do campo. Essas palavras reservadas devem ser utilizadas em conjunto com o comando `Cancel(2);`.

### ValRet

A função `ValRet` é utilizada para retornar valores numéricos para a aplicação.

Exemplo de uso do `ValRet`:

```lsp
ValRet = 10;
Cancel(2);
```

### ValStr

A função `ValStr` é utilizada para retornar valores alfanuméricos para a aplicação.

Exemplo de uso do `ValStr`:

```lsp
ValStr = "Texto de Retorno";
Cancel(2);
```

## Funções Gerais

As funções gerais na LSP são utilizadas para realizar operações comuns, como manipulação de strings, datas e números.

| Nome                        | Descrição                                                                 |
|-----------------------------|---------------------------------------------------------------------------|
| AlfaParaInt                 | Converte um número armazenado como Alfa e o retorna como um tipo Número.  |
| ArqExiste                   | Verifica se um arquivo físico existe no local especificado.               |
| AtualizaBarraProgresso      | Atualiza as mensagens apresentadas na tela da barra de progresso.         |
| CaracterParaAlfa            | Converte um caracter (que fica armazenado pelo código ASCII) para o valor Alfanumérico correspondente. |
| CodData                     | Possibilita a composição de uma data, montando-a através de dia, mês e ano.|
| ConverteCodificacaoString   | Esta função converte a codificação de um texto para o formato definido pelo usuário. |
| ConverteMascara             | Esta função converte um valor de entrada (numérico, data, hora ou cadeia de caracteres), para o tipo de dado cadeia de caracteres. |
| ConverteParaMaiusculo       | Converte o conteúdo de uma variável do tipo Alfa para maiúsculo.          |
| ConverteParaMinusculo       | Converte o conteúdo de uma variável do tipo Alfa para minúsculo.          |
| ConverteTexto               | Substitui os caracteres especiais informados no texto de acordo com a codificação do padrão informada, retorna em uma nova variável o texto convertido. |
| CopiarAlfa                  | Esta função copia parte do conteúdo de uma variável/campo alfanumérico para a variável alfanumérica Retorno. |
| CriarArquivoTemporario      | Cria um arquivo temporário de nome aleatório e único prefixado com o valor do parâmetro prefixo. |
| DataHoje                    | Retorna a data atual do sistema operacional.                              |
| DataHora                    | Retorna data e hora atual.                                                |
| DecodData                   | Permite a separação de uma data em dia, mês e ano para que os dados possam ser usados separadamente. |
| DeletarAlfa                 | Esta função apaga uma determinada quantidade de caracteres de uma variável/campo a partir da posição informada. |
| Desencriptar                | Função para descriptografar uma cadeia de caracteres.                     |
| Dividir                     | Função disponível para dividir um valor por outro.                        |
| Encriptar                   | Criptografa a cadeia de caracteres.                                       |
| ExcluirArquivoTemporario    | Exclui um arquivo criado pela função CriarArquivoTemporario.              |
| ExecProg                    | Permite a execução de aplicativos durante a execução de regras.           |
| FormatarData                | Formata a data.                                                           |
| GeraHash                    | Retorna um Hash do texto informado.                                       |
| GerarNonce                  | Gera o valor do campo Nonce, um número aleatório.                         |
| GerarPwdDigest              | Gera o Digest da senha, a partir do Nonce, Data e senha, em formato base64.|
| GeraSenha                   | Retorna uma sequência de caracteres alfanuméricos aleatoriamente.         |
| GeraToken                   | Retorna um token criptografado.                                           |
| HoraParaMinuto              | Converte em minutos os valores que representam hora e minuto.             |
| IniciaBarraProgresso        | Inicia a barra de progresso utilizada para mostrar ao usuário o andamento de um processo mais extenso. |
| OcultaBarraProgressoRelatorio | Oculta a barra de progresso padrão durante a execução de relatórios.    |
| FinalizaBarraProgresso      | Finaliza a tela de barra de progresso.                                    |
| IntParaAlfa                 | Converte um número para formato alfanumérico, desprezando as casas decimais.|
| LerPosicaoAlfa              | Identifica qual caracter está em determinada posição do campo/variável de origem. |
| LinhasArquivo               | Leitura da quantidade de linhas existentes em um determinado arquivo.     |
| ListaItem                   | Retorna o valor de um item de uma lista de valores concatenados por um caracter separador. |
| ListaQuantidade             | Retorna a quantidade de itens de uma lista de valores concatenados por um caracter separador em um texto. |
| Mensagem                    | Apresenta a mensagem em tela de acordo com a parametrização do tipo de retorno e da mensagem que será visualizada. |
| ObtemIdiomaAtivo            | Retorna o código do idioma utilizado pelo usuário.                        |
| ObterVersaoSistema          | Esta função retorna a versão do sistema.                                  |

| PosicaoAlfa                 | Procura por uma parte de texto dentro de um campo/variável do tipo Alfa, retornando a posição em que o texto inicia. |
| RemoveExpressoesProibidas   | Não permite que campos de relatórios/regras aceitem algum tipo de script. |
| RestoDivisao                | Retorna o resto da divisão de um número por outro.                        |
| RetornaValorCFG             | Responsável por retornar para a regra o valor de uma determinada chave da Central de Configuração Senior que está sendo utilizada pelo sistema. |
| TamanhoAlfa                 | Verifica o tamanho do campo Alfa especificado em Origem.                  |
| TrocaString                 | Procura por um trecho específico dentro de um texto e o substitui, retornando um novo texto. |
| Truncar                     | Trunca um número para inteiro, removendo a parte fracionária do número.   |
| VerificaAbaAtiva            | Verifica, pela descrição passada por parâmetro, se essa é a descrição da aba ativa. |
| VrfAbrA                     | Verifica se um determinado valor está contido em uma abrangência especificada. |
| VrfAbrN                     | Verifica se um determinado valor numérico está contido em uma abrangência especificada. |
| sleep                       | Pausa a execução do código por X milesegundos |

Para mais detalhes sobre cada função, consulte a @documentação da Senior.

## Funções SQL

As funções a seguir podem ser utilizadas para manipulação de comandos SQL e o resultado dos comandos (cursores) em regras. A partir destas funções podem ser executados comandos DML (INSERT, UPDATE, DELETE) e também comandos SELECT que retornam cursores que poderão ser manipulados também.

| Nome                | Descrição                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------|
| SQL_AbrirCursor     | Função que abre o cursor (depois de informado o comando SQL a ser utilizado, que é definido na função SQL_DefinirComando). |
| SQL_BOF             | Função que retorna a informação se o cursor está na posição inicial (antes do primeiro registro: posição BOF). |
| SQL_Criar           | A partir de uma variável criada como alfa, é criado um cursor para trabalhar com informações da base de dados. |
| SQL_DefinirAlfa     | Função que define um valor do tipo alfa para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_DefinirBlob     | Função que define um valor do tipo alfa (que representa o arquivo blob) para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_DefinirBoleano  | Função que define um valor do tipo boolean (Número 1 para verdadeiro e 0 para falso) para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_DefinirComando  | Função que aplica o comando SQL para o cursor passado como parâmetro. |
| SQL_DefinirData     | Função que define um valor do tipo data ou date para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_DefinirFlutuante| Função que define um valor do tipo flutuante ou float (Fracionado Ex: 1,5) para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_DefinirInteiro  | Função que define um valor do tipo inteiro para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_Destruir        | Função que elimina um cursor e deve ser chamada quando o cursor não for mais utilizado. |
| SQL_EOF             | Função que retorna se o cursor está na posição final (depois do último registro chamada de posição EOF). |
| SQL_FecharCursor    | Função que fecha a pesquisa sendo feita pelo cursor. |
| SQL_Proximo         | Função que posiciona o cursor no próximo registro. |
| SQL_RetornarAlfa    | Função que retorna um valor alfa de um campo do registro do cursor. |
| SQL_RetornarBlob    | Função que retorna um valor alfa de um campo do registro do cursor. |
| SQL_RetornarBoleano | Função que retorna um número que representa um valor boolean, 1 para verdadeiro e 0 (zero) para falso, de um campo do tipo boolean do cursor. |
| SQL_RetornarData    | Função que retorna um valor do tipo data de um campo do registro do cursor. |
| SQL_RetornarFlutuante| Função que retorna um valor flutuante (fracionado, por exemplo 1,5) de um campo do registro do cursor. |
| SQL_RetornarInteiro | Função que retorna um valor inteiro de um campo do registro do cursor. |
| SQL_RetornarSeNulo  | Função que retorna se campo do registro do cursor é nulo. |
| SQL_UsarAbrangencia | Função que informa ao cursor se é para utilizar abrangência de usuários ou não. |
| SQL_UsarSQLSenior2  | Função que informa se o comando a ser definido para o cursor utiliza a sintaxe de linguagem Senior ou a sintaxe nativa (SQL Nativa: linguagem originada da base de dados utilizada, ex: Oracle, SQL server...etc). |


### SQL Senior 2

A linguagem Senior SQL 2 pode ser utilizada nas regras dos geradores de informação (gerador de relatórios e consultas), regras de cálculo (regras avulsas executadas diretamente pelo sistema) e importador/exportador de arquivos texto. Esta linguagem é um padrão adotado pela Senior para que os comandos SQL possam ser escritos em um formato padrão que permita um melhor aprendizado e uma melhor tradução para os bancos de dados suportados pelos sistemas da Senior.

#### Ativação da Linguagem

- **Gerador de Relatórios**: Menu principal do gerador > Diversos > Usar Senior SQL 2.
- **Importador/Exportador de Arquivos Texto**: Página Definições > Usar Senior SQL 2.
- **Gerador de Consultas**: Tela principal de definição de modelos > Senior SQL 2.
- **Regras**: Editor de regras > Compilar > Usar Senior SQL 2 ou Ctrl + F12.

#### Restrições

- **Funções de Agregação**: Funções como SUM, COUNT, MAX não podem ser usadas dentro da cláusula SELECT.
- **Comandos Nativos do Banco de Dados**: Comandos como TO_DATE ou CONVERT devem ser substituídos por comandos da linguagem Senior SQL 2.
- **JOIN e UNION**: Não têm garantias de funcionamento dentro das regras.

### Exemplos

#### Utilização de INSERT

```lsp
Definir Alfa xCursor;
Definir Alfa xBlob;

SQL_Criar(xCursor);

@ Insere um novo registro na tabela de intervalos. @
SQL_DefinirComando(xCursor, "INSERT INTO R006INT VALUES (9999, 'Exemplo de intervalo')");
SQL_AbrirCursor(xCursor);

/* Todas as operações referentes à base de dados
   serão feitas entre abrirCursor e fecharCursor. */

SQL_FecharCursor(xCursor);
SQL_Destruir(xCursor);
```

#### Utilização de SELECT

```lsp
Definir Alfa xCursor;

@ Cria o cursor. @
SQL_Criar(xCursor);

@ Define um comando para poder carregar as informações no Cursor. @
SQL_DefinirComando(xCursor, "SELECT R034FUN.CODFIL FROM R034FUN WHERE R034FUN.CODFIL = 1");

@ Abre o cursor para utilização. @
SQL_AbrirCursor(xCursor);

/* Todas as operações referentes à base de dados
   serão feitas entre abrirCursor e fecharCursor. */

@ Fecha o cursor depois de utilizar. @
SQL_FecharCursor(xCursor);
SQL_Destruir(xCursor);
```

#### Utilização de UPDATE

```lsp
Definir Alfa xCursor;
Definir Alfa xBlob;

SQL_Criar(xCursor);

@ Atualiza as informações na base de dados através do comando UPDATE. @
SQL_DefinirComando(xCursor, "UPDATE R034FOT SET FOTEMP = :xBlob WHERE NUMEMP = 9999");

@ Abre o arquivo para a leitura (Indicado pelo 2º parâmetro). @
xArquivo = Abrir("C:/Teste.jpg", Ler);

@ Lê o arquivo que foi aberto acima, e o atribui à variável xBlob (em binário). @
Ler(xArquivo, xBlob, 9999999);

SQL_DefinirBlob(xCursor, "xBlob", xBlob);
SQL_AbrirCursor(xCursor);

/* Todas as operações referentes à base de dados
   serão feitas entre abrirCursor e fecharCursor. */

SQL_FecharCursor(xCursor);
SQL_Destruir(xCursor);
```

### Passagem de Parâmetros

A passagem de parâmetros para dentro de um cursor pode ser feita utilizando `__inserir` ou `SQL_Definir<tipo_variavel>` e passando com `:` para dentro da query, em vez de concatenar um valor na Query.

O `:` é utilizado para indicar que se trata de um parâmetro que será substituído por um valor específico antes da execução do comando SQL. Isso é comum em consultas parametrizadas para evitar a concatenação direta de valores nas strings SQL, o que pode ajudar a prevenir injeções de SQL, melhorar a legibilidade e manutenção do código, pois não é necessário converter variáveis para alfa para concatenar na query. O ideal é sempre utilizar passagem de parâmetro e evitar concatenar variáveis na query.

#### Exemplo com `__inserir`

```lsp
Definir Cursor C;
Definir Numero vnCodEmp;
Definir Numero vnCodFil;
Definir Alfa vaOrderBy;

vnCodEmp = 1;
vnCodFil = 6;
vaOrderBy = "ORDER BY CODFIL";

C.SQL "SELECT NumEmp, TipCol, NumCad, NomFun, ValSal FROM R034FUN WHERE CodEmp = __inserir(:vnCodEmp) and CodFil = __inserir(:vnCodFil) __inserir(:vaOrderBy)";

C.AbrirCursor();
se (C.Achou) {
  // ...existing code...
}
C.FecharCursor();
```

#### Exemplo com `SQL_Definir<tipo_variavel>`

```lsp
Definir Alfa xCursor;
Definir Numero xNumero;

SQL_Criar(xCursor);
SQL_DefinirComando(xCursor, "SELECT * FROM Tabela WHERE Campo = :xNumero");
SQL_DefinirInteiro(xCursor, "xNumero", 123);

SQL_AbrirCursor(xCursor);
Enquanto (SQL_EOF(xCursor) = 0) {
  SQL_Proximo(xCursor);
}
SQL_FecharCursor(xCursor);
SQL_Destruir(xCursor);
```

## Manipulação de Arquivos

A LSP permite a manipulação de arquivos utilizando comandos específicos para abrir, ler, gravar e fechar arquivos.

### Abrir (Open)

Abre o arquivo informado em nome do arquivo para o modo de abertura informado (Ler/Gravar). Se o arquivo não existir, ele é criado. Ele retorna um manipulador de arquivos.

**Sintaxe:**

```lsp
Abrir ("<nome do arquivo>",<modo de abertura>);
```

**Exemplo:**

```lsp
arq = Abrir("Teste.txt", Ler);
```

### Ler (Read)

Lê uma quantidade de caracteres especificados em tamanho do arquivo especificado no manipulador de arquivo e joga o valor lido na variável especificada.

**Sintaxe:**

```lsp
Ler(<manipulador de arquivo>,<variável>,<tamanho>);
```

**Exemplo:**

```lsp
Ler(arq, S, 20);
```

### Lernl (ReadLn)

Lê uma linha do arquivo indicado pelo manipulador de arquivo e joga o valor lido para a variável indicada.

**Sintaxe:**

```lsp
Lernl(<manipulador de arquivo>,<variável>);
```

**Exemplo:**

```lsp
Lernl(arq, S);
```

### Gravar (Write)

Grava o valor de uma constante ou de uma variável, e uma quantidade de caracteres especificados em tamanho no arquivo especificado no manipulador de arquivo.

**Sintaxe:**

```lsp
Gravar(<manipulador de arquivo>,<<variável> ou <constante>>,<tamanho>);
```

**Exemplo:**

```lsp
Gravar(arq, S, 20);
```

### Gravarnl (WriteLn)

Grava uma linha no arquivo indicado pelo manipulador de arquivo com o valor de uma variável ou constante, passada como parâmetro.

**Sintaxe:**

```lsp
Gravarnl(<manipulador de arquivo>,<<variável> ou <constante>>);
```

**Exemplo:**

```lsp
Gravarnl(arq, Str);
```

### Fechar (Close)

Fecha um arquivo aberto anteriormente pelo comando Abrir.

**Sintaxe:**

```lsp
Fechar (<manipulador do arquivo>);
```

**Exemplo:**

```lsp
Fechar(arq);
```

## Chamada de Web Service

O Editor de Regras dispõe de um conjunto de funções para que seja possível a atribuição e manipulação dos parâmetros de um web service, bem como a sua execução. Para isto é necessário declarar uma variável identificando o serviço que se deseja executar.

**Sintaxe:**

```lsp
@ Definir idProvedor.idServico.idPorta VarName; @

Definir interno.com.senior.g5.rh.fp.calculoFolha.Calcular vCalcula;
```

A variável informada é a que será utilizada para acessar os parâmetros, funções da porta, ler, fazer atribuições e comparações com os parâmetros.

**Importante:**

Para que não ocorra conflito nas chamadas de web service, caso existam regras que utilizem o mesmo web service, a variável declarada deve ser uma diferente das já existentes.

**Exemplo:**

```lsp
Definir interno.com.senior.g5.rh.fp.calculoFolha.Calcular vCalcula;
Definir interno.com.senior.g5.rh.fp.calculoFolha.Calcular vCalcula2;
Definir interno.com.senior.g5.rh.fp.calculoFolha.Calcular vCalcula3;
Definir interno.com.senior.g5.rh.fp.calculoFolha.Calcular vCalcula4;
```

### Modos de Execução

Os modos de execução de web service via regra LSP são tratados por numeração na regra, conforme abaixo:

1. Local
2. Síncrono
3. Assíncrono

**Importante:**

Não é possível utilizar o modo de execução Agendado em regras LSP, pois não é possível informar a periodicidade na regra.

O parâmetro `ModoExecucao = 1 (Local)` deve ser utilizado apenas em regras que serão executadas em instâncias de web services. Ou seja, esse parâmetro não deve ser usado nas seguintes formas de acesso: Cliente-Servidor, BrowserAccess, WindowsAccess, Web 5.0 e processos automáticos.

### WS-Security

Permite a integração de sistemas que utilizam web services terceiros com autenticação WS-Security. Com isto, as chamadas destes web services, do tipo SOAP, permitem a inclusão de informações de segurança no cabeçalho e assim, a sua integração.

A customização desta chamada é realizada a partir de um parâmetro na regra LSP: `WSSeguranca`, que receberá um XML e posteriormente será repassado para o cabeçalho do envelope SOAP:

```lsp
Webservice.WSSeguranca = "XML_Segurança";
```

### Autenticação

A autenticação de web services é feita, por padrão, através dos parâmetros `usuario`, ou `user`, e `senha`, ou `password`. Quando não informado, a autenticação é feita através dos valores do usuário do sistema.

Caso desejar ignorar os parâmetros, acesse a Central de Configurações Senior e insira a chave `com.senior.middleware.webservices.use_implicit_params_login` com o valor `false`.

## Chamada HTTP

A LSP oferece um conjunto robusto de funções para realizar requisições HTTP/HTTPS, permitindo integração com APIs REST, web services e outros endpoints HTTP. Estas funções suportam todos os métodos HTTP principais e oferecem controle granular sobre cabeçalhos, timeouts e tratamento de respostas.

### Visão Geral das Funções HTTP

| Função | Descrição |
|--------|-----------|
| **Métodos HTTP Principais** |
| HttpGet | Executa requisições GET para obter dados |
| HttpPost | Executa requisições POST para enviar dados |
| HttpPut | Executa requisições PUT para atualizar recursos |
| HttpPatch | Executa requisições PATCH para modificações parciais |
| HttpDelete | Executa requisições DELETE para remover recursos |
| HttpDeleteBody | Executa requisições DELETE com corpo da mensagem |
| HttpDownload | Faz download de arquivos diretamente para disco |
| **Configuração e Upload** |
| HttpSetAttachment | Anexa arquivos locais ao corpo da requisição |
| HttpAlteraCabecalhoRequisicao | Configura cabeçalhos HTTP personalizados |
| HttpAlteraCodifCaracPadrao | Define codificação de caracteres padrão |
| HttpAlteraRedirecionamento | Controla tratamento de redirecionamentos |
| HttpSetaTimeout | Define timeout para requisições |
| **Gerenciamento de Sessão** |
| HttpHabilitarCookies | Habilita armazenamento automático de cookies |
| HttpDesabilitarCookies | Desabilita armazenamento de cookies |
| **Leitura de Respostas** |
| HttpLeCabecalhoResposta | Obtém cabeçalhos de resposta do servidor |
| HttpLeCodigoResposta | Consulta código de status da resposta |
| HttpNormalizaRetorno | Normaliza caracteres Unicode em respostas |
| **Configuração de Proxy** |
| HttpAlteraConfiguracaoProxy | Configura definições de servidor proxy |
| HttpLeConfiguracaoProxy | Lê configurações atuais de proxy |
| **Configuração SSL/TLS** |
| HttpAlteraConfiguracaoSSL | Configura opções SSL/TLS |
| HttpLeConfiguracaoSSL | Lê configurações SSL atuais |
| HttpHabilitaSNI | Habilita Server Name Indication |
| HttpDesabilitaSNI | Desabilita Server Name Indication |
| **Utilitários** |
| HttpObjeto | Cria objeto HTTP com configurações padrão |
| HttpDesabilitaErroResposta | Desabilita erros automáticos HTTP |
| HttpHabilitaErroResposta | Habilita erros automáticos HTTP |
| Base64Encode | Codifica strings em Base64 para autenticação |
| Base64Decode | Decodifica strings Base64 de volta para texto |

### Configuração Inicial

Antes de realizar qualquer requisição HTTP, é necessário criar um objeto HTTP:

```lsp
Definir Alfa vaHTTP;
HttpObjeto(vaHTTP);
```

### ⚠️ **Importante: Configurações e Limitações HTTP**

#### **Configurações de Acesso**

As funções que executam requisições (HttpGet, HttpPost, HttpPut, HttpPatch, HttpDelete e HttpDownload) necessitam de um **HttpObjeto** que contenha as configurações de acesso como:
- Servidor proxy
- Configurações SSL/TLS
- Codificação de caracteres
- Timeouts
- Cookies

#### **Formas de Configurar:**

1. **🌐 Central de Configurações Senior**
   - Configure na tela "Configurações de Internet"
   - Aplicadas automaticamente para todos os objetos HTTP

2. **💻 Dentro da regra LSP** 
   - Configure programaticamente usando as funções de manipulação
   - Alterações feitas apenas **em memória** no objeto HTTP específico
   - Sobrescreve as configurações da Central de Configurações

#### **⚠️ Limitações Importantes:**

- **❌ Certificados digitais**: As funções HTTP LSP **NÃO oferecem suporte** ao uso de certificados digitais
- **✅ Parâmetros suportados**: Apenas parâmetros que compõem as requisições (headers, content-type, autenticação básica, etc.)

**Exemplo de configuração programática:**
```lsp
Definir Alfa vaHTTP;

HttpObjeto(vaHTTP);

@ Configurações específicas para esta requisição @
HttpAlteraConfiguracaoProxy(vaHTTP, 1, "proxy.empresa.com", 8080, 1);
HttpAlteraConfiguracaoSSL(vaHTTP, 2); @ Sempre SSL @
HttpAlteraCodifCaracPadrao(vaHTTP, "utf-8");
HttpSetaTimeout(vaHTTP, 30);

@ Essas configurações só afetam este objeto vaHTTP @
HttpGet(vaHTTP, "https://api.exemplo.com/dados", vaResposta);
```

### HttpGet

Executa uma requisição HTTP GET para obter dados de um servidor. É o método mais utilizado para consulta de dados em APIs REST.

**Sintaxe:** `HttpGet(Alfa Objeto, Alfa URL, Alfa end HTML);`

**Parâmetros:**
- `Objeto`: Objeto HTTP criado com HttpObjeto
- `URL`: URL completa do endpoint (deve incluir http:// ou https://)
- `HTML`: Variável que receberá a resposta do servidor

**Exemplo Básico:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;

HttpObjeto(vaHTTP);
HttpGet(vaHTTP, "https://www.senior.com.br/index.htm", vaResposta);
Mensagem(Retorna, vaResposta);
```

**Exemplo com Cabeçalhos Personalizados:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;

HttpObjeto(vaHTTP);

@ Configurar cabeçalhos @
HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept", "application/json");
HttpAlteraCabecalhoRequisicao(vaHTTP, "User-Agent", "SeniorApp/1.0");
HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", "Bearer token123");

HttpGet(vaHTTP, "https://api.exemplo.com/dados", vaResposta);
```

**Exemplo com Verificação de Status:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;
Definir Numero vnStatus;

HttpObjeto(vaHTTP);
HttpDesabilitaErroResposta(vaHTTP);

HttpGet(vaHTTP, "https://api.exemplo.com/usuarios", vaResposta);
HttpLeCodigoResposta(vaHTTP, vnStatus);

Se (vnStatus = 200) {
  @ Processar resposta @
  Mensagem(Retorna, "Dados recebidos com sucesso!");
} Senao {
  @ Tratar erro @
  Mensagem(Erro, "Erro na requisição. Status: " + vnStatus);
}
```

**Observações:**
- Sempre informe a URL completa com protocolo (http:// ou https://)
- Para HTTPS sem certificado, use `HttpHabilitaSNI(vaHTTP)` antes da requisição
- Caracteres especiais na URL podem causar erros em alguns sistemas
- Use `HttpDesabilitaErroResposta` para controle manual de erros

### HttpPost

Executa uma requisição HTTP POST para enviar dados ao servidor. Utilizado para criação de recursos, envio de formulários e dados em geral.

**Sintaxe:** `HttpPost(Alfa Objeto, Alfa URL, Alfa Dados, Alfa end HTML);`

**Parâmetros:**
- `Objeto`: Objeto HTTP criado com HttpObjeto
- `URL`: URL do endpoint
- `Dados`: Dados a serem enviados no corpo da requisição
- `HTML`: Variável que receberá a resposta

**Exemplo com Dados de Formulário:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;
Definir Alfa vaDados;

HttpObjeto(vaHTTP);

@ Dados no formato application/x-www-form-urlencoded @
vaDados = "NomeUsuario=SENIOR&EmailUsuario=senior@senior.com.br&Texto=SENIOR+SA";

HttpPost(vaHTTP, "https://www.senior.com.br/cadastro.html", vaDados, vaResposta);
Mensagem(Retorna, vaResposta);
```

**Exemplo com JSON:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;
Definir Alfa vaDados;

HttpObjeto(vaHTTP);

@ Configurar para JSON @
HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept", "text/plain");
HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json");

@ Dados em formato JSON @
vaDados = "{\"NomeParametro1\": \"valor1\", \"NomeParametro2\": \"valor2\"}";

HttpPost(vaHTTP, "https://exemplo.com/app/path", vaDados, vaResposta);
```

**Exemplo com Autenticação:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;
Definir Alfa vaDados;
Definir Alfa vaToken;

HttpObjeto(vaHTTP);

@ Configurar autenticação @
vaToken = "Bearer seu_token_aqui";
HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", vaToken);
HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json");

vaDados = "{\"nome\": \"João\", \"email\": \"joao@exemplo.com\"}";
HttpPost(vaHTTP, "https://api.exemplo.com/usuarios", vaDados, vaResposta);
```

**Observações:**
- O Content-Type padrão é `application/x-www-form-urlencoded; charset=windows-1252`
- Para JSON, sempre configure `Content-Type: application/json`
- Para UTF-8, configure explicitamente com `HttpAlteraCodifCaracPadrao`
- Quando usar JSON, os dados devem estar no formato correto, caso contrário retornará erro 400

### HttpPut

Executa uma requisição HTTP PUT para atualizar recursos existentes. Usado para modificar dados de um recurso específico.

**Sintaxe:** `HttpPut(Alfa Objeto, Alfa URL, Alfa Dados, Alfa end HTML);`

**Parâmetros:**
- `Objeto`: Objeto HTTP criado com HttpObjeto
- `URL`: URL do recurso a ser atualizado
- `Dados`: Dados de atualização
- `HTML`: Variável que receberá a resposta

**Exemplo Básico:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;
Definir Alfa vaDados;

HttpObjeto(vaHTTP);

vaDados = "NomeUsuario=SENIOR&EmailUsuario=senior@senior.com.br&Texto=SENIOR+SA";
HttpPut(vaHTTP, "https://www.senior.com.br/cadastro.html", vaDados, vaResposta);
Mensagem(Retorna, vaResposta);
```

**Exemplo com JSON:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;
Definir Alfa vaDados;

HttpObjeto(vaHTTP);

@ Configurar cabeçalhos @
HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json");
HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", "Bearer token123");

@ Dados para atualização @
vaDados = "{\"nome\": \"João Silva\", \"status\": \"ativo\", \"email\": \"joao.silva@exemplo.com\"}";

HttpPut(vaHTTP, "https://api.exemplo.com/usuarios/123", vaDados, vaResposta);
```

**Observações:**
- PUT é usado para atualização completa de recursos
- Só suporta formato texto, não arquivos binários
- Sempre inclua todos os campos necessários do recurso

### HttpDelete

Executa uma requisição HTTP DELETE para remover recursos. Usado para exclusão de dados específicos.

**Sintaxe:** `HttpDelete(Alfa Objeto, Alfa URL, Alfa end HTML);`

**Parâmetros:**
- `Objeto`: Objeto HTTP criado com HttpObjeto
- `URL`: URL do recurso a ser removido
- `HTML`: Variável que receberá a resposta

**Exemplo Básico:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;

HttpObjeto(vaHTTP);

HttpDelete(vaHTTP, "https://www.senior.com.br/registro/1", vaResposta);
Mensagem(Retorna, vaResposta);
```

**Exemplo com Autenticação:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;
Definir Numero vnStatus;

HttpObjeto(vaHTTP);
HttpDesabilitaErroResposta(vaHTTP);

@ Configurar autenticação @
HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", "Bearer token123");

HttpDelete(vaHTTP, "https://api.exemplo.com/usuarios/123", vaResposta);

@ Verificar resultado @
HttpLeCodigoResposta(vaHTTP, vnStatus);
Se (vnStatus = 204) {
  Mensagem(Retorna, "Usuário excluído com sucesso!");
} Senao {
  Mensagem(Erro, "Erro ao excluir usuário. Status: " + vnStatus);
}
```

### HttpDeleteBody

Executa uma requisição HTTP DELETE com dados no corpo da mensagem. Útil para exclusões em lote ou com parâmetros específicos.

**Sintaxe:** `HttpDeleteBody(Alfa Objeto, Alfa URL, Alfa Dados, Alfa end HTML);`

**Parâmetros:**
- `Objeto`: Objeto HTTP criado com HttpObjeto
- `URL`: URL do endpoint
- `Dados`: Dados a serem enviados no corpo
- `HTML`: Variável que receberá a resposta

**Exemplo Básico:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;
Definir Alfa vaDados;

HttpObjeto(vaHTTP);

vaDados = "[{\"id\": \"123\"}]";
HttpDeleteBody(vaHTTP, "https://www.senior.com.br/registro", vaDados, vaResposta);
Mensagem(Retorna, vaResposta);
```

**Exemplo com Múltiplos IDs:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;
Definir Alfa vaDados;

HttpObjeto(vaHTTP);

@ Configurar cabeçalhos @
HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json");
HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", "Bearer token123");

@ Lista de IDs para exclusão em lote @
vaDados = "[{\"id\": \"123\"}, {\"id\": \"456\"}, {\"id\": \"789\"}]";

HttpDeleteBody(vaHTTP, "https://api.exemplo.com/usuarios/lote", vaDados, vaResposta);
```

### HttpDownload

Faz download de arquivos diretamente para o disco, sem carregar na memória. Ideal para arquivos grandes.

**Sintaxe:** `HttpDownload(Alfa Objeto, Alfa URL, Alfa Arquivo);`

**Parâmetros:**
- `Objeto`: Objeto HTTP criado com HttpObjeto
- `URL`: URL do arquivo para download
- `Arquivo`: Caminho completo onde salvar o arquivo

**Exemplo Básico:**
```lsp
Definir Alfa vaHTTP;

HttpObjeto(vaHTTP);
HttpDownload(vaHTTP, "https://www.senior.com.br/product.zip", "C:\\Senior\\product.zip");
```

**Exemplo com Verificação:**
```lsp
Definir Alfa vaHTTP;
Definir Numero vnStatus;
Definir Alfa vaCaminho;

HttpObjeto(vaHTTP);
HttpDesabilitaErroResposta(vaHTTP);

vaCaminho = "C:\\Downloads\\relatorio.pdf";
HttpDownload(vaHTTP, "https://exemplo.com/relatorio.pdf", vaCaminho);

HttpLeCodigoResposta(vaHTTP, vnStatus);
Se (vnStatus = 200) {
  Mensagem(Retorna, "Download concluído: " + vaCaminho);
} Senao {
  Mensagem(Erro, "Erro no download. Status: " + vnStatus);
}
```

**Observações:**
- Funciona como HttpGet, mas salva diretamente em arquivo
- Recomendado para arquivos grandes para evitar consumo excessivo de memória
- O diretório de destino deve existir

### HttpSetaTimeout

Define um timeout (tempo limite) para requisições HTTP. Evita travamentos em requisições lentas.

**Sintaxe:** `HttpSetaTimeout(Alfa Objeto, Numero Timeout);`

**Parâmetros:**
- `Objeto`: Objeto HTTP criado com HttpObjeto
- `Timeout`: Tempo limite em segundos

**Exemplo Básico:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;

HttpObjeto(vaHTTP);

@ Definir timeout de 5 segundos @
HttpSetaTimeout(vaHTTP, 5);

HttpGet(vaHTTP, "https://httpstat.us/200?sleep=4000", vaResposta);
Mensagem(Retorna, vaResposta);
```

**Exemplo com Diferentes Timeouts:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;

HttpObjeto(vaHTTP);

@ Para APIs rápidas - timeout baixo @
HttpSetaTimeout(vaHTTP, 10);
HttpGet(vaHTTP, "https://api-rapida.exemplo.com/dados", vaResposta);

@ Para APIs lentas - timeout maior @
HttpSetaTimeout(vaHTTP, 120);
HttpGet(vaHTTP, "https://api-lenta.exemplo.com/relatorio", vaResposta);
```

### HttpPatch

Executa uma requisição HTTP PATCH para aplicar modificações parciais em um recurso. Ideal para atualizações que modificam apenas alguns campos.

**Sintaxe:** `HttpPatch(Alfa end Objeto, Alfa URL, Alfa Dados, Alfa end Retorno);`

**Parâmetros:**
- `Objeto`: Objeto HTTP criado com HttpObjeto
- `URL`: URL do recurso a ser modificado parcialmente
- `Dados`: Dados de modificação parcial no formato texto
- `Retorno`: Variável que receberá a resposta

**Exemplo Básico:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;
Definir Alfa vaDados;

HttpObjeto(vaHTTP);

@ Dados para modificação parcial (apenas os campos que mudaram) @
vaDados = "{\"status\": \"ativo\", \"ultimo_acesso\": \"2024-01-15\"}";

HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json");
HttpPatch(vaHTTP, "https://api.exemplo.com/usuarios/123", vaDados, vaResposta);
```

**Exemplo com Verificação:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;
Definir Alfa vaDados;
Definir Numero vnStatus;

HttpObjeto(vaHTTP);
HttpDesabilitaErroResposta(vaHTTP);

vaDados = "{\"email\": \"novo@exemplo.com\"}";

HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json");
HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", "Bearer token123");

HttpPatch(vaHTTP, "https://api.exemplo.com/perfil", vaDados, vaResposta);

HttpLeCodigoResposta(vaHTTP, vnStatus);
Se (vnStatus = 200) {
  Mensagem(Retorna, "Perfil atualizado com sucesso!");
} Senao {
  Mensagem(Erro, "Erro ao atualizar. Status: " + vnStatus);
}
```

**Observações:**
- PATCH é usado para modificações parciais (só os campos alterados)
- Diferente do PUT, que substitui o recurso completo
- Suporta apenas formato texto, não arquivos binários

### HttpSetAttachment

Permite o envio de arquivos locais no corpo de uma requisição HTTP. Disponível para os métodos POST, PUT e PATCH.

**Sintaxe:** `HttpSetAttachment(Alfa end Objeto, Alfa CaminhoArquivo);`

**Parâmetros:**
- `Objeto`: Objeto HTTP criado com HttpObjeto
- `CaminhoArquivo`: Caminho completo do arquivo local a ser anexado

**Exemplo com POST:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;

HttpObjeto(vaHTTP);

@ Anexar arquivo @
HttpSetAttachment(vaHTTP, "C:\\temp\\documento.pdf");

@ Configurar cabeçalhos @
HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", "Bearer token123");

HttpPost(vaHTTP, "https://api.exemplo.com/upload", "", vaResposta);
```

**Exemplo com Múltiplos Arquivos (conceitual):**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;

HttpObjeto(vaHTTP);

@ Para múltiplos arquivos, fazer requisições separadas @
HttpSetAttachment(vaHTTP, "C:\\docs\\relatorio.pdf");
HttpPost(vaHTTP, "https://api.exemplo.com/upload", "", vaResposta);

HttpSetAttachment(vaHTTP, "C:\\docs\\planilha.xlsx");
HttpPost(vaHTTP, "https://api.exemplo.com/upload", "", vaResposta);
```

**Observações:**
- O arquivo deve existir no caminho especificado
- Funciona com POST, PUT e PATCH
- Para múltiplos arquivos, faça requisições separadas

### Base64Encode / Base64Decode

Funções para codificar e decodificar strings em Base64, essenciais para autenticação HTTP básica e transmissão segura de dados.

#### Base64Encode

Codifica strings em Base64, comumente usado para autenticação básica HTTP.

**Sintaxe:** `Base64Encode(Alfa valor, Alfa end Base64Encode);`

**Parâmetros:**
- `valor`: String a ser codificada em Base64
- `Base64Encode`: Variável que receberá o resultado codificado

#### Base64Decode

Decodifica um valor Base64 de volta para texto original.

**Sintaxe:** `Base64Decode(Alfa valor, Alfa end Base64Decode);`

**Parâmetros:**
- `valor`: Valor em Base64 a ser decodificado
- `Base64Decode`: Variável que receberá o conteúdo decodificado

**Exemplo Básico de Codificação:**
```lsp
Definir Alfa vaValor;
Definir Alfa vaBase64;

vaValor = "valor para converter";
Base64Encode(vaValor, vaBase64);
Mensagem(Retorna, vaBase64); @ Exibirá: dmFsb3IgcGFyYSBjb252ZXJ0ZXI= @
```

**Exemplo Básico de Decodificação:**
```lsp
Definir Alfa vaValorBase64;
Definir Alfa vaValor;

vaValorBase64 = "dmFsb3IgcGFyYSBjb252ZXJ0ZXI=";
Base64Decode(vaValorBase64, vaValor);
Mensagem(Retorna, vaValor); @ Exibirá: valor para converter @
```

**Exemplo para Autenticação HTTP:**
```lsp
Definir Alfa vaUsuario;
Definir Alfa vaSenha;
Definir Alfa vaCredenciais;
Definir Alfa vaBase64;
Definir Alfa vaAuth;

vaUsuario = "admin";
vaSenha = "senha123";
vaCredenciais = vaUsuario + ":" + vaSenha;

@ Codificar credenciais @
Base64Encode(vaCredenciais, vaBase64);
vaAuth = "Basic " + vaBase64;

@ Usar vaAuth no cabeçalho Authorization @
HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", vaAuth);
```

**Exemplo de Uso Completo (Codificar e Decodificar):**
```lsp
Definir Alfa vaTextoOriginal;
Definir Alfa vaTextoCodificado;
Definir Alfa vaTextoDecodificado;

vaTextoOriginal = "dados sensíveis da aplicação";

@ Codificar para transmissão segura @
Base64Encode(vaTextoOriginal, vaTextoCodificado);
Mensagem(Retorna, "Dados codificados: " + vaTextoCodificado);

@ Decodificar após receber @
Base64Decode(vaTextoCodificado, vaTextoDecodificado);
Mensagem(Retorna, "Dados decodificados: " + vaTextoDecodificado);

@ Verificar se são iguais @
Se (vaTextoOriginal = vaTextoDecodificado) {
  Mensagem(Retorna, "Codificação/Decodificação realizada com sucesso!");
}
```

**Casos de Uso Comuns:**
- **Autenticação HTTP Basic**: Codificar usuário:senha
- **Tokens de API**: Decodificar tokens JWT recebidos 
- **Transmissão de dados**: Codificar dados binários como texto
- **Armazenamento**: Codificar credenciais para armazenamento temporário
- **Integração**: Decodificar dados recebidos de APIs externas

### Exemplo Completo: Sistema de Autenticação

Aqui está um exemplo completo de geração de token com autenticação básica:

```lsp
Definir Alfa vaToken;
Definir Funcao gerarToken();

gerarToken();

Funcao gerarToken(); {
  Definir Alfa vaHTTP;
  Definir Alfa vaJSON;
  Definir Alfa vaCodRes;
  Definir Alfa vaMsgUsu;
  Definir Numero vnCodRes;
  
  Definir Alfa vaUsuario;
  Definir Alfa vaAPIKey;
  Definir Alfa vaEncode;
  Definir Alfa vaAuthToken;
  Definir Alfa vaURL;
  Definir Alfa vaDados;

  @ Credenciais de exemplo (substitua pelas reais) @
  vaUsuario = "usuario_demo";  
  vaAPIKey = "sk_test_1234567890abcdef1234567890abcdef12345678";
  
  @ Criar token de autenticação Basic @
  vaEncode = vaUsuario + ":" + vaAPIKey;
  Base64Encode(vaEncode, vaAuthToken); 
  vaAuthToken = "Basic " + vaAuthToken;
  
  @ Configurar URL e dados @
  vaURL = "https://api.exemplo.com/v1/auth/token"; 
  vaDados = "{\"numero_cartao\": \"0012345678\"}";
  
  @ Criar objeto HTTP @
  HttpObjeto(vaHTTP);

  @ Configurar tratamento de erros @
  HttpDesabilitaErroResposta(vaHTTP); 
  
  @ Configurar timeout @
  HttpSetaTimeout(vaHTTP, 30);
  
  @ Configurar cabeçalhos @
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept", "application/json;charset=utf-8");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json;charset=utf-8");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept-Charset", "utf-8");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Cache-Control", "no-cache");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", vaAuthToken);
  HttpAlteraCodifCaracPadrao(vaHTTP, "utf-8");
  
  @ Executar requisição @
  HttpPost(vaHTTP, vaURL, vaDados, vaJSON);
  
  @ Verificar código de resposta @
  HttpLeCodigoResposta(vaHTTP, vnCodRes);
  
  @ Processar resposta de sucesso @
  Se ((vnCodRes >= 200) e (vnCodRes <= 204)) {
    @ Extrair token do JSON @
    ValorElementoJson(vaJSON, "", "token", vaToken);
    
    @ Log de sucesso @
    Mensagem(Retorna, "Token gerado com sucesso!");
  }
  
  @ Tratamento de erro @
  Se ((vnCodRes < 200) ou (vnCodRes >= 300)) {
    IntParaAlfa(vnCodRes, vaCodRes);
    vaMsgUsu = "Erro HTTP [" + vaCodRes + "]: Falha na autenticação. Verifique as credenciais.";
    Mensagem(Erro, vaMsgUsu);
  }
}
```

### Funções de Configuração Avançada

#### HttpAlteraCabecalhoRequisicao

Configura cabeçalhos HTTP personalizados para requisições. Válido para todos os métodos HTTP.

**Sintaxe:** `HttpAlteraCabecalhoRequisicao(Alfa end Objeto, Alfa Nome, Alfa Valor);`

**Parâmetros:**
- `Objeto`: Objeto HTTP criado com HttpObjeto
- `Nome`: Nome do cabeçalho (não pode ser vazio)
- `Valor`: Valor do cabeçalho (vazio remove o cabeçalho)

**Exemplo com API REST:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;

HttpObjeto(vaHTTP);

HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept", "text/plain");
HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json");
HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", "Bearer token123");
HttpAlteraCabecalhoRequisicao(vaHTTP, "User-Agent", "MeuApp/1.0");

HttpPost(vaHTTP, "https://exemplo.com/app/path", "<dados>", vaResposta);
```

#### HttpAlteraCodifCaracPadrao

Configura a codificação de caracteres para respostas do servidor quando não especificada.

**Sintaxe:** `HttpAlteraCodifCaracPadrao(Alfa end Objeto, Alfa Codificacao);`

**Parâmetros:**
- `Objeto`: Objeto HTTP criado com HttpObjeto
- `Codificacao`: Nome da codificação (UTF-8, ISO-8859-1, Windows-1252)

**Exemplo:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;

HttpObjeto(vaHTTP);

@ Configurar para UTF-8 @
HttpAlteraCodifCaracPadrao(vaHTTP, "utf-8");

HttpGet(vaHTTP, "https://api.exemplo.com/dados", vaResposta);
```

**Observações:**
- Valor padrão: ISO-8859-1
- Codificações suportadas: UTF-8, ISO-8859-1, Windows-1252
- Se a codificação for inválida, pode retornar vazio ou erro

#### HttpAlteraRedirecionamento

Controla o tratamento automático de redirecionamentos HTTP (3xx).

**Sintaxe:** `HttpAlteraRedirecionamento(Alfa Objeto, Numero AceitaRedirecionamento);`

**Parâmetros:**
- `Objeto`: Objeto HTTP criado com HttpObjeto
- `AceitaRedirecionamento`: 0 = Não trata, 1 = Trata redirecionamentos

**Exemplo:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;

HttpObjeto(vaHTTP);

@ Habilitar tratamento automático de redirecionamentos @
HttpAlteraRedirecionamento(vaHTTP, 1);

HttpGet(vaHTTP, "https://site-com-redirect.exemplo.com", vaResposta);
```

### Funções de Gerenciamento de Cookies

#### HttpHabilitarCookies / HttpDesabilitarCookies

Controla o armazenamento e envio automático de cookies durante as requisições.

**Sintaxe:** 
- `HttpHabilitarCookies(Alfa Objeto);`
- `HttpDesabilitarCookies(Alfa Objeto);`

**Exemplo:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;

HttpObjeto(vaHTTP);

@ Habilitar cookies para manter sessão @
HttpHabilitarCookies(vaHTTP);

@ Fazer login @
HttpPost(vaHTTP, "https://app.exemplo.com/login", "user=admin&pass=123", vaResposta);

@ Os cookies de sessão serão enviados automaticamente @
HttpGet(vaHTTP, "https://app.exemplo.com/dashboard", vaResposta);

@ Desabilitar cookies se necessário @
HttpDesabilitarCookies(vaHTTP);
```

### Funções de Leitura de Respostas

#### HttpLeCabecalhoResposta

Obtém valores de cabeçalhos retornados pelo servidor após uma requisição.

**Sintaxe:** `HttpLeCabecalhoResposta(Alfa end Objeto, Alfa Nome, Alfa end Valor);`

**Parâmetros:**
- `Objeto`: Objeto HTTP após uma requisição
- `Nome`: Nome do cabeçalho a consultar
- `Valor`: Variável que receberá o valor (vazio se não existir)

**Exemplo:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;
Definir Alfa vaContentType;
Definir Alfa vaContentLength;
Definir Alfa vaServer;

HttpObjeto(vaHTTP);

HttpGet(vaHTTP, "https://exemplo.com/api/dados", vaResposta);

@ Ler cabeçalhos de resposta @
HttpLeCabecalhoResposta(vaHTTP, "Content-Type", vaContentType);
HttpLeCabecalhoResposta(vaHTTP, "Content-Length", vaContentLength);
HttpLeCabecalhoResposta(vaHTTP, "Server", vaServer);

Mensagem(Retorna, "Tipo: " + vaContentType + ", Tamanho: " + vaContentLength);
```

**Observações:**
- Disponível apenas após realizar uma requisição
- Se o mesmo cabeçalho aparecer múltiplas vezes, retorna apenas o primeiro
- Exceção: WWW-Authenticate e Proxy-Authenticate podem retornar múltiplos valores

#### HttpNormalizaRetorno

Aplica normalização Unicode para caracteres acentuados em respostas HTTP.

**Sintaxe:** `HttpNormalizaRetorno(Alfa end Objeto);`

**Exemplo:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;

HttpObjeto(vaHTTP);

@ Habilitar normalização Unicode @
HttpNormalizaRetorno(vaHTTP);

HttpGet(vaHTTP, "https://api.exemplo.com/dados-acentuados", vaResposta);

@ A resposta terá caracteres acentuados normalizados @
Mensagem(Retorna, vaResposta);
```

**Observações:**
- Converte caracteres como Á (dois code points) para Á (um code point)
- Útil para compatibilidade com sistemas que usam diferentes representações Unicode
- Aplica normalização canônica Unicode C

### Configuração de Proxy

#### HttpAlteraConfiguracaoProxy

Configura as definições de servidor proxy para as requisições.

**Sintaxe:** `HttpAlteraConfiguracaoProxy(Alfa Objeto, Numero UsarProxy, Alfa Servidor, Numero Porta, Numero AutPorUsu);`

**Parâmetros:**
- `UsarProxy`: 0 = Não usar, 1 = Usar proxy
- `Servidor`: Endereço do servidor proxy
- `Porta`: Porta do servidor proxy
- `AutPorUsu`: 0 = Sem autenticação, 1 = Com autenticação

**Exemplo:**
```lsp
Definir Alfa vaHTTP;

HttpObjeto(vaHTTP);

@ Configurar proxy corporativo @
HttpAlteraConfiguracaoProxy(vaHTTP, 1, "proxy.empresa.com.br", 8080, 1);

HttpGet(vaHTTP, "https://api.externa.com/dados", vaResposta);
```

#### HttpLeConfiguracaoProxy

Lê as configurações atuais de proxy do objeto HTTP.

**Sintaxe:** `HttpLeConfiguracaoProxy(Alfa Objeto, Numero end UsarProxy, Alfa end Servidor, Numero end Porta, Numero end AutPorUsu);`

**Exemplo:**
```lsp
Definir Alfa vaHTTP;
Definir Numero vnUsarProxy;
Definir Alfa vaServidor;
Definir Numero vnPorta;
Definir Numero vnAutPorUsu;

HttpObjeto(vaHTTP);

HttpLeConfiguracaoProxy(vaHTTP, vnUsarProxy, vaServidor, vnPorta, vnAutPorUsu);

Se (vnUsarProxy = 1) {
  Mensagem(Retorna, "Proxy: " + vaServidor + ":" + vnPorta);
}
```

#### HttpAlteraAutenticacaoProxy / HttpLeAutenticacaoProxy

Configura e lê as credenciais de autenticação para o servidor proxy.

**Sintaxe:**
- `HttpAlteraAutenticacaoProxy(Alfa Objeto, Alfa Usuario, Alfa Senha);`
- `HttpLeAutenticacaoProxy(Alfa Objeto, Alfa end Usuario, Alfa end Senha);`

**Parâmetros:**
- `Usuario`: Nome de usuário para autenticação no proxy
- `Senha`: Senha para autenticação no proxy

**Exemplo de Configuração:**
```lsp
Definir Alfa vaHTTP;

HttpObjeto(vaHTTP);

@ Configurar credenciais do proxy @
HttpAlteraAutenticacaoProxy(vaHTTP, "nome", "senha");
```

**Exemplo de Leitura:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaUsuario;
Definir Alfa vaSenha;

HttpObjeto(vaHTTP);

@ Ler credenciais configuradas @
HttpLeAutenticacaoProxy(vaHTTP, vaUsuario, vaSenha);

Mensagem(Retorna, "Usuário proxy: " + vaUsuario);
```

**⚠️ Observações Importantes:**

#### **Autenticação Automática:**
- Se não informar usuário/senha válidos e a conexão exigir autenticação em servidor proxy, será exibida uma **tela de autenticação**

#### **🌐 Limitação WEB 5.0:**
- A **tela de autenticação NÃO está disponível na WEB 5.0**
- Para conexões que exigem autenticação, **deve-se obrigatoriamente** informar usuário e senha válidos
- Configure através de uma das opções:
  1. **Configuração padrão** na Central de Configurações
  2. **SGU** (Sistema de Gerenciamento de Usuários)
  3. **Regra LSP** usando `HttpAlteraAutenticacaoProxy`

#### **Comportamento da Leitura:**
- Se configurado para **autenticação por usuário**: retorna valores do **SGU**
- Caso contrário: retorna valores das propriedades **Usuário padrão** e **Senha padrão**

#### Gerenciamento de Exceções de Proxy

##### HttpAdicionaExcecaoProxy

Adiciona endereços à lista de exceções de proxy (URLs que não passam pelo proxy).

**Sintaxe:** `HttpAdicionaExcecaoProxy(Alfa Objeto, Alfa Endereco);`

**Observação:** O endereço não deve ser precedido do protocolo (ex: "localhost" em vez de "http://localhost").

##### HttpLeContadorExcecoesProxy

Retorna a quantidade de exceções cadastradas na lista de proxy.

**Sintaxe:** `HttpLeContadorExcecoesProxy(Alfa Objeto, Numero end Quantidade);`

##### HttpLeExcecaoProxy

Retorna um endereço específico da lista de exceções de proxy pelo índice.

**Sintaxe:** `HttpLeExcecaoProxy(Alfa Objeto, Numero Indice, Alfa end Endereco);`

##### HttpExcluiExcecaoProxy

Remove um endereço específico da lista de exceções pelo índice.

**Sintaxe:** `HttpExcluiExcecaoProxy(Alfa Objeto, Numero Indice);`

##### HttpLimpaExcecoesProxy

Remove todos os endereços da lista de exceções de proxy.

**Sintaxe:** `HttpLimpaExcecoesProxy(Alfa Objeto);`

**Exemplo completo de gerenciamento de exceções:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaEndereco;
Definir Numero vnQuantidade;
Definir Numero vnIndice;

HttpObjeto(vaHTTP);

@ Limpar exceções existentes @
HttpLimpaExcecoesProxy(vaHTTP);

@ Adicionar exceções para serviços internos @
HttpAdicionaExcecaoProxy(vaHTTP, "localhost");
HttpAdicionaExcecaoProxy(vaHTTP, "127.0.0.1");
HttpAdicionaExcecaoProxy(vaHTTP, "api-interna.empresa.com.br");
HttpAdicionaExcecaoProxy(vaHTTP, "10.0.30.25");

@ Verificar quantidade de exceções @
HttpLeContadorExcecoesProxy(vaHTTP, vnQuantidade);
Mensagem(Retorna, "Total de exceções: " + vnQuantidade);

@ Listar todas as exceções @
Para (vnIndice = 0; vnIndice < vnQuantidade; vnIndice++) {
  HttpLeExcecaoProxy(vaHTTP, vnIndice, vaEndereco);
  Mensagem(Retorna, "Exceção " + vnIndice + ": " + vaEndereco);
}

@ Remover uma exceção específica (índice 2) @
HttpExcluiExcecaoProxy(vaHTTP, 2);
```

### Configuração SSL

#### HttpAlteraConfiguracaoSSL / HttpLeConfiguracaoSSL

Controla as configurações SSL/TLS para requisições HTTPS.

**Sintaxe:** 
- `HttpAlteraConfiguracaoSSL(Alfa Objeto, Numero SSL);`
- `HttpLeConfiguracaoSSL(Alfa Objeto, Numero end SSL);`

**Valores SSL:**
- 0 = Automático
- 1 = Nunca
- 2 = Sempre

**Exemplo:**
```lsp
Definir Alfa vaHTTP;
Definir Numero vnSSL;

HttpObjeto(vaHTTP);

@ Sempre usar SSL @
HttpAlteraConfiguracaoSSL(vaHTTP, 2);

@ Verificar configuração @
HttpLeConfiguracaoSSL(vaHTTP, vnSSL);
```

### Configuração de Progresso de Download

#### HttpAlteraMostrarProgresso / HttpLeMostrarProgresso

Controla a exibição da barra de progresso durante downloads de arquivos.

**Sintaxe:**
- `HttpAlteraMostrarProgresso(Alfa Objeto, Numero Mostrar);`
- `HttpLeMostrarProgresso(Alfa Objeto, Numero end Mostrar);`

**Parâmetros:**
- `Mostrar`: 0 = Não exibir progresso, 1 = Exibir progresso

**Exemplo Básico:**
```lsp
Definir Alfa vaHTTP;

HttpObjeto(vaHTTP);

@ Habilitar barra de progresso @
HttpAlteraMostrarProgresso(vaHTTP, 1);
```

**Exemplo Completo:**
```lsp
Definir Alfa vaHTTP;
Definir Numero vnMostrarProgresso;

HttpObjeto(vaHTTP);

@ Habilitar barra de progresso para downloads @
HttpAlteraMostrarProgresso(vaHTTP, 1);

@ Verificar configuração atual @
HttpLeMostrarProgresso(vaHTTP, vnMostrarProgresso);

Se (vnMostrarProgresso = 1) {
  Mensagem(Retorna, "Progresso de download habilitado");
}

@ Fazer download com progresso visível @
HttpDownload(vaHTTP, "https://exemplo.com/arquivo-grande.zip", "C:\\Downloads\\arquivo.zip");

@ Desabilitar progresso para próximas operações @
HttpAlteraMostrarProgresso(vaHTTP, 0);
```

**Casos de Uso:**
- **Downloads grandes**: Habilite para mostrar progresso ao usuário
- **Downloads automáticos**: Desabilite para não interromper o fluxo
- **Experiência do usuário**: Use conforme a necessidade de feedback visual

### Configuração SNI (Server Name Indication)

#### HttpHabilitaSNI / HttpDesabilitaSNI

Controla o envio do nome do servidor na requisição HTTPS.

**Sintaxe:**
- `HttpHabilitaSNI(Alfa Objeto);`
- `HttpDesabilitaSNI(Alfa Objeto);`

**Exemplo:**
```lsp
Definir Alfa vaHTTP;
Definir Alfa vaResposta;

HttpObjeto(vaHTTP);

@ Habilitar SNI para sites que exigem @
HttpHabilitaSNI(vaHTTP);

HttpGet(vaHTTP, "https://www.google.com.br/", vaResposta);

@ O nome "google.com.br" será enviado na requisição @
```

**Observações:**
- SNI é desabilitado por padrão
- Necessário para alguns servidores que hospedam múltiplos domínios
- Obrigatório para alguns certificados SSL modernos

### Funções Auxiliares Importantes

As funções HTTP da LSP contam com várias funções auxiliares que permitem controle granular sobre as requisições.

#### Configuração de Cabeçalhos
```lsp
@ Cabeçalhos comuns para APIs REST @
HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept", "application/json");
HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json");
HttpAlteraCabecalhoRequisicao(vaHTTP, "User-Agent", "MeuApp/1.0");
HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", "Bearer " + vaToken);

@ Cabeçalhos para cache @
HttpAlteraCabecalhoRequisicao(vaHTTP, "Cache-Control", "no-cache");
HttpAlteraCabecalhoRequisicao(vaHTTP, "Pragma", "no-cache");
```

#### Verificação de Status HTTP
```lsp
HttpLeCodigoResposta(vaHTTP, vnCodigo);

Se (vnCodigo = 200) {
  @ Sucesso @
} Senao Se (vnCodigo = 201) {
  @ Criado com sucesso @
} Senao Se (vnCodigo = 401) {
  @ Não autorizado @
} Senao Se (vnCodigo = 404) {
  @ Não encontrado @
} Senao Se (vnCodigo >= 500) {
  @ Erro do servidor @
} Senao {
  @ Outros erros @
}
```

#### Controle de Erros
```lsp
@ Desabilita exceções automáticas para códigos 4xx/5xx @
HttpDesabilitaErroResposta(vaHTTP);

@ Habilita exceções automáticas (padrão) @
HttpHabilitaErroResposta(vaHTTP);
```

#### Configurações SSL e Proxy
```lsp
@ Para HTTPS sem certificado válido @
HttpHabilitaSNI(vaHTTP);

@ Configurar codificação @
HttpAlteraCodifCaracPadrao(vaHTTP, "utf-8");

@ Configurar proxy se necessário @
HttpAlteraConfiguracaoProxy(vaHTTP, 1, "proxy.exemplo.com", 8080, 1);
```

### Exemplo Completo: Configuração Corporativa

Aqui está um exemplo abrangente mostrando como configurar um objeto HTTP para um ambiente corporativo:

```lsp
Definir Funcao configurarHttpCorporativo();
Definir Funcao exemploRequisicaoCompleta();

configurarHttpCorporativo();
exemploRequisicaoCompleta();

Funcao configurarHttpCorporativo(); {
  Definir Alfa vaHTTP;
  Definir Alfa vaResposta;
  Definir Numero vnStatus;
  
  @ Criar objeto HTTP @
  HttpObjeto(vaHTTP);
  
  @ Configurar proxy corporativo @
  HttpAlteraConfiguracaoProxy(vaHTTP, 1, "proxy.empresa.com.br", 8080, 1);
  
  @ Adicionar exceções de proxy para serviços internos @
  HttpAdicionaExcecaoProxy(vaHTTP, "localhost");
  HttpAdicionaExcecaoProxy(vaHTTP, "127.0.0.1");
  HttpAdicionaExcecaoProxy(vaHTTP, "api-interna.empresa.com.br");
  
  @ Configurar SSL @
  HttpAlteraConfiguracaoSSL(vaHTTP, 2); @ Sempre usar SSL @
  HttpHabilitaSNI(vaHTTP);
  
  @ Configurar codificação @
  HttpAlteraCodifCaracPadrao(vaHTTP, "utf-8");
  
  @ Configurar redirecionamentos @
  HttpAlteraRedirecionamento(vaHTTP, 1);
  
  @ Habilitar cookies para sessões @
  HttpHabilitarCookies(vaHTTP);
  
  @ Configurar normalização Unicode @
  HttpNormalizaRetorno(vaHTTP);
  
  @ Configurar timeout @
  HttpSetaTimeout(vaHTTP, 60);
  
  @ Desabilitar erros automáticos para controle manual @
  HttpDesabilitaErroResposta(vaHTTP);
  
  @ Configurar cabeçalhos padrão @
  HttpAlteraCabecalhoRequisicao(vaHTTP, "User-Agent", "SistemaCorporativo/1.0");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept", "application/json");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Cache-Control", "no-cache");
  
  @ Exemplo de requisição com toda configuração @
  HttpGet(vaHTTP, "https://api.externa.com/dados", vaResposta);
  
  @ Verificar resultado @
  HttpLeCodigoResposta(vaHTTP, vnStatus);
  Se (vnStatus = 200) {
    Mensagem(Retorna, "Configuração corporativa funcionando!");
  } Senao {
    Mensagem(Erro, "Erro na configuração. Status: " + vnStatus);
  }
}

Funcao exemploRequisicaoCompleta(); {
  Definir Alfa vaHTTP;
  Definir Alfa vaResposta;
  Definir Alfa vaContentType;
  Definir Alfa vaServer;
  Definir Numero vnStatus;
  
  HttpObjeto(vaHTTP);
  
  @ Upload de arquivo com configuração completa @
  HttpSetAttachment(vaHTTP, "C:\\temp\\relatorio.pdf");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", "Bearer token123");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "X-Upload-Type", "document");
  
  HttpPost(vaHTTP, "https://api.exemplo.com/upload", "", vaResposta);
  
  @ Analisar resposta @
  HttpLeCodigoResposta(vaHTTP, vnStatus);
  HttpLeCabecalhoResposta(vaHTTP, "Content-Type", vaContentType);
  HttpLeCabecalhoResposta(vaHTTP, "Server", vaServer);
  
  Se (vnStatus = 201) {
    Mensagem(Retorna, "Upload realizado com sucesso!");
    Mensagem(Retorna, "Servidor: " + vaServer);
  } Senao {
    Mensagem(Erro, "Falha no upload. Status: " + vnStatus);
  }
}
```

### Boas Práticas

1. **Sempre configure timeouts** para evitar travamentos em requisições lentas
2. **Use HttpDesabilitaErroResposta** para controle manual de erros HTTP
3. **Configure cabeçalhos adequados** para cada tipo de API (Accept, Content-Type, etc.)
4. **Valide códigos de status HTTP** antes de processar respostas
5. **Use HTTPS** sempre que possível para garantir segurança
6. **Trate erros de rede** adequadamente com mensagens claras
7. **Para arquivos grandes**, use `HttpDownload` em vez de `HttpGet`
8. **Mantenha credenciais seguras** e nunca faça hardcode em produção
9. **Use Base64Encode/Base64Decode** para autenticação básica e decodificação de tokens
10. **Configure User-Agent** para identificar sua aplicação
11. **Configure proxy adequadamente** em ambientes corporativos
12. **Use exceções de proxy** para acessos internos sem proxy
13. **Habilite SNI** para sites que requerem certificados modernos
14. **Configure codificação UTF-8** para suporte internacional
15. **Use cookies** para manter sessões em aplicações web

### Códigos de Status HTTP Comuns

| Código | Significado | Uso Típico |
|--------|-------------|------------|
| 200 | OK | Requisição bem-sucedida |
| 201 | Created | Recurso criado com sucesso |
| 204 | No Content | Sucesso sem conteúdo de retorno |
| 400 | Bad Request | Requisição inválida ou malformada |
| 401 | Unauthorized | Autenticação necessária |
| 403 | Forbidden | Acesso negado |
| 404 | Not Found | Recurso não encontrado |
| 409 | Conflict | Conflito no estado do recurso |
| 422 | Unprocessable Entity | Dados inválidos |
| 500 | Internal Server Error | Erro interno do servidor |
| 502 | Bad Gateway | Erro de gateway |
| 503 | Service Unavailable | Serviço temporariamente indisponível |

### Observações Importantes

#### **Codificação e Caracteres**
- **Codificação padrão**: windows-1252. Para UTF-8, use `HttpAlteraCodifCaracPadrao(vaHTTP, "utf-8")`
- **Caracteres especiais**: Evite caracteres como `|` em URLs em alguns sistemas Senior
- **Unicode**: Use `HttpNormalizaRetorno` para normalizar caracteres acentuados
- **Codificações suportadas**: UTF-8, ISO-8859-1, Windows-1252

#### **SSL/TLS e Certificados**
- **SNI**: Use `HttpHabilitaSNI` para sites que requerem certificados modernos
- **Configuração SSL**: 0=Automático, 1=Nunca, 2=Sempre
- **HTTPS**: Sempre prefira HTTPS para segurança em produção

#### **Proxy e Rede**
- **Ambientes corporativos**: Configure proxy com `HttpAlteraConfiguracaoProxy`
- **Exceções de proxy**: Use `HttpAdicionaExcecaoProxy` para serviços internos
- **Redirecionamentos**: Habilite com `HttpAlteraRedirecionamento(vaHTTP, 1)`

#### **Upload e Download**
- **Upload de arquivos**: Use `HttpSetAttachment` para anexar arquivos
- **Download de arquivos grandes**: Prefira `HttpDownload` em vez de `HttpGet`
- **Formatos suportados**: POST/PUT/PATCH são limitados a formato texto
- **Múltiplos arquivos**: Faça requisições separadas para cada arquivo

#### **Sessões e Cookies**
- **Manter sessão**: Use `HttpHabilitarCookies` para login automático
- **Segurança**: Desabilite cookies quando não necessários
- **Persistência**: Cookies são mantidos durante toda a sessão do objeto HTTP

#### **Cabeçalhos e Respostas**
- **Content-Type**: Configure corretamente (application/json, application/x-www-form-urlencoded)
- **Leitura de cabeçalhos**: Use `HttpLeCabecalhoResposta` após requisições
- **User-Agent**: Sempre identifique sua aplicação
- **Authorization**: Use Base64Encode para autenticação básica
- **Tokens**: Use Base64Decode para decodificar tokens JWT recebidos

#### **Tratamento de Erros**
- **Controle manual**: Use `HttpDesabilitaErroResposta` para tratar erros manualmente
- **Verificação de status**: Sempre verifique códigos HTTP antes de processar
- **Timeouts**: Configure valores apropriados baseados na velocidade esperada
- **Logs**: Implemente logging adequado para depuração

#### **Performance e Boas Práticas**
- **Timeouts**: Configure sempre para evitar travamentos
- **Reutilização**: Um objeto HTTP pode ser reutilizado para múltiplas requisições
- **Conexões**: LSP gerencia automaticamente o pool de conexões
- **Cache**: Configure cabeçalhos Cache-Control adequadamente

## 🚀 **Exemplos Práticos de APIs**

Esta seção contém exemplos reais de integração com APIs públicas usando as funções HTTP da LSP.

### Exemplo 1: Busca CEP na API ViaCEP

Função completa para buscar informações de CEP usando a API gratuita do ViaCEP.

```lsp
Funcao buscarCepApi(Numero vnCepApi); {
  Definir Alfa vaCepApi;
  Definir Alfa vaHTTP;
  Definir Alfa vaURL;
  Definir Alfa vaJSON;
  Definir Alfa vaCodRes;
  Definir Alfa vaMsgUsu;
  Definir Numero vnCodRes;

  @ Tratamento de Variáveis @
  vaURL = "https://viacep.com.br/ws/__NUMCEP__/json/"; @ URL do ViaCEP @
  vaJSON = ""; @ Objeto de Retorno da Requisição @
  vnCodRes = 0; @ Cód. HTTP Response @

  ConverteMascara(1, vnCepApi, vaCepApi, "99999999");
  TrocaString(vaURL, "__NUMCEP__", vaCepApi);

  @ Cria Objeto HTTP @
  HttpObjeto(vaHTTP);

  @ Desabilita Erro Padrão, evita que mensagens de erros HTTP 4XX/5XX gerem Exceptions em tela ao usuário @
  HttpDesabilitaErroResposta(vaHTTP);

  @ Altera os Cabeçalhos da Requisição @
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept", "application/json;charset=utf-8");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept-Encoding", "gzip, deflate, br");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept-Charset", "utf-8");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Cache-Control", "no-cache");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json;charset=utf-8");
  HttpAlteraCodifCaracPadrao(vaHTTP, "utf-8");

  @ Efetua a Requisição @
  HttpGet(vaHTTP, vaURL, vaJSON);

  @ Verifica Cód. HTTP Response @
  HttpLeCodigoResposta(vaHTTP, vnCodRes);

  @ Se a resposta foi "OK", extrai os dados do JSON @
  Se ((vnCodRes >= 200) e (vnCodRes <= 204)) {
    @ Logradouro @
    ValorElementoJson(vaJSON, "", "logradouro", vaLogradouro);

    @ Complemento @
    ValorElementoJson(vaJSON, "", "complemento", vaComplemento);

    @ Bairro @
    ValorElementoJson(vaJSON, "", "bairro", vaBairro);

    @ Cidade @
    ValorElementoJson(vaJSON, "", "localidade", vaCidadeCep);

    @ Estado @
    ValorElementoJson(vaJSON, "", "uf", vaEstadoCep);

    @ IBGE @
    ValorElementoJson(vaJSON, "", "ibge", vaIbge);
  }

  @ Tratamento de Erro @
  Se ((vnCodRes < 200) ou (vnCodRes >= 300)) {
    @ Tratamento de Variáveis @
    IntParaAlfa(vnCodRes, vaCodRes);

    @ Mensagem @
    vaMsgUsu = "HTTP [" + vaCodRes + "]: Verifique os parâmetros da requisição";
    Mensagem(Retorna, vaMsgUsu);
  }
}
```

### Exemplo 2: Busca Cidade na API IBGE

Função para obter informações de municípios usando a API do IBGE.

```lsp
Funcao buscarCidadeApi(Numero vnCidApi); {
  Definir Alfa vaCidApi;
  Definir Alfa vaHTTP;
  Definir Alfa vaURL;
  Definir Alfa vaJSON;
  Definir Alfa vaCodRes;
  Definir Alfa vaMsgUsu;
  Definir Numero vnCodRes;

  @ Tratamento de Variáveis @
  vaURL = "https://servicodados.ibge.gov.br/api/v1/localidades/municipios/__NUMCID__?view=nivelado"; @ URL do IBGE @
  vaJSON = ""; @ Objeto de Retorno da Requisição @
  vnCodRes = 0; @ Cód. HTTP Response @

  ConverteMascara(1, vnCidApi, vaCidApi, "9999999");
  TrocaString(vaURL, "__NUMCID__", vaCidApi);

  @ Cria Objeto HTTP @
  HttpObjeto(vaHTTP);

  @ Desabilita Erro Padrão, evita que mensagens de erros HTTP 4XX/5XX gerem Exceptions em tela ao usuário @
  HttpDesabilitaErroResposta(vaHTTP);

  @ Altera os Cabeçalhos da Requisição @
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept", "application/json;charset=utf-8");
  @ HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept-Encoding", "gzip, deflate, br"); @
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept-Charset", "utf-8");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Cache-Control", "no-cache");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json;charset=utf-8");
  HttpAlteraCodifCaracPadrao(vaHTTP, "utf-8");

  @ Efetua a Requisição @
  HttpGet(vaHTTP, vaURL, vaJSON);

  @ Verifica Cód. HTTP Response @
  HttpLeCodigoResposta(vaHTTP, vnCodRes);

  @ Se a resposta foi "OK", extrai os dados do JSON @
  Se ((vnCodRes >= 200) e (vnCodRes <= 204)) {
    @ Cidade @
    ValorElementoJson(vaJSON, "", "municipio-nome", vaCidadeRai);

    @ Estado @
    ValorElementoJson(vaJSON, "", "UF-sigla", vaEstadoRai);
  }

  @ Tratamento de Erro @
  Se ((vnCodRes < 200) ou (vnCodRes >= 300)) {
    @ Tratamento de Variáveis @
    IntParaAlfa(vnCodRes, vaCodRes);

    @ Mensagem @
    vaMsgUsu = "HTTP [" + vaCodRes + "]: Verifique os parâmetros da requisição";
    Mensagem(Retorna, vaMsgUsu);
  }
}
```

### 💡 **Características dos Exemplos**

#### **🔧 Exemplo ViaCEP:**
- **Método**: GET
- **Formato**: JSON
- **Encoding**: UTF-8
- **Tratamento**: Erros HTTP e parsing JSON
- **Casos de uso**: Autocompletar endereços, validação de CEP

#### **🌐 Exemplo IBGE:**
- **Método**: GET
- **Formato**: JSON com view nivelada
- **API**: Gratuita e confiável do governo
- **Casos de uso**: Listagem de municípios, dados geográficos

#### **🎯 Boas Práticas Demonstradas:**
1. **Configuração de encoding UTF-8** para caracteres especiais
2. **Desabilitação de erros automáticos** para controle manual
3. **Verificação de códigos de status** antes de processar
4. **Formatação adequada de parâmetros** com ConverteMascara
5. **Tratamento de erros** com mensagens informativas

## 🚀 **Exemplos Práticos de APIs**

Esta seção demonstra operações HTTP essenciais usando APIs reais. Os exemplos são organizados por funcionalidade e incluem autenticação completa.

### 🔧 **CRUD Básico - ReqRes API**

A **ReqRes API** (https://reqres.in) oferece operações CRUD funcionais sem necessidade de autenticação.

#### **GET - Buscar Usuário**

```lsp
Funcao buscarUsuario(Numero vnIdUsuario); {
  Definir Alfa vaHTTP;
  Definir Alfa vaURL;
  Definir Alfa vaJSON;
  Definir Alfa vaId;
  Definir Alfa vaMensagem;
  Definir Alfa vaNome;
  Definir Alfa vaEmail;
  Definir Numero vnCodRes;

  @ Monta URL @
  IntParaAlfa(vnIdUsuario, vaId);
  vaURL = "https://reqres.in/api/users/" + vaId;

  @ Configura requisição @
  HttpObjeto(vaHTTP);
  HttpDesabilitaErroResposta(vaHTTP);
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept", "application/json");

  @ Executa GET @
  HttpGet(vaHTTP, vaURL, vaJSON);
  HttpLeCodigoResposta(vaHTTP, vnCodRes);

  Se (vnCodRes = 200) {
    ValorElementoJson(vaJSON, "data", "first_name", vaNome);
    ValorElementoJson(vaJSON, "data", "email", vaEmail);
    vaMensagem = "✅ Usuário encontrado: " + vaNome + " (" + vaEmail + ")";
    Mensagem(Retorna, vaMensagem);
  } Senao Se (vnCodRes = 404) {
    Mensagem(Retorna, "❌ Usuário não encontrado");
  } Senao {
    IntParaAlfa(vnCodRes, vaId);
    Mensagem(Erro, "❌ Erro na requisição: " + vaId);
  }
}
```

#### **POST - Criar Usuário**

```lsp
@ Variáveis globais para dados do usuário @
Definir Alfa vaNomeUsuario;
Definir Alfa vaCargoUsuario;

@ Exemplo de uso @
vaNomeUsuario = "João Silva";
vaCargoUsuario = "Desenvolvedor";
criarUsuario();

Funcao criarUsuario(); {
  Definir Alfa vaHTTP;
  Definir Alfa vaJSON;
  Definir Alfa vaBody;
  Definir Alfa vaId;
  Definir Alfa vaMensagem;
  Definir Numero vnCodRes;

  @ Monta JSON usando variáveis globais @
  vaBody = "{\"name\": \"" + vaNomeUsuario + "\", \"job\": \"" + vaCargoUsuario + "\"}";

  @ Configura requisição @
  HttpObjeto(vaHTTP);
  HttpDesabilitaErroResposta(vaHTTP);
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json");

  @ Executa POST @
  HttpPost(vaHTTP, "https://reqres.in/api/users", vaBody, vaJSON);
  HttpLeCodigoResposta(vaHTTP, vnCodRes);

  Se (vnCodRes = 201) {
    ValorElementoJson(vaJSON, "", "id", vaId);
    vaMensagem = "✅ Usuário criado! ID: " + vaId;
    Mensagem(Retorna, vaMensagem);
  } Senao {
    IntParaAlfa(vnCodRes, vaId);
    Mensagem(Erro, "❌ Erro ao criar: " + vaId);
  }
}
```

#### **PUT - Atualizar Completo**

```lsp
@ Variáveis globais para atualização @
Definir Numero vnIdUsuario;
Definir Alfa vaNomeAtualizar;
Definir Alfa vaCargoAtualizar;

@ Exemplo de uso @
vnIdUsuario = 2;
vaNomeAtualizar = "João Santos";
vaCargoAtualizar = "Analista Senior";
atualizarUsuario();

Funcao atualizarUsuario(); {
  Definir Alfa vaHTTP;
  Definir Alfa vaURL;
  Definir Alfa vaJSON;
  Definir Alfa vaBody;
  Definir Alfa vaIdStr;
  Definir Numero vnCodRes;

  IntParaAlfa(vnIdUsuario, vaIdStr);
  vaURL = "https://reqres.in/api/users/" + vaIdStr;
  vaBody = "{\"name\": \"" + vaNomeAtualizar + "\", \"job\": \"" + vaCargoAtualizar + "\"}";

  HttpObjeto(vaHTTP);
  HttpDesabilitaErroResposta(vaHTTP);
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json");

  @ PUT substitui recurso completo @
  HttpPut(vaHTTP, vaURL, vaBody, vaJSON);
  HttpLeCodigoResposta(vaHTTP, vnCodRes);

  Se (vnCodRes = 200) {
    Mensagem(Retorna, "✅ Usuário " + vaIdStr + " atualizado completamente");
  } Senao {
    IntParaAlfa(vnCodRes, vaIdStr);
    Mensagem(Erro, "❌ Erro ao atualizar: " + vaIdStr);
  }
}

@ Exemplo de uso @
vnIdUsuario = 2;
vaNomeAtualizar = "João Santos";
vaCargoAtualizar = "Analista Senior";
atualizarUsuario();
```

#### **PATCH - Atualizar Parcial**

```lsp
@ Variáveis globais para PATCH @
Definir Numero vnIdCargo;
Definir Alfa vaNovoCargo;

@ Exemplo de uso @
vnIdCargo = 2;
vaNovoCargo = "Tech Lead";
atualizarCargo();

Funcao atualizarCargo(); {
  Definir Alfa vaHTTP;
  Definir Alfa vaURL;
  Definir Alfa vaJSON;
  Definir Alfa vaBody;
  Definir Alfa vaIdStr;
  Definir Numero vnCodRes;

  IntParaAlfa(vnIdCargo, vaIdStr);
  vaURL = "https://reqres.in/api/users/" + vaIdStr;
  vaBody = "{\"job\": \"" + vaNovoCargo + "\"}"; @ Apenas o campo alterado @

  HttpObjeto(vaHTTP);
  HttpDesabilitaErroResposta(vaHTTP);
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json");

  @ PATCH modifica apenas campos específicos @
  HttpPatch(vaHTTP, vaURL, vaBody, vaJSON);
  HttpLeCodigoResposta(vaHTTP, vnCodRes);

  Se (vnCodRes = 200) {
    Mensagem(Retorna, "✅ Cargo atualizado para: " + vaNovoCargo);
  } Senao {
    IntParaAlfa(vnCodRes, vaIdStr);
    Mensagem(Erro, "❌ Erro ao atualizar cargo: " + vaIdStr);
  }
}

@ Exemplo de uso @
vnIdCargo = 2;
vaNovoCargo = "Tech Lead";
atualizarCargo();
```

#### **DELETE - Excluir Usuário**

```lsp
Funcao excluirUsuario(Numero vnId); {
  Definir Alfa vaHTTP;
  Definir Alfa vaURL;
  Definir Alfa vaJSON;
  Definir Alfa vaIdStr;
  Definir Numero vnCodRes;

  IntParaAlfa(vnId, vaIdStr);
  vaURL = "https://reqres.in/api/users/" + vaIdStr;

  HttpObjeto(vaHTTP);
  HttpDesabilitaErroResposta(vaHTTP);

  HttpDelete(vaHTTP, vaURL, vaJSON);
  HttpLeCodigoResposta(vaHTTP, vnCodRes);

  Se (vnCodRes = 204) {
    Mensagem(Retorna, "✅ Usuário " + vaIdStr + " excluído com sucesso");
  } Senao {
    IntParaAlfa(vnCodRes, vaIdStr);
    Mensagem(Erro, "❌ Erro ao excluir: " + vaIdStr);
  }
}
```

### 🔐 **Autenticação Basic Auth - HTTPBin**

Demonstra autenticação básica real usando usuário e senha.

```lsp
@ Variáveis globais para Basic Auth @
Definir Alfa vaUsuarioAuth;
Definir Alfa vaSenhaAuth;

@ Exemplo de uso @
vaUsuarioAuth = "admin";
vaSenhaAuth = "senha123";
testarBasicAuth();

Funcao testarBasicAuth(); {
  Definir Alfa vaHTTP;
  Definir Alfa vaURL;
  Definir Alfa vaJSON;
  Definir Alfa vaCredenciais;
  Definir Alfa vaAuth;
  Definir Alfa vaUsuarioRetornado;
  Definir Numero vnCodRes;

  @ Monta URL com credenciais @
  vaURL = "https://httpbin.org/basic-auth/" + vaUsuarioAuth + "/" + vaSenhaAuth;

  @ Gera header Authorization @
  vaCredenciais = vaUsuarioAuth + ":" + vaSenhaAuth;
  Base64Encode(vaCredenciais, vaAuth);
  vaAuth = "Basic " + vaAuth;

  @ Configura requisição @
  HttpObjeto(vaHTTP);
  HttpDesabilitaErroResposta(vaHTTP);
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", vaAuth);

  @ Executa requisição @
  HttpGet(vaHTTP, vaURL, vaJSON);
  HttpLeCodigoResposta(vaHTTP, vnCodRes);

  Se (vnCodRes = 200) {
    ValorElementoJson(vaJSON, "", "user", vaUsuarioRetornado);
    Mensagem(Retorna, "✅ Autenticação Basic Auth: " + vaUsuarioRetornado);
  } Senao Se (vnCodRes = 401) {
    Mensagem(Retorna, "❌ Credenciais inválidas - 401 Unauthorized");
  } Senao {
    IntParaAlfa(vnCodRes, vaAuth);
    Mensagem(Erro, "❌ Erro inesperado: " + vaAuth);
  }
}

@ Exemplo de uso @
vaUsuarioAuth = "admin";
vaSenhaAuth = "senha123";
testarBasicAuth();
```

### 🎫 **Autenticação Bearer Token - HTTPBin**

Demonstra autenticação com token Bearer.

```lsp
@ Variável global para Bearer Token @
Definir Alfa vaTokenBearer;

@ Exemplo de uso @
vaTokenBearer = "meu-token-secreto";
testarBearerToken();

Funcao testarBearerToken(); {
  Definir Alfa vaHTTP;
  Definir Alfa vaJSON;
  Definir Alfa vaAuth;
  Definir Alfa vaTokenRetornado;
  Definir Numero vnCodRes;

  @ Monta header Authorization @
  vaAuth = "Bearer " + vaTokenBearer;

  @ Configura requisição @
  HttpObjeto(vaHTTP);
  HttpDesabilitaErroResposta(vaHTTP);
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", vaAuth);

  @ Executa requisição @
  HttpGet(vaHTTP, "https://httpbin.org/bearer", vaJSON);
  HttpLeCodigoResposta(vaHTTP, vnCodRes);

  Se (vnCodRes = 200) {
    ValorElementoJson(vaJSON, "", "token", vaTokenRetornado);
    Mensagem(Retorna, "✅ Autenticação Bearer: " + vaTokenRetornado);
  } Senao Se (vnCodRes = 401) {
    Mensagem(Retorna, "❌ Token inválido - 401 Unauthorized");
  } Senao {
    IntParaAlfa(vnCodRes, vaAuth);
    Mensagem(Erro, "❌ Erro inesperado: " + vaAuth);
  }
}

@ Exemplo de uso @
vaTokenBearer = "meu-token-secreto";
testarBearerToken();
```

### 🔑 **Fluxo Completo: Login + Token + CRUD**

Exemplo completo simulando login para obter token e usar em operações subsequentes.

```lsp
Funcao exemploFluxoCompleto(); {
  Definir Alfa vaHTTP;
  Definir Alfa vaJSON;
  Definir Alfa vaBody;
  Definir Alfa vaToken;
  Definir Alfa vaAuth;
  Definir Numero vnCodRes;

  HttpObjeto(vaHTTP);
  HttpDesabilitaErroResposta(vaHTTP);

  @ 1. LOGIN - Simula obtenção de token @
  vaBody = "{\"email\": \"eve.holt@reqres.in\", \"password\": \"cityslicka\"}";
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json");
  
  HttpPost(vaHTTP, "https://reqres.in/api/login", vaBody, vaJSON);
  HttpLeCodigoResposta(vaHTTP, vnCodRes);

  Se (vnCodRes = 200) {
    @ Extrai token @
    ValorElementoJson(vaJSON, "", "token", vaToken);
    Mensagem(Retorna, "✅ Login realizado! Token: " + vaToken);

    @ 2. USA TOKEN - Em requisição subsequente @
    vaAuth = "Bearer " + vaToken;
    HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", vaAuth);

    @ 3. OPERAÇÃO AUTENTICADA - Buscar usuários @
    HttpGet(vaHTTP, "https://reqres.in/api/users?page=1", vaJSON);
    HttpLeCodigoResposta(vaHTTP, vnCodRes);

    Se (vnCodRes = 200) {
      Mensagem(Retorna, "✅ Dados obtidos com token de autenticação!");
    } Senao {
      Mensagem(Erro, "❌ Erro ao usar token autenticado");
    }
  } Senao {
    Mensagem(Erro, "❌ Falha no login");
  }
}
```

### 📋 **Exemplos de Uso**

```lsp
@ CRUD Básico @
buscarUsuario(2);

vaNomeUsuario = "João Silva";
vaCargoUsuario = "Desenvolvedor";
criarUsuario();

vnIdUsuario = 2;
vaNomeAtualizar = "João Santos";
vaCargoAtualizar = "Analista Senior";
atualizarUsuario();

vnIdCargo = 2;
vaNovoCargo = "Tech Lead";
atualizarCargo();

excluirUsuario(2);

@ Autenticação @
vaUsuarioAuth = "admin";
vaSenhaAuth = "senha123";
testarBasicAuth();

vaTokenBearer = "meu-token-secreto";
testarBearerToken();

@ Fluxo completo @
exemploFluxoCompleto();
```

### ✅ **Resumo das APIs Utilizadas**

| API | Funcionalidade | Autenticação | Status |
|-----|---------------|--------------|--------|
| **ReqRes** | CRUD completo funcional | ❌ Não requer | ✅ Real |
| **HTTPBin Basic** | Teste Basic Auth | ✅ user:pass | ✅ Real |
| **HTTPBin Bearer** | Teste Bearer Token | ✅ Bearer token | ✅ Real |

**💡 Vantagens desta abordagem:**
- 🎯 **Foco didático**: Um exemplo claro de cada conceito
- ✅ **Funcionalidade real**: Todas as operações funcionam de verdade
- 🔐 **Autenticação completa**: Basic Auth e Bearer Token reais
- 📚 **Progressão lógica**: Do básico ao avançado
