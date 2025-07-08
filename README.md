# Documentação da Linguagem LSP - Linguagem Sênior de Programação

[![Senior Sistemas](https://img.shields.io/badge/Senior-Sistemas-blue)](https://www.senior.com.br)
[![LSP](https://img.shields.io/badge/Linguagem-LSP-green)](https://documentacao.senior.com.br/tecnologia)
[![Status](https://img.shields.io/badge/Status-Ativo-brightgreen)]()

> **Documentação Oficial:** <https://documentacao.senior.com.br/tecnologia>

---

## 🚀 **Início Rápido**

### **Primeiro Programa LSP**
```lsp
@ Meu primeiro programa em LSP @
Definir Alfa vaMensagem;
vaMensagem = "Olá, mundo LSP!";
Mensagem(Retorna, vaMensagem);
```

### **Conceitos Fundamentais**
- **Case Insensitive**: `vaNome` = `VANOME` = `vanome`
- **Terminador obrigatório**: Toda linha termina com `;`
- **Comentários**: `@ uma linha @` ou `/* múltiplas linhas */`
- **Identação**: 2 espaços (padrão Senior)

### **Tipos de Dados Essenciais**
```lsp
Definir Alfa vaNome;        @ Texto/String @
Definir Numero vnIdade;     @ Número (int/decimal) @
Definir Data vdNascimento;  @ Data @
```

### **⚠️ Lembre-se Sempre**
1. **Não concatene dentro de parâmetros de funções**
2. **Use variáveis intermediárias para conversões**
3. **Siga o padrão de nomenclatura (va, vn, vd)**

---

## 📖 **Índice Completo**

### **🎯 Fundamentos**
- [Introdução](#introdução)
- [Sintaxe e Estrutura](#sintaxe-e-estrutura)
- [Comentários](#comentários)
- [Palavras Reservadas](#palavras-reservadas)
- [Variáveis de Sistema](#variáveis-de-sistema)
- [Operadores](#operadores)

### **📊 Dados e Variáveis**
- [Tipo de Dados e Variáveis](#tipo-de-dados-e-variáveis)
- [Definição de Arrays](#definição-de-arrays)
- [Definição de Tabelas](#definição-de-tabelas)
### **🔧 Manipulação de Dados**
- [Manipulação Avançada de Strings](#manipulação-avançada-de-strings)
- [Manipulação Avançada de Datas](#manipulação-avançada-de-datas)
- [Manipulação Dinâmica de Variáveis](#manipulação-dinâmica-de-variáveis)
- [Cast de Variável](#cast-de-variável)

### **🔒 Segurança e Validação**
- [Criptografia e Segurança](#criptografia-e-segurança)
- [Validação e Verificação](#validação-e-verificação)

### **🧮 Operações e Cálculos**
- [Operações Numéricas Avançadas](#operações-numéricas-avançadas)

### **🎮 Controle de Fluxo**
- [Controle de Fluxo](#controle-de-fluxo)
- [Definição de Funções](#definição-de-funções)

### **🗃️ Banco de Dados**
- [Definição de Cursor](#definição-de-cursor)
- [Funções SQL](#funções-sql)
- [Funções de Lista de Regras](#funções-de-lista-de-regras)

### **🌐 Integração e APIs**
- [Manipulação de Arquivos](#manipulação-de-arquivos)
- [Chamada de Web Service](#chamada-de-web-service)
- [Chamada HTTP](#chamada-http)
- [🚀 Exemplos Práticos de APIs](#-exemplos-práticos-de-apis)

### **🎨 Interface do Usuário**
- [Interface e Feedback do Usuário](#interface-e-feedback-do-usuário)
- [Mensagens](#mensagens)
- [Cancel](#cancel)

### **📋 Referência e Boas Práticas**
- [Funções Gerais](#funções-gerais)
- [Padrões e Boas Práticas](#padrões-e-boas-práticas)
- [⚠️ LIMITAÇÕES CRÍTICAS DA LSP](#️-limitações-críticas-da-lsp)
- [🚨 Erros Comuns e Soluções](#️-erros-comuns-e-soluções)
- [🎯 Padrões de Projeto LSP](#️-padrões-de-projeto-lsp)
- [🔍 Debugging e Troubleshooting](#️-debugging-e-troubleshooting)
- [🎓 Exercícios Práticos por Nível](#️-exercícios-práticos-por-nível)
- [🎯 Quick Reference Cards](#️-quick-reference-cards)
- [🎯 Casos de Uso Reais Detalhados](#️-casos-de-uso-reais-detalhados)

---

## 🎯 **Guia de Aprendizado Progressivo**

### **📖 Nível 1: Iniciante (Conceitos Básicos)**
1. **Primeiro**: [Sintaxe e Estrutura](#sintaxe-e-estrutura) - Aprenda a sintaxe básica
2. **Segundo**: [Tipo de Dados e Variáveis](#tipo-de-dados-e-variáveis) - Entenda os tipos de dados
3. **Terceiro**: [Operadores](#operadores) - Domine os operadores
4. **Quarto**: [Controle de Fluxo](#controle-de-fluxo) - Aprenda if/else e loops
5. **Quinto**: [Mensagens](#mensagens) - Saiba como exibir mensagens

### **🚀 Nível 2: Intermediário (Funcionalidades Essenciais)**
1. **Sexto**: [Manipulação Avançada de Strings](#manipulação-avançada-de-strings) - Manipule textos
2. **Sétimo**: [Manipulação Avançada de Datas](#manipulação-avançada-de-datas) - Trabalhe com datas
3. **Oitavo**: [Definição de Funções](#definição-de-funções) - Crie suas próprias funções
4. **Nono**: [Validação e Verificação](#validação-e-verificação) - Valide dados
5. **Décimo**: [Cast de Variável](#cast-de-variável) - Converta entre tipos

### **⚡ Nível 3: Avançado (Recursos Especializados)**
1. **Décimo primeiro**: [Definição de Cursor](#definição-de-cursor) - Acesse bancos de dados
2. **Décimo segundo**: [Funções SQL](#funções-sql) - Execute SQL diretamente
3. **Décimo terceiro**: [Chamada HTTP](#chamada-http) - Integre com APIs
4. **Décimo quarto**: [Criptografia e Segurança](#criptografia-e-segurança) - Proteja dados
5. **Décimo quinto**: [🚀 Exemplos Práticos de APIs](#-exemplos-práticos-de-apis) - Exemplos reais

## 🔍 **Debugging e Troubleshooting**

### **🐛 Problemas Comuns e Soluções**

#### **Problema: "Variável não definida"**
**Causa:** Variável declarada dentro de bloco condicional ou não declarada
**Solução:** Declare todas as variáveis no início da regra
```lsp
@ ❌ INCORRETO @
Se (vnCondicao = 1) {
  Definir Alfa vaVariavel;  @ Declaração no meio @
  vaVariavel = "valor";
}

@ ✅ CORRETO @
Definir Alfa vaVariavel;  @ Declaração no início @
Se (vnCondicao = 1) {
  vaVariavel = "valor";
}
```

#### **Problema: "Função não funciona"**
**Causa:** Parâmetros incorretos ou ordem errada
**Solução:** Verifique a documentação da função
```lsp
@ ❌ INCORRETO @
TamanhoAlfa(vnTamanho, vaTexto);  @ Ordem errada @

@ ✅ CORRETO @
TamanhoAlfa(vaTexto, vnTamanho);  @ Ordem correta @
```

#### **Problema: "Comparação com função sem retorno"**
**Causa:** Tentar comparar função que usa parâmetro de retorno
**Solução:** Execute a função primeiro, depois compare a variável
```lsp
@ ❌ INCORRETO @
Se (EstaNulo(vaDado, vnEhNulo) = 0) {  @ Função não retorna valor @

@ ✅ CORRETO @
EstaNulo(vaDado, vnEhNulo);  @ Executa função primeiro @
Se (vnEhNulo = 0) {          @ Compara variável preenchida @
```

#### **Problema: "Erro de tipo"**
**Causa:** Tentativa de atribuir tipo incorreto
**Solução:** Use funções de conversão apropriadas
```lsp
@ ❌ INCORRETO @
Definir Numero vnValor;
vnValor = "123";  @ String em número @

@ ✅ CORRETO @
Definir Numero vnValor;
Definir Alfa vaTexto;
vaTexto = "123";
AlfaParaInt(vaTexto, vnValor);
```

#### **Problema: "Loop infinito"**
**Causa:** Condição de parada nunca atingida
**Solução:** Verifique a lógica da condição e atualize variáveis de controle
```lsp
@ ❌ INCORRETO @
vnContador = 1;
Enquanto (vnContador > 0) {
  @ Processamento sem incrementar @
}

@ ✅ CORRETO @
vnContador = 1;
Enquanto (vnContador <= 10) {
  @ Processamento @
  vnContador++;  @ Incrementa controle @
}
```

#### **Problema: "Função não funciona"**
**Causa:** Parâmetros incorretos ou ordem errada
**Solução:** Verifique a documentação da função
```lsp
@ ❌ INCORRETO @
TamanhoAlfa(vnTamanho, vaTexto);  @ Ordem errada @

@ ✅ CORRETO @
TamanhoAlfa(vaTexto, vnTamanho);  @ Ordem correta @
```

### **🔧 Técnicas de Debugging**

#### **Técnica 1: Mensagens de Debug**
```lsp
@ Adicione mensagens para rastrear execução @
Definir Alfa vaDebug;
vaDebug = "Passo 1: Iniciando processamento";
Mensagem(Retorna, vaDebug);

@ ... código ... @

vaDebug = "Passo 2: Dados processados";
Mensagem(Retorna, vaDebug);
```

#### **Técnica 2: Validação de Dados**
```lsp
@ Sempre valide dados antes de processar @
EstaNulo(vaDado, vnEhNulo);
Se (vnEhNulo = 0) {
  TamanhoAlfa(vaDado, vnTamanho);
  Se (vnTamanho > 0) {
    @ Processa apenas se válido @
    Mensagem(Retorna, "Dado válido: " + vaDado);
  } Senao {
    Mensagem(Erro, "Dado vazio");
  }
} Senao {
  Mensagem(Erro, "Dado nulo");
}
```

#### **Técnica 3: Tratamento de Erros**
```lsp
@ Use estruturas try-catch equivalentes @
Se (operacaoCritica() = 1) {
  @ Sucesso @
  processarResultado();
} Senao {
  @ Falha @
  Mensagem(Erro, "Operação falhou");
  @ Log do erro @
  registrarErro();
}
```

## 🎓 **Exercícios Práticos por Nível**

### **📖 Nível 1: Exercícios Básicos**

#### **🔢 Exercício 1: Calculadora Simples**
**Objetivo:** Criar uma calculadora que soma dois números
**Conceitos:** Variáveis, operadores, conversões, mensagens

```lsp
@ Calculadora Simples @
Definir Numero vnNumero1;
Definir Numero vnNumero2;
Definir Numero vnResultado;
Definir Alfa vaResultadoStr;
Definir Alfa vaMensagem;

vnNumero1 = 10;
vnNumero2 = 20;
vnResultado = vnNumero1 + vnNumero2;

IntParaAlfa(vnResultado, vaResultadoStr);
vaMensagem = "Resultado: " + vaResultadoStr;
Mensagem(Retorna, vaMensagem);
```

#### **📝 Exercício 2: Validador de Nome**
**Objetivo:** Validar se um nome tem pelo menos 3 caracteres
**Conceitos:** Validação, condicionais, funções de string

```lsp
@ Validador de Nome @
Definir Alfa vaNome;
Definir Numero vnTamanho;
Definir Numero vnEhNulo;

vaNome = "João";
EstaNulo(vaNome, vnEhNulo);

Se (vnEhNulo = 0) {
  TamanhoAlfa(vaNome, vnTamanho);
  Se (vnTamanho >= 3) {
    Mensagem(Retorna, "Nome válido!");
  } Senao {
    Mensagem(Erro, "Nome deve ter pelo menos 3 caracteres");
  }
} Senao {
  Mensagem(Erro, "Nome não pode ser nulo");
}
```

### **🚀 Nível 2: Exercícios Intermediários**

#### **🏷️ Exercício 3: Formatador de CPF**
**Objetivo:** Remover pontos e traços de um CPF
**Conceitos:** Manipulação de strings, loops, funções avançadas

```lsp
@ Formatador de CPF @
Definir Alfa vaCPF;
Definir Numero vnPosicao;

vaCPF = "123.456.789-10";

@ Remove pontos @
DeletarAlfa(vaCPF, 4, 1);
DeletarAlfa(vaCPF, 7, 1);
DeletarAlfa(vaCPF, 10, 1);

Mensagem(Retorna, "CPF limpo: " + vaCPF);
```

#### **📅 Exercício 4: Calculadora de Idade**
**Objetivo:** Calcular idade a partir da data de nascimento
**Conceitos:** Datas, operações aritméticas, validação

```lsp
@ Calculadora de Idade @
Definir Data vdDataNascimento;
Definir Data vdDataAtual;
Definir Numero vnAnoNascimento;
Definir Numero vnAnoAtual;
Definir Numero vnIdade;
Definir Alfa vaIdadeStr;
Definir Alfa vaMensagem;

@ Define data de nascimento (exemplo: 15/08/1990) @
MontaData(15, 8, 1990, vdDataNascimento);
DataHoje(vdDataAtual);

@ Extrai anos @
Definir Numero vnDia;
Definir Numero vnMes;
DecodData(vdDataNascimento, vnDia, vnMes, vnAnoNascimento);
DecodData(vdDataAtual, vnDia, vnMes, vnAnoAtual);

@ Calcula idade @
vnIdade = vnAnoAtual - vnAnoNascimento;

IntParaAlfa(vnIdade, vaIdadeStr);
vaMensagem = "Idade: " + vaIdadeStr + " anos";
Mensagem(Retorna, vaMensagem);
```

### **⚡ Nível 3: Exercícios Avançados**

#### **🌐 Exercício 5: Validador de Email**
**Objetivo:** Validar formato básico de email
**Conceitos:** Manipulação de strings, validação complexa

```lsp
@ Validador de Email @
Definir Alfa vaEmail;
Definir Numero vnPosArroba;
Definir Numero vnPosPonto;
Definir Numero vnTamanho;
Definir Numero vnEhNulo;

vaEmail = "usuario@empresa.com.br";

@ Verifica se não é nulo @
EstaNulo(vaEmail, vnEhNulo);
Se (vnEhNulo = 1) {
  Mensagem(Erro, "Email não pode ser nulo");
  Cancel(1);
}

@ Verifica se tem @ @
PosicaoAlfa("@", vaEmail, vnPosArroba);
Se (vnPosArroba = 0) {
  Mensagem(Erro, "Email deve conter @");
  Cancel(1);
}

@ Verifica se tem ponto após @ @
TamanhoAlfa(vaEmail, vnTamanho);
CopiarAlfa(vaEmail, vnPosArroba + 1, vnTamanho - vnPosArroba);
PosicaoAlfa(".", vaEmail, vnPosPonto);
Se (vnPosPonto <= vnPosArroba) {
  Mensagem(Erro, "Email deve conter ponto após @");
  Cancel(1);
}

Mensagem(Retorna, "Email válido!");
```

#### **📊 Exercício 6: Processador de Lista CSV**
**Objetivo:** Processar uma lista separada por vírgulas
**Conceitos:** Listas, loops, funções de lista

```lsp
@ Processador de Lista CSV @
Definir Alfa vaLista;
Definir Alfa vaItem;
Definir Numero vnQuantidade;
Definir Numero vnContador;

vaLista = "João,Maria,Pedro,Ana";

@ Conta itens @
ListaQuantidade(vaLista, ",", vnQuantidade);

@ Processa cada item @
Para (vnContador = 1; vnContador <= vnQuantidade; vnContador++) {
  ListaItem(vaLista, ",", vnContador, vaItem);
  Mensagem(Retorna, "Item " + vaItem + " processado");
}
```

---

## ⚠️ **Avisos Importantes para Iniciantes**

### 🚫 **Limitação #1: Parâmetros de Funções**
```lsp
@ NUNCA FAÇA - NÃO FUNCIONA @
Mensagem(Retorna, "Resultado: " + vaValor);

@  SEMPRE FAÇA - FUNCIONA @
Definir Alfa vaMensagem;
vaMensagem = "Resultado: " + vaValor;
Mensagem(Retorna, vaMensagem);
```

### 📤 **Limitação #2: Funções Usam Parâmetros de Retorno**
```lsp
@ INCORRETO @
vnTamanho = TamanhoAlfa(vaTexto);

@  CORRETO @
TamanhoAlfa(vaTexto, vnTamanho);
```

### 🏷️ **Regra #3: Padrão de Nomenclatura**
```lsp
Definir Alfa vaNome;     @ va = variável alfa @
Definir Numero vnIdade;  @ vn = variável numero @
Definir Data vdData;     @ vd = variável data @
```

### 🔧 **Regra #4: Grids Precisam de Variáveis Intermediárias**
```lsp
@ INCORRETO @
AlfaParaDecimal(vaTexto, MinhaGrid.CampoDecimal);

@  CORRETO @
Definir Numero vnValor;
AlfaParaDecimal(vaTexto, vnValor);
MinhaGrid.CampoDecimal = vnValor;
```

## 🚨 **Erros Comuns e Soluções**

### **⚠️ AVISO IMPORTANTE: Problemas de Sintaxe Corrigidos**

#### **❌ Problema #1: Função `Chr()` Inexistente**
**Problema:** A função `Chr()` não existe na LSP
```lsp
@ ❌ INCORRETO @
vaStrProcura = "Primeira linha" + Chr(13) + Chr(10) + "Segunda linha";
```

**Solução:** Use `CaracterParaAlfa()` para caracteres especiais
```lsp
@ ✅ CORRETO @
Definir Alfa vaEnter;
CaracterParaAlfa(13, vaEnter);
vaStrProcura = "Primeira linha" + vaEnter + "Segunda linha";
```

#### **❌ Problema #2: `FormatarData` com Tipo Data**
**Problema:** `FormatarData` aceita apenas tipo `Numero`, não `Data`
```lsp
@ ❌ INCORRETO @
DataHoje(vdData);
FormatarData(vdData, "dd/MM/yyyy", vaFormatada);
```

**Solução:** Use `DataHora()` que retorna `Numero`
```lsp
@ ✅ CORRETO @
Definir Numero vnDataHora;
DataHora(vnDataHora);
FormatarData(vnDataHora, "dd/MM/yyyy", vaFormatada);
```

#### **❌ Problema #3: Atribuição Direta de Data**
**Problema:** Não é possível atribuir data diretamente
```lsp
@ ❌ INCORRETO @
vdData = 15/08/1990;
```

**Solução:** Use `MontaData()` ou `CodData()`
```lsp
@ ✅ CORRETO @
MontaData(15, 8, 1990, vdData);
```

#### **❌ Problema #4: Variáveis Não Declaradas**
**Problema:** Variáveis usadas sem declaração
```lsp
@ ❌ INCORRETO @
DecodData(vdData, vnDia, vnMes, vnAno);
```

**Solução:** Declare todas as variáveis
```lsp
@ ✅ CORRETO @
Definir Numero vnDia;
Definir Numero vnMes;
Definir Numero vnAno;
DecodData(vdData, vnDia, vnMes, vnAno);
```

#### **❌ Problema #5: Função `Truncar` Inexistente**
**Problema:** A função `Truncar` não existe na LSP
```lsp
@ ❌ INCORRETO @
vnParteInteira = Truncar(vnDataHora);
```

**Solução:** Use conversão para inteiro ou outras funções
```lsp
@ ✅ CORRETO @
vnParteInteira = vnDataHora;  @ Conversão implícita @
```

### **❌ Erro #1: Concatenação em Parâmetros de Funções**
**Problema:** Tentar concatenar strings diretamente nos parâmetros
```lsp
@ ❌ INCORRETO - NÃO FUNCIONA @
Mensagem(Retorna, "Resultado: " + vaValor);
TamanhoAlfa("Texto: " + vaNome, vnTamanho);
```

**Solução:** Sempre use variáveis intermediárias
```lsp
@ ✅ CORRETO - FUNCIONA @
Definir Alfa vaMensagem;
vaMensagem = "Resultado: " + vaValor;
Mensagem(Retorna, vaMensagem);

Definir Alfa vaTextoCompleto;
vaTextoCompleto = "Texto: " + vaNome;
TamanhoAlfa(vaTextoCompleto, vnTamanho);
```

### **❌ Erro #2: Confundir Tipos de Retorno**
**Problema:** Tentar usar funções LSP como se retornassem valores
```lsp
@ ❌ INCORRETO - NÃO FUNCIONA @
vnTamanho = TamanhoAlfa(vaTexto);
vaResultado = IntParaAlfa(vnNumero);
Se (EstaNulo(vaDado, vnEhNulo) = 0) {  @ Função não retorna valor @
```

**Solução:** LSP usa parâmetros de retorno
```lsp
@ ✅ CORRETO - FUNCIONA @
TamanhoAlfa(vaTexto, vnTamanho);
IntParaAlfa(vnNumero, vaResultado);
EstaNulo(vaDado, vnEhNulo);  @ Executa função primeiro @
Se (vnEhNulo = 0) {          @ Depois compara variável @
```

### **❌ Erro #3: Declaração de Variáveis no Meio do Código**
**Problema:** Declarar variáveis dentro de blocos condicionais
```lsp
@ ❌ INCORRETO - PODE CAUSAR ERROS @
Se (vnCondicao = 1) {
  Definir Alfa vaVariavel;  @ Declaração no meio do código @
  vaVariavel = "valor";
}
```

**Solução:** Declare todas as variáveis no início da regra
```lsp
@ ✅ CORRETO - SEMPRE FUNCIONA @
Definir Alfa vaVariavel;  @ Declaração no início @

Se (vnCondicao = 1) {
  vaVariavel = "valor";
}
```

### **❌ Erro #4: Confundir Tipos de Dados**
**Problema:** Tentar atribuir tipos incompatíveis
```lsp
@ ❌ INCORRETO - ERRO DE TIPO @
Definir Numero vnValor;
vnValor = "123";  @ Tentando atribuir string a número @
```

**Solução:** Use conversões apropriadas
```lsp
@ ✅ CORRETO - CONVERSÃO ADEQUADA @
Definir Numero vnValor;
Definir Alfa vaTexto;
vaTexto = "123";
AlfaParaInt(vaTexto, vnValor);
```

### **❌ Erro #5: Loop Infinito**
**Problema:** Condição de parada nunca é atingida
```lsp
@ ❌ INCORRETO - LOOP INFINITO @
vnContador = 1;
Enquanto (vnContador > 0) {
  @ Processamento sem incrementar vnContador @
}
```

**Solução:** Sempre atualize a variável de controle
```lsp
@ ✅ CORRETO - LOOP CONTROLADO @
vnContador = 1;
Enquanto (vnContador <= 10) {
  @ Processamento @
  vnContador++;  @ Incrementa a variável de controle @
}
```

## 🎯 **Padrões de Projeto LSP**

### **📋 Padrão: Validação de Dados**
```lsp
@ Sempre valide antes de processar @
Definir Funcao validarDados();

Funcao validarDados(); {
  @ 1. Verifica se não é nulo @
  EstaNulo(vaDado, vnEhNulo);
  Se (vnEhNulo = 0) {
    @ 2. Verifica se não é vazio @
    TamanhoAlfa(vaDado, vnTamanho);
    Se (vnTamanho > 0) {
      @ 3. Processa apenas se válido @
      @ ... lógica de processamento ... @
    } Senao {
      Mensagem(Erro, "Dado não pode ser vazio");
    }
  } Senao {
    Mensagem(Erro, "Dado não pode ser nulo");
  }
}
```

### **🔄 Padrão: Conversão Segura**
```lsp
@ Sempre use variáveis intermediárias para conversões @
Definir Funcao converterSeguro();

Funcao converterSeguro(); {
  @ 1. Declara variáveis intermediárias @
  Definir Numero vnValor;
  Definir Alfa vaValorStr;
  Definir Alfa vaMensagem;
  
  @ 2. Faz a conversão @
  AlfaParaInt(vaTexto, vnValor);
  
  @ 3. Converte para exibição @
  IntParaAlfa(vnValor, vaValorStr);
  
  @ 4. Monta mensagem @
  vaMensagem = "Valor convertido: " + vaValorStr;
  
  @ 5. Exibe resultado @
  Mensagem(Retorna, vaMensagem);
}
```

### **🔍 Padrão: Tratamento de Erros**
```lsp
@ Sempre trate erros de forma estruturada @
Definir Funcao processarComTratamento();

Funcao processarComTratamento(); {
  @ 1. Tenta a operação @
  Se (operacaoCritica() = 1) {
    @ 2. Sucesso - processa resultado @
    processarResultado();
  } Senao {
    @ 3. Falha - registra erro e notifica @
    registrarErro();
    Mensagem(Erro, "Operação falhou. Verifique os dados.");
  }
}
```

## Introdução

A Linguagem Senior de Programação (LSP) é uma linguagem proprietária utilizada nos sistemas da Senior para a customização e extensão de funcionalidades. Ela permite a manipulação de dados, a criação de regras de negócio personalizadas e a automação de processos dentro do ambiente Senior.

Diferente de linguagens tradicionais como Java, C# ou Python, a LSP foi projetada especificamente para interagir com os sistemas Senior, possuindo sintaxe e estrutura próprias. Seu uso é essencial para desenvolvedores que desejam criar soluções personalizadas dentro da plataforma.

### **🎯 Características Principais da LSP**

- **🏢 Integração Nativa**: Desenvolvida especificamente para o ecossistema Senior
- **📝 Sintaxe Simples**: Fácil de aprender para quem conhece programação básica
- **🔄 Case Insensitive**: Não diferencia maiúsculas de minúsculas
- **💾 Tipagem Específica**: Tipos otimizados para dados empresariais
- **🚀 Execução Direta**: Roda diretamente no ambiente Senior

### **📚 Como Usar Esta Documentação**

1. **Iniciantes**: Comece pelo [Guia de Aprendizado Progressivo](#-guia-de-aprendizado-progressivo)
2. **Experientes**: Use o [Índice Completo](#-índice-completo) para navegação rápida
3. **Referência**: Consulte [Funções Gerais](#funções-gerais) para encontrar funções específicas
4. **Práticos**: Veja [Exemplos Práticos de APIs](#-exemplos-práticos-de-apis) para casos reais

## 🧠 **Conceitos Mentais Importantes**

### **💭 Modelo Mental #1: "Parâmetros de Retorno"**
**Pense assim:** Em LSP, as funções **não retornam valores**, elas **preenchem variáveis** que você passa como parâmetro.

**Analogia:** É como dar um formulário para alguém preencher, em vez de receber uma resposta direta.

**Exemplo:**
```lsp
@ ❌ Pensamento INCORRETO (estilo outras linguagens) @
vnTamanho = TamanhoAlfa(vaTexto);  @ "A função retorna um valor" @
Se (EstaNulo(vaDado, vnEhNulo) = 0) {  @ "A função retorna um valor" @

@ ✅ Pensamento CORRETO (estilo LSP) @
TamanhoAlfa(vaTexto, vnTamanho);   @ "A função preenche vnTamanho" @
EstaNulo(vaDado, vnEhNulo);        @ "A função preenche vnEhNulo" @
Se (vnEhNulo = 0) {                @ "Compara a variável preenchida" @
```

### **💭 Modelo Mental #2: "Manipulação Primeiro, Função Depois"**
**Pense assim:** Faça **todas as operações** primeiro, depois chame a função com o resultado.

**Analogia:** É como cozinhar - prepare todos os ingredientes antes de colocar na panela.

**Exemplo:**
```lsp
@ ❌ INCORRETO - Tentando fazer tudo na função @
Mensagem(Retorna, "Resultado: " + vaValor + " - Total: " + vaTotal);

@ ✅ CORRETO - Preparando tudo antes @
vaMensagem = "Resultado: " + vaValor + " - Total: " + vaTotal;
Mensagem(Retorna, vaMensagem);
```

### **💭 Modelo Mental #3: "Variáveis são Recipientes"**
**Pense assim:** Variáveis são como **caixas** que guardam valores. Você precisa de uma caixa para cada valor que quer manipular.

**Analogia:** É como organizar uma despensa - cada tipo de alimento vai em um recipiente específico.

**Exemplo:**
```lsp
@ ❌ INCORRETO - Tentando usar valores "soltos" @
Mensagem(Retorna, "Nome: " + "João" + " - Idade: " + 25);

@ ✅ CORRETO - Cada valor em sua "caixa" @
Definir Alfa vaNome;
Definir Numero vnIdade;
Definir Alfa vaMensagem;

vaNome = "João";
vnIdade = 25;
vaMensagem = "Nome: " + vaNome + " - Idade: " + vnIdade;
Mensagem(Retorna, vaMensagem);
```

### **💭 Modelo Mental #4: "LSP é Sequencial"**
**Pense assim:** LSP executa **linha por linha**, na ordem que você escreveu. Não há "mágica" - tudo é explícito.

**Analogia:** É como seguir uma receita de bolo - cada passo deve ser feito na ordem correta.

**Exemplo:**
```lsp
@ ❌ INCORRETO - Tentando usar antes de preparar @
vaMensagem = "Resultado: " + vaResultado;  @ vaResultado ainda não existe @
vnResultado = vnA + vnB;

@ ✅ CORRETO - Preparando antes de usar @
vnResultado = vnA + vnB;
vaMensagem = "Resultado: " + vaResultado;
```

### **🎯 Casos de Uso Comuns da LSP**

#### **📊 Automação de Processos**
- Cálculos automáticos em formulários
- Validação de dados em tempo real
- Geração de relatórios personalizados
- Processamento em lote

#### **🌐 Integrações**
- Consumo de APIs REST
- Integração com sistemas externos
- Sincronização de dados
- Importação/exportação de arquivos

#### **🔧 Customizações Senior**
- Regras de negócio específicas
- Workflows personalizados
- Validações complexas
- Transformação de dados

#### **💼 Exemplos Práticos**
```lsp
@ Validação de CNPJ @
Se (TamanhoAlfa(vaCNPJ) <> 14) {
  Mensagem(Erro, "CNPJ deve ter 14 dígitos");
}

@ Integração com CEP @
HttpGet(vaHTTP, "https://viacep.com.br/ws/" + vaCEP + "/json/", vaResposta);
ValorElementoJson(vaResposta, "", "logradouro", vaEndereco);

@ Cálculo automático @
vnDesconto = (vnValor * vnPercentual) / 100;
vnTotal = vnValor - vnDesconto;
```

## 🎯 **Casos de Uso Reais Detalhados**

### **🏢 Cenário Empresarial: Validação de Cliente**
```lsp
@ Sistema completo de validação de dados de cliente @
Definir Funcao validarCliente();

Funcao validarCliente(); {
  @ 1. Validação de CNPJ @
  EstaNulo(vaCNPJ, vnEhNulo);
  Se (vnEhNulo = 0) {
    DeixaNumeros(vaCNPJ);
    TamanhoAlfa(vaCNPJ, vnTamanho);
    Se (vnTamanho <> 14) {
      Mensagem(Erro, "CNPJ deve ter 14 dígitos");
      Cancel(1);
    }
  } Senao {
    Mensagem(Erro, "CNPJ não pode ser nulo");
    Cancel(1);
  }
  
  @ 2. Validação de email @
  EstaNulo(vaEmail, vnEhNulo);
  Se (vnEhNulo = 0) {
    PosicaoAlfa("@", vaEmail, vnPosArroba);
    Se (vnPosArroba = 0) {
      Mensagem(Erro, "Email inválido - deve conter @");
      Cancel(1);
    }
  } Senao {
    Mensagem(Erro, "Email não pode ser nulo");
    Cancel(1);
  }
  
  @ 3. Validação de telefone @
  EstaNulo(vaTelefone, vnEhNulo);
  Se (vnEhNulo = 0) {
    DeixaNumeros(vaTelefone);
    TamanhoAlfa(vaTelefone, vnTamanho);
    Se (vnTamanho < 10) {
      Mensagem(Erro, "Telefone inválido - mínimo 10 dígitos");
      Cancel(1);
    }
  } Senao {
    Mensagem(Erro, "Telefone não pode ser nulo");
    Cancel(1);
  }
  
  @ 4. Validação de data de nascimento @
  DataHoje(vdDataAtual);
  Se (vdDataNascimento > vdDataAtual) {
    Mensagem(Erro, "Data de nascimento não pode ser futura");
    Cancel(1);
  }
  
  Mensagem(Retorna, "Cliente validado com sucesso!");
}
```

### **🌐 Cenário de Integração: Consulta CEP Automática**
```lsp
@ Sistema de consulta automática de CEP com validação @
Definir Funcao consultarCEP();

Funcao consultarCEP(); {
  @ 1. Limpa e valida CEP @
  EstaNulo(vaCEP, vnEhNulo);
  Se (vnEhNulo = 0) {
    DeixaNumeros(vaCEP);
    TamanhoAlfa(vaCEP, vnTamanho);
    Se (vnTamanho <> 8) {
      Mensagem(Erro, "CEP deve ter 8 dígitos");
      Cancel(1);
    }
  } Senao {
    Mensagem(Erro, "CEP não pode ser nulo");
    Cancel(1);
  }
  
  @ 2. Monta URL da API @
  vaURL = "https://viacep.com.br/ws/" + vaCEP + "/json/";
  
  @ 3. Configura e executa requisição @
  HttpObjeto(vaHTTP);
  HttpGet(vaHTTP, vaURL, vaResposta);
  
  @ 4. Verifica se encontrou CEP @
  PosicaoAlfa("erro", vaResposta, vnPosErro);
  Se (vnPosErro > 0) {
    Mensagem(Erro, "CEP não encontrado");
    Cancel(1);
  }
  
  @ 5. Extrai dados do JSON @
  ValorElementoJson(vaResposta, "", "logradouro", vaEndereco);
  ValorElementoJson(vaResposta, "", "bairro", vaBairro);
  ValorElementoJson(vaResposta, "", "localidade", vaCidade);
  ValorElementoJson(vaResposta, "", "uf", vaEstado);
  
  @ 6. Monta e exibe resultado @
  vaMensagem = vaEndereco + ", " + vaBairro + " - " + vaCidade + "/" + vaEstado;
  Mensagem(Retorna, vaMensagem);
}
```

### **📊 Cenário de Processamento: Relatório de Vendas**
```lsp
@ Sistema de geração de relatório de vendas @
Definir Funcao gerarRelatorioVendas();

Funcao gerarRelatorioVendas(); {
  @ 1. Valida período @
  Se (vdDataInicio > vdDataFim) {
    Mensagem(Erro, "Data inicial não pode ser maior que final");
    Cancel(1);
  }
  
  @ 2. Consulta vendas no banco @
  vaSQL = "SELECT SUM(valor) as total FROM vendas WHERE data BETWEEN '" + 
          vdDataInicio + "' AND '" + vdDataFim + "'";
  
  SQL_Criar(vaSQL);
  SQL_Executar(vaSQL);
  
  @ 3. Processa resultado @
  Se (SQL_Proximo(vaSQL) = 1) {
    SQL_DefinirNumero(vaSQL, "total", vnTotalVendas);
    
    @ 4. Formata valores @
    IntParaAlfa(vnTotalVendas, vaTotalStr);
    
    @ 5. Calcula estatísticas @
    vnMediaDiaria = vnTotalVendas / 30;  @ Assumindo 30 dias @
    IntParaAlfa(vnMediaDiaria, vaMediaStr);
    
    @ 6. Monta relatório @
    vaRelatorio = "RELATÓRIO DE VENDAS" + #13 + #10 +
                  "Período: " + vdDataInicio + " a " + vdDataFim + #13 + #10 +
                  "Total: R$ " + vaTotalStr + #13 + #10 +
                  "Média diária: R$ " + vaMediaStr;
    
    Mensagem(Retorna, vaRelatorio);
  } Senao {
    Mensagem(Erro, "Nenhuma venda encontrada no período");
  }
  
  SQL_Fechar(vaSQL);
}
```

### **🔐 Cenário de Segurança: Validação de Senha**
```lsp
@ Sistema de validação de senha com critérios de segurança @
Definir Funcao validarSenha();

Funcao validarSenha(); {
  @ 1. Verifica se não é nulo @
  EstaNulo(vaSenha, vnEhNulo);
  Se (vnEhNulo = 1) {
    Mensagem(Erro, "Senha não pode ser nula");
    Cancel(1);
  }
  
  @ 2. Verifica tamanho mínimo @
  TamanhoAlfa(vaSenha, vnTamanho);
  Se (vnTamanho < 8) {
    Mensagem(Erro, "Senha deve ter pelo menos 8 caracteres");
    Cancel(1);
  }
  
  @ 3. Verifica se tem letra maiúscula @
  vnContador = 1;
  vnTemMaiuscula = 0;
  Enquanto (vnContador <= vnTamanho) {
    CopiarAlfa(vaSenha, vnContador, 1);
    Se (vaCaracter >= "A" E vaCaracter <= "Z") {
      vnTemMaiuscula = 1;
    }
    vnContador++;
  }
  
  Se (vnTemMaiuscula = 0) {
    Mensagem(Erro, "Senha deve conter pelo menos uma letra maiúscula");
    Cancel(1);
  }
  
  @ 4. Verifica se tem número @
  vaSenhaNumeros = vaSenha;  @ Faz cópia para não modificar original @
  DeixaNumeros(vaSenhaNumeros);
  TamanhoAlfa(vaSenhaNumeros, vnTamanhoNumeros);
  Se (vnTamanhoNumeros = 0) {
    Mensagem(Erro, "Senha deve conter pelo menos um número");
    Cancel(1);
  }
  
  @ 5. Verifica se tem caractere especial @
  PosicaoAlfa("!", vaSenha, vnPos);
  Se (vnPos = 0) {
    PosicaoAlfa("@", vaSenha, vnPos);
  }
  Se (vnPos = 0) {
    PosicaoAlfa("#", vaSenha, vnPos);
  }
  
  Se (vnPos = 0) {
    Mensagem(Erro, "Senha deve conter pelo menos um caractere especial (!@#)");
    Cancel(1);
  }
  
  Mensagem(Retorna, "Senha válida!");
}
```

---

## 📋 **Referência Rápida**

### **Declaração de Variáveis**
```lsp
Definir Alfa vaNome;        @ Texto/String @
Definir Numero vnIdade;     @ Número (int/decimal) @
Definir Data vdNascimento;  @ Data @
```

### **Operadores Básicos**
```lsp
@ Aritméticos @
vnSoma = vnA + vnB;         @ Adição @
vnSub = vnA - vnB;          @ Subtração @
vnMult = vnA * vnB;         @ Multiplicação @
vnDiv = vnA / vnB;          @ Divisão @

@ Lógicos @
Se (vnA = vnB) { }          @ Igual @
Se (vnA <> vnB) { }         @ Diferente @
Se (vnA > vnB) { }          @ Maior @
Se (vnA < vnB) { }          @ Menor @
```

### **Estruturas de Controle**
```lsp
@ Condicional @
Se (condição) {
  @ código @
} Senao {
  @ código alternativo @
}

@ Loop @
Para (vnI = 1; vnI <= 10; vnI++) {
  @ código repetido @
}

Enquanto (condição) {
  @ código repetido @
}
```

### **Funções Essenciais**
```lsp
@ Mensagens @
Mensagem(Retorna, vaMensagem);
Mensagem(Erro, vaErro);

@ Conversões @
IntParaAlfa(vnNumero, vaTexto);
AlfaParaInt(vaTexto, vnNumero);

@ Strings @
TamanhoAlfa(vaTexto, vnTamanho);
PosicaoAlfa("busca", vaTexto, vnPosicao);
```

## 🎯 **Quick Reference Cards**

### **💳 Card: Manipulação de Strings**
```
┌─────────────────────────────────┐
│ 📝 MANIPULAÇÃO DE STRINGS       │
├─────────────────────────────────┤
│ TamanhoAlfa(texto, tamanho)     │
│ PosicaoAlfa(busca, texto, pos)  │
│ SubstAlfa(antigo, novo, texto)  │
│ CopiarAlfa(texto, pos, qtd)     │
│ LimpaEspacos(texto)             │
│ DeletarAlfa(texto, pos, qtd)    │
│ InserirAlfa(texto, pos, novo)   │
└─────────────────────────────────┘
```

### **💳 Card: Conversões**
```
┌─────────────────────────────────┐
│ 🔄 CONVERSÕES                   │
├─────────────────────────────────┤
│ IntParaAlfa(numero, texto)      │
│ AlfaParaInt(texto, numero)      │
│ AlfaParaDecimal(texto, decimal) │
│ StrParaInt(texto, numero)       │
│ IntParaStr(numero, texto)       │
│ AlfaParaData(texto, data)       │
└─────────────────────────────────┘
```

### **💳 Card: Datas**
```
┌─────────────────────────────────┐
│ 📅 MANIPULAÇÃO DE DATAS         │
├─────────────────────────────────┤
│ DataHoje(data)                  │
│ DataHora(data)                  │
│ MontaData(dia, mes, ano, data)  │
│ DecodData(data, dia, mes, ano)  │
│ AdicionarDias(data, dias)       │
│ FormatarData(data, formato)     │
└─────────────────────────────────┘
```

### **💳 Card: Validação**
```
┌─────────────────────────────────┐
│ ✅ VALIDAÇÃO E VERIFICAÇÃO      │
├─────────────────────────────────┤
│ EstaNulo(dado, ehNulo)         │
│ DeixaNumeros(texto)             │
│ VrfAbrA(valor, min, max)        │
│ TamanhoAlfa(texto, tamanho)     │
│ PosicaoAlfa(busca, texto, pos)  │
│                                 │
│ ⚠️ Lembre-se: Execute primeiro, │
│    depois compare a variável!   │
└─────────────────────────────────┘
```

### **💳 Card: HTTP e APIs**
```
┌─────────────────────────────────┐
│ 🌐 HTTP E APIS                  │
├─────────────────────────────────┤
│ HttpObjeto(http)                │
│ HttpGet(http, url, resposta)    │
│ HttpPost(http, url, dados)      │
│ ValorElementoJson(json, path)   │
└─────────────────────────────────┘
```

### **💳 Card: Banco de Dados**
```
┌─────────────────────────────────┐
│ 🗃️ BANCO DE DADOS               │
├─────────────────────────────────┤
│ SQL_Criar(sql)                  │
│ SQL_Executar(sql)               │
│ SQL_Proximo(sql)                │
│ SQL_Fechar(sql)                 │
│ SQL_Definir<tipo>(sql, campo)   │
└─────────────────────────────────┘
```

---

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
Definir Alfa vaResultadoStr;
IntParaAlfa(vnResultado, vaResultadoStr);
Mensagem(Retorna, vaResultadoStr);
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
- **Funcao**: Funções definidas pelo programador.

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

- Variáveis do tipo Data deve-se usar a função MontaData(dd,mm,yyyy,vdData); para atribuir uma data ou atribuir a variável de sistema DatSis
- O nome das variáveis não pode ser igual ao nome dos parâmetros de funções
- O nome das variáveis não pode ser igual ao nome dos campos de listas
- Variáveis devem seguir o padrão de nomenclatura: prefixo + nome descritivo em CamelCase

### Padrão de Nomenclatura de Variáveis

A LSP utiliza um padrão específico de nomenclatura que facilita a identificação do tipo de variável:

**Prefixos por Tipo:**
- `va`: Variáveis do tipo **Alfa** (string/texto)
- `vn`: Variáveis do tipo **Numero** (inteiro/decimal)
- `vd`: Variáveis do tipo **Data** (data/hora)

**Regras de Nomenclatura:**
- Use CamelCase após o prefixo
- Nomes descritivos e significativos
- Máximo de 100 caracteres
- Pode conter `_` (underscore)
- Não use acentuação
- Não use palavras reservadas

**Exemplos Corretos:**
```lsp
@ Variáveis Alfa @
Definir Alfa vaNomeCompleto;
Definir Alfa vaEmailUsuario;
Definir Alfa vaCaminhoArquivo;

@ Variáveis Número @
Definir Numero vnIdadeUsuario;
Definir Numero vnValorTotal;
Definir Numero vnContadorRegistros;

@ Variáveis Data @
Definir Data vdDataNascimento;
Definir Data vdDataCadastro;
Definir Data vdDataVencimento;
```

**Exemplos Incorretos:**
```lsp
@ Sem prefixo @
Definir Alfa nome; @ Incorreto @

@ Prefixo errado @
Definir Numero vaIdade; @ Incorreto: va é para Alfa @

@ Nomes não descritivos @
Definir Alfa va1; @ Incorreto: não é descritivo @
Definir Numero vnX; @ Incorreto: muito genérico @
```


## Manipulação Avançada de Strings

As funções de manipulação de strings na LSP permitem realizar operações complexas de processamento de texto, desde operações básicas até transformações avançadas e limpeza de dados.

### **📋 Resumo das Funções de String**

| **Categoria** | **Função** | **Uso** | **Exemplo** |
|---|---|---|---|
| **📏 Tamanho** | `TamanhoAlfa` | Obtém tamanho de texto | `TamanhoAlfa(vaTexto, vnTamanho)` |
| **🔍 Busca** | `PosicaoAlfa` | Encontra posição de texto | `PosicaoAlfa("@", vaEmail, vnPos)` |
| **✂️ Extração** | `CopiarAlfa` | Extrai parte do texto | `CopiarAlfa(vaTexto, 1, 5)` |
| **🔄 Substituição** | `SubstAlfa` | Substitui texto | `SubstAlfa("old", "new", vaTexto)` |
| **🔤 Conversão** | `ConverteParaMaiusculo` | Maiúsculo/minúsculo | `ConverteParaMaiusculo(vaTexto)` |
| **📝 Limpeza** | `DeixaNumeros` | Remove não-números | `DeixaNumeros(vaCEP)` |

### **🚀 Exemplo Prático: Processamento de Email**

```lsp
@ === EXEMPLO COMPLETO: VALIDAÇÃO DE EMAIL === @
Definir Funcao validarEmail();

@ Variáveis globais @
Definir Alfa vaEmail;
Definir Numero vnPosArroba;
Definir Numero vnPosPonto;
Definir Numero vnTamanho;
Definir Alfa vaUsuario;
Definir Alfa vaDominio;

vaEmail = "joao.silva@empresa.com.br";
validarEmail();

Funcao validarEmail(); {
  @ 1. Verificar tamanho @
  TamanhoAlfa(vaEmail, vnTamanho);
  Se (vnTamanho < 5) {
    Mensagem(Erro, "Email muito curto!");
    Pare;
  }
  
  @ 2. Encontrar @ @
  PosicaoAlfa("@", vaEmail, vnPosArroba);
  Se (vnPosArroba = 0) {
    Mensagem(Erro, "Email deve conter @");
    Pare;
  }
  
  @ 3. Extrair usuário @
  vaUsuario = vaEmail;
  CopiarAlfa(vaUsuario, 1, vnPosArroba - 1);
  
  @ 4. Extrair domínio @
  vaDominio = vaEmail;
  CopiarAlfa(vaDominio, vnPosArroba + 1, vnTamanho - vnPosArroba);
  
  @ 5. Verificar domínio @
  PosicaoAlfa(".", vaDominio, vnPosPonto);
  Se (vnPosPonto = 0) {
    Mensagem(Erro, "Domínio deve conter ponto");
  } Senao {
    Definir Alfa vaMensagem;
    vaMensagem = "Email válido! Usuário: " + vaUsuario + ", Domínio: " + vaDominio;
    Mensagem(Retorna, vaMensagem);
  }
}
```

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

#### CaracterParaAlfa

Converte um caracter (que fica armazenado pelo código ASCII) para o valor Alfanumérico correspondente.

**Sintaxe:**

```lsp
CaracterParaAlfa(<caractere>, <destino>);
```

**Parâmetros:**
- `caractere`: Campo/Variável que mantém o código ASCII de um caracter
- `destino`: Variável que receberá o resultado da conversão

**Exemplo:**
```lsp
Definir Alfa vaLetra;
Definir Alfa vaEnter;

@ Conversão de código ASCII para caracter @
CaracterParaAlfa(65, vaLetra); @ vaLetra será "A" @

@ Quebra de linha @
CaracterParaAlfa(13, vaEnter); @ vaEnter será quebra de linha @
```

**⚠️ Importante:** Se for utilizar para inserir quebras de linha em envio de e-mail e na Central de Configurações Senior estiver habilitada a opção "Converter quebras de linha para HTML", todas as quebras de linha Windows (caracteres ASCII 13 e 10) serão convertidas para tags `<br/>`. 

### Funções Básicas de Manipulação

#### CopiarAlfa e CopiarStr

Copiam parte do conteúdo de uma variável/campo alfanumérico modificando a própria variável de origem.

**Sintaxe:**

```lsp
CopiarAlfa(<variavel>, <posicao>, <tamanho>);
CopiarStr(<variavel>, <posicao>, <tamanho>);
```

**Parâmetros:**
- `variavel`: Variável que contém o texto e que será modificada para conter apenas a parte copiada
- `posicao`: Posição inicial (baseada em 1)
- `tamanho`: Quantidade de caracteres a copiar

**⚠️ Importante:** A função **modifica diretamente** a variável de origem, substituindo seu conteúdo pela parte copiada.

**Exemplo Prático:**

```lsp
Definir Alfa vaTexto;
Definir Alfa vaNome;
Definir Alfa vaSobrenome;

@ Para extrair "João" @
vaTexto = "João Silva Santos";
vaNome = vaTexto;  @ Faz uma cópia primeiro @
CopiarAlfa(vaNome, 1, 4); @ vaNome será "João" @

@ Para extrair "Silva" @
vaSobrenome = vaTexto;  @ Faz uma cópia primeiro @
CopiarAlfa(vaSobrenome, 6, 5); @ vaSobrenome será "Silva" @
```

**📋 Exemplo da Documentação Oficial Senior:**

```lsp
Definir Alfa exemplo;
exemplo = "texto de exemplo";
CopiarAlfa(exemplo, 12, 3);
@ Após o uso da função, o conteúdo da variável "exemplo" seria "emp" @
```

#### TamanhoAlfa e TamanhoStr

Retornam o tamanho de uma variável/campo alfanumérico através de parâmetro de retorno.

**Sintaxe:**

```lsp
TamanhoAlfa(<origem>, <tamanho>);
TamanhoStr(<origem>, <tamanho>);
```

**Parâmetros:**
- `origem`: Campo/Variável que se deseja saber o tamanho
- `tamanho`: Variável Numero que receberá o tamanho

**Exemplo de Validação:**

```lsp
Definir Alfa vaSenha;
Definir Numero vnTamanho;
Definir Alfa vaMensagem;
Definir Alfa vaNumeroStr;

vaSenha = "minhasenha123";
TamanhoAlfa(vaSenha, vnTamanho);

Se (vnTamanho < 8) {
  vaMensagem = "Senha deve ter pelo menos 8 caracteres";
  Mensagem(Erro, vaMensagem);
} Senao {
  IntParaAlfa(vnTamanho, vaNumeroStr);
  vaMensagem = "Senha válida com " + vaNumeroStr + " caracteres";
  Mensagem(Retorna, vaMensagem);
}
```

**⚠️ Importante:** Essas funções **não retornam valor diretamente**. O resultado é passado através do parâmetro de retorno.

#### PosicaoAlfa e PosicaoStr

Procuram por uma parte de texto dentro de um campo/variável, retornando a posição inicial através de parâmetro.

**Sintaxe:**

```lsp
PosicaoAlfa(<subtexto>, <texto>, <posicao>);
PosicaoStr(<subtexto>, <texto>, <posicao>);
```

**Parâmetros:**
- `subtexto`: Texto que se está procurando
- `texto`: Campo/variável onde fazer a busca
- `posicao`: Variável que receberá a posição inicial (0 se não encontrar)

**Exemplo de Validação de Email:**

```lsp
Definir Alfa vaEmail;
Definir Numero vnPosArroba;
Definir Numero vnPosPonto;

vaEmail = "usuario@empresa.com.br";
PosicaoAlfa("@", vaEmail, vnPosArroba);
PosicaoAlfa(".", vaEmail, vnPosPonto);

Se (vnPosArroba = 0) {
  Mensagem(Erro, "Email inválido: falta @");
} Senao Se (vnPosPonto = 0) {
  Mensagem(Erro, "Email inválido: falta domínio");
} Senao {
  Mensagem(Retorna, "Email válido!");
}
```

**⚠️ Importante:** Essas funções **usam parâmetro de retorno**, não retorno direto.

#### SubstAlfa e SubstAlfaUmaVez

Substituem trechos específicos dentro de um texto por outro texto.

**Sintaxe:**

```lsp
SubstAlfa(<subtexto>, <novoTexto>, <texto>);      @ Substitui todas as ocorrências @
SubstAlfaUmaVez(<subtexto>, <novoTexto>, <texto>); @ Substitui apenas a primeira @
```

**Parâmetros:**
- `subtexto`: Texto a ser localizado e substituído
- `novoTexto`: Texto que irá substituir
- `texto`: Variável que contém o texto original e receberá o resultado

**Exemplo de Limpeza de Dados:**

```lsp
Definir Alfa vaTexto;
Definir Alfa vaTextoLimpo;

vaTexto = "João--Silva--Santos";
vaTextoLimpo = vaTexto;

@ Substitui todos os traços duplos por espaço simples @
SubstAlfa("--", " ", vaTextoLimpo);
@ vaTextoLimpo será "João Silva Santos" @

@ Exemplo com SubstAlfaUmaVez @
vaTexto = "teste teste teste";
SubstAlfaUmaVez("teste", "TESTE", vaTexto);
@ vaTexto será "TESTE teste teste" (apenas o primeiro) @
```

#### Concatena

Concatena até 3 campo/variáveis tipo alfa, formando uma só variável.

**Sintaxe:**

```lsp
Concatena(<str1>, <str2>, <str3>, <destino>);
```

**Parâmetros:**
- `str1`: Campo/Variável que será concatenado
- `str2`: Campo/Variável que será concatenado  
- `str3`: Campo/Variável que será concatenado
- `destino`: Variável que receberá o resultado da concatenação (retorno)

**Exemplo:**

```lsp
Definir Alfa vaTexto1;
Definir Alfa vaTexto2;
Definir Alfa vaTexto3;
Definir Alfa vaResultado;

vaTexto1 = "Pedro Luiz Souza";
vaTexto2 = " - ";
vaTexto3 = "Pedrão";

Concatena(vaTexto1, vaTexto2, vaTexto3, vaResultado);
@ vaResultado será "Pedro Luiz Souza - Pedrão" @
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

#### DeletarStr

Elimina parte de um texto.

**Sintaxe:**
```lsp
DeletarStr(<origem>, <posicao>, <quantidade>);
```

**Parâmetros:**
- `origem`: Variável que passará o texto cuja parte será deletada
- `posicao`: Variável que indica a posição de início da eliminação
- `quantidade`: Variável que indica a quantidade de caracteres a serem eliminados

**Exemplo:**
```lsp
Definir Alfa vaOrigem;
vaOrigem = "Senior empresa de Sistemas";
DeletarStr(vaOrigem, 8, 11);
@ vaOrigem será "Senior Sistemas" @
```

#### InserirAlfa

Insere um ou mais caracteres em uma variável/campo, a partir da posição indicada.

**Sintaxe:**
```lsp
InserirAlfa(<valor>, <origem>, <posicao>);
```

**Parâmetros:**
- `valor`: Variável que contém a string que deseja-se inserir
- `origem`: Variável que contém a string de origem e que receberá o conteúdo da inserção
- `posicao`: Variável que indica a posição em Origem a partir de onde Valor será inserido

**Exemplo:**
```lsp
Definir Alfa vaOrigem;
vaOrigem = "Senior Sistemas";
InserirAlfa("empresa de ", vaOrigem, 8);
@ vaOrigem será "Senior empresa de Sistemas" @
```

**Observação:** O conteúdo da variável Origem será truncado caso o tamanho definido para o campo/variável não for respeitado.

#### InserirStr

Esta função insere um ou mais caracteres em uma Variável/Campo, a partir da posição indicada.

**Sintaxe:**
```lsp
InserirStr(<valor>, <origem>, <posicao>);
```

**Parâmetros:**
- `valor`: Variável que contém a string que deseja-se inserir
- `origem`: Variável que contém a string de origem e que receberá o conteúdo da inserção
- `posicao`: Variável que indica a posição em Origem a partir de onde Valor será inserido

**Exemplo:**
```lsp
Definir Alfa vaOrigem;
vaOrigem = "Senior Sistemas";
InserirStr("empresa de ", vaOrigem, 8);
@ vaOrigem será "Senior empresa de Sistemas" @
```

**Observação:** O conteúdo da variável Origem será truncado caso o tamanho definido para o campo/variável não for respeitado.

#### LimpaEspacos

Limpa os espaços em branco à direita e à esquerda de uma variável alfanumérica.

**Sintaxe:**
```lsp
LimpaEspacos(<texto>);
```

**Exemplo:**
```lsp
Definir Alfa vaTexto;
vaTexto = "  texto com espaços  ";
LimpaEspacos(vaTexto);
@ vaTexto será "texto com espaços" @
```

#### LimpaEspacosDireita

Limpa os espaços em branco à direita de uma variável alfanumérica.

**Sintaxe:**
```lsp
LimpaEspacosDireita(<texto>);
```

**Exemplo:**
```lsp
Definir Alfa vaTexto;
vaTexto = "  texto com espaços  ";
LimpaEspacosDireita(vaTexto);
@ vaTexto será "  texto com espaços" @
```

#### LimpaEspacosEsquerda

Limpa os espaços em branco à esquerda de uma variável alfanumérica.

**Sintaxe:**
```lsp
LimpaEspacosEsquerda(<texto>);
```

**Exemplo:**
```lsp
Definir Alfa vaTexto;
vaTexto = "  texto com espaços  ";
LimpaEspacosEsquerda(vaTexto);
@ vaTexto será "texto com espaços  " @
```

#### QuebraTexto

Esta função pega o texto indicado e faz assinalamentos de quebra de linha conforme o Tamanho_Linha especificado, retornando a quantidade de linhas que será usada para imprimir o texto.

**Sintaxe:**
```lsp
QuebraTexto(<texto>, <tamanhoLinha>, <quantidadeLinhas>);
```

**Parâmetros:**
- `texto`: Campo/Variável que se deseja imprimir em mais de uma linha
- `tamanhoLinha`: Variável que indica a quantidade máxima de caracteres por linha
- `quantidadeLinhas`: Variável que indica qual é a quantidade de linhas que serão necessárias para imprimir o texto

**Exemplo:**
```lsp
Definir Alfa vaTexto;
Definir Alfa vaFrase;
Definir Numero vnNumLin;
Definir Numero vnLinAtu;

vaTexto = "Vamos ver o que acontece quando usamos estas funções para controle de impressão de linhas de um texto mais extenso";
QuebraTexto(vaTexto, 30, vnNumLin);

vnLinAtu = 1;
Enquanto (vnLinAtu <= vnNumLin) {
  BuscaLinhaTexto(vaTexto, vnLinAtu, vaFrase);
  @ Processa cada linha @
  vnLinAtu++;
}
```

**Utilização da Função (dependentes):** BuscaLinhaTexto(Alfa Texto, Numero NroLin, Alfa End LinTex);

#### ProcuraEnter

Esta função procura um caractere que indica "enter" ou nova linha (#13 ou #10) em uma string e retorna a string antes do primeiro enter, e o restante da string original, em variáveis separadas.

**Sintaxe:**
```lsp
ProcuraEnter(<strProcura>, <strImp>, <strResto>);
```

**Parâmetros:**
- `strProcura`: String na qual será procurada o enter ou nova linha (#13 ou #10)
- `strImp`: A primeira parte da string procurada, até o primeiro caracter que indica nova linha (retorno)
- `strResto`: O restante da string, depois do primeiro caracter que indica nova linha (retorno)

**Exemplo:**
```lsp
Definir Alfa vaStrProcura;
Definir Alfa vaStrImp;
Definir Alfa vaStrResto;

vaStrProcura = "Primeira linha" + vaEnter + "Segunda linha";
ProcuraEnter(vaStrProcura, vaStrImp, vaStrResto);
@ vaStrImp será "Primeira linha" @
@ vaStrResto será "Segunda linha" @
```

**Observações:** Para imprimir cada obs separada por enter basta mandar imprimir a variável StrImp e depois procurar sempre pela StrResto.

#### CalculaAlfa

Realiza operações matemáticas com valores alfanuméricos.

**Sintaxe:**
```lsp
CalculaAlfa(<operacao>, <argumento1>, <argumento2>, <resultado>);
```

**Parâmetros:**
- `operacao`: Campo indicando que operação deve ser realizada:
  - "+": soma
  - "-": subtração
  - "*": multiplicação
- `argumento1`: Campo contendo o primeiro argumento a ser usado no cálculo
- `argumento2`: Campo contendo o segundo argumento a ser usado no cálculo
- `resultado`: Variável alfa que receberá o resultado do cálculo

**Exemplo:**
```lsp
Definir Alfa vaOperacao;
Definir Alfa vaArg1;
Definir Alfa vaArg2;
Definir Alfa vaResultado;

vaOperacao = "+";
vaArg1 = "100";
vaArg2 = "50";
CalculaAlfa(vaOperacao, vaArg1, vaArg2, vaResultado);
@ vaResultado será "150" @
```

**Observações:** Estão disponíveis as operações de soma, subtração e multiplicação. Todos os cálculos são realizados com números inteiros, caso seja informado um número não inteiro um erro ocorrerá. Cálculos feitos com esta função demoram muito mais para serem processados do que cálculos diretos (c = a + b).

#### CarregarTextoArq

Esta função carrega para uma variável alfanumérica o conteúdo de um arquivo texto.

**Sintaxe:**
```lsp
CarregarTextoArq(<arquivo>, <texto>);
```

**Parâmetros:**
- `arquivo`: Variável com o caminho do arquivo a ser lido
- `texto`: Variável que retorna o texto lido do arquivo

**Exemplo:**
```lsp
Definir Alfa vaTexto;
CarregarTextoArq("C:\\Senior\\Sapiens\\Arquivo.txt", vaTexto);
```

#### Concatena

Esta função concatena até 3 campo/variáveis tipo alfa, formando uma só variável.

**Sintaxe:**
```lsp
Concatena(<str1>, <str2>, <str3>, <destino>);
```

**Parâmetros:**
- `str1`: Campo/Variável que será concatenado
- `str2`: Campo/Variável que será concatenado
- `str3`: Campo/Variável que será concatenado
- `destino`: Variável que receberá o resultado da concatenação (retorno)

**Exemplo:**
```lsp
Definir Alfa vaResultado;
Definir Alfa vaNome;
Definir Alfa vaApelido;

vaNome = "Pedro Luiz Souza";
vaApelido = "Pedrão";

Concatena(vaNome, " - ", vaApelido, vaResultado);
@ vaResultado será "Pedro Luiz Souza - Pedrão" @
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

Identifica qual caracter está em determinada posição do campo/variável de origem.

**Sintaxe:**

```lsp
LerPosicaoAlfa(<origem>, <destino>, <posicao>);
```

**Parâmetros:**
- `origem`: Campo/Variável Alfa que se deseja verificar
- `destino`: Variável Numero que receberá o código ASCII do caracter lido
- `posicao`: Posição do Campo/Variável de Origem que se deseja identificar o caracter

**Exemplo:**

```lsp
Definir Alfa vaTexto;
Definir Numero vnCodigoCaractere;
Definir Numero vnPosicao;

vaTexto = "TESTE";
vnPosicao = 1;

@ Obtém o código ASCII do primeiro caractere @
LerPosicaoAlfa(vaTexto, vnCodigoCaractere, vnPosicao);
@ vnCodigoCaractere será 84 (código ASCII de 'T') @

@ Comparação com código ASCII @
Se (vnCodigoCaractere = 84) { @ 'T' @
  Mensagem(Retorna, "Primeiro caractere é T");
}

@ Para comparar diretamente com caractere, use aspas simples @
Se (vnCodigoCaractere = 'T') {
  Mensagem(Retorna, "Primeiro caractere é T");
}
```

**Observações:**
- A função retorna o código ASCII do caractere, não o caractere em si
- Para obter o caractere como string, use `CopiarAlfa` em vez de `LerPosicaoAlfa`
- Para comparações diretas com caracteres, use aspas simples (`'T'`)

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

Retorna a quantidade de itens em uma lista concatenada através de parâmetro de retorno.

**Sintaxe:**

```lsp
ListaQuantidade(<texto>, <separador>, <quantidade>);
```

**Parâmetros:**
- `texto`: Texto com itens separados
- `separador`: Caractere que separa os itens
- `quantidade`: Variável que receberá a quantidade de itens

**Exemplo de Contagem:**

```lsp
Definir Alfa vaEmails;
Definir Numero vnQuantidade;
Definir Alfa vaMensagem;
Definir Alfa vaQuantidadeStr;

vaEmails = "user1@teste.com,user2@teste.com,user3@teste.com";
ListaQuantidade(vaEmails, ",", vnQuantidade);

IntParaAlfa(vnQuantidade, vaQuantidadeStr);
vaMensagem = "Total de emails: " + vaQuantidadeStr;
Mensagem(Retorna, vaMensagem); @ "Total de emails: 3" @
```

**⚠️ Importante:** Esta função **usa parâmetro de retorno**, seguindo o padrão LSP.

### Funções de Codificação

#### ConverteCodificacaoString

Esta função altera a codificação de um texto contido em uma variável, onde este texto com a codificação alterada pode ser utilizado para comunicação com web services.

**Sintaxe:**

```lsp
vnRetorno = ConverteCodificacaoString(<textoOrigem>, <codificacao>, <textoDestino>);
```

**Parâmetros:**
- `textoOrigem`: Contém o texto original que necessita ter sua codificação alterada
- `codificacao`: Nome da codificação para a qual o texto será convertido ("UTF-8" ou "WINDOWS-1252")
- `textoDestino`: Contém o texto com a codificação alterada

**Valor de Retorno:**
- `0`: Conversão realizada com sucesso
- `1`: Texto possui caracteres não suportados pela codificação

**Exemplo:**

```lsp
Definir Alfa vaTextoOriginal;
Definir Alfa vaTextoCodificado;
Definir Numero vnRetorno;

vaTextoOriginal = "Acentuação especial";

vnRetorno = ConverteCodificacaoString(vaTextoOriginal, "UTF-8", vaTextoCodificado);

Se (vnRetorno = 1) {
  Mensagem(Retorna, "Encontrado caracteres incompatíveis!");
} Senao {
  Mensagem(Retorna, "Conversão realizada com sucesso!");
}
```

**Observação:** Se o sistema não suportar a codificação informada, será emitida a mensagem: "A codificação X não é suportada. Verifique a documentação".

#### ConverteTexto

Realiza a substituição de caracteres especiais de acordo com o padrão de codificação informada no primeiro parâmetro, retorna um novo texto com os caracteres convertidos.

**Sintaxe:**

```lsp
ConverteTexto(<codificacao>, <textoOrigem>, <textoDestino>);
```

**Parâmetros:**
- `codificacao`: Codificação do formato de origem do texto (formato suportado: "JSON")
- `textoOrigem`: Texto contendo os caracteres que necessitam ser convertidos
- `textoDestino`: Variável que recebe o texto convertido

**Exemplo:**

```lsp
Definir Alfa vaTextoOrigem;
Definir Alfa vaTextoDestino;

vaTextoOrigem = "\\u00c1gua";

ConverteTexto("JSON", vaTextoOrigem, vaTextoDestino);
@ vaTextoDestino recebe o valor "Água" @
```

**Observação:** A função ConverteTexto deve ser utilizada somente para a conversão de conjunto de caracteres, não sendo recomendada para conversão de conjunto de dados, por exemplo estruturas JSON.

**Tabela de Caracteres Suportados na Conversão:**

| Código | Conversão | Código | Conversão | Código | Conversão | Código | Conversão |
|--------|-----------|--------|-----------|--------|-----------|--------|-----------|
| \\u0021 | ! | \\u0041 | A | \\u0061 | a | \\u00C1 | Á |
| \\u0022 | " | \\u0042 | B | \\u0062 | b | \\u00C2 | Â |
| \\u0023 | # | \\u0043 | C | \\u0063 | c | \\u00C3 | Ã |
| \\u0025 | % | \\u0044 | D | \\u0064 | d | \\u00C7 | Ç |
| \\u0026 | & | \\u0045 | E | \\u0065 | e | \\u00C8 | È |
| \\u0027 | ' | \\u0046 | F | \\u0066 | f | \\u00C9 | É |
| \\u0028 | ( | \\u0047 | G | \\u0067 | g | \\u00CA | Ê |
| \\u0029 | ) | \\u0048 | H | \\u0068 | h | \\u00CC | Ì |
| \\u002A | * | \\u0049 | I | \\u0069 | i | \\u00CD | Í |
| \\u002B | + | \\u004A | J | \\u006A | j | \\u00CE | Î |
| \\u002C | , | \\u004B | K | \\u006B | k | \\u00D2 | Ò |
| \\u002D | - | \\u004C | L | \\u006C | l | \\u00D3 | Ó |
| \\u002E | . | \\u004D | M | \\u006D | m | \\u00D4 | Ô |
| \\u002F | / | \\u004E | N | \\u006E | n | \\u00D5 | Õ |
| \\u0030 | 0 | \\u004F | O | \\u006F | o | \\u00D9 | Ù |
| \\u0031 | 1 | \\u0050 | P | \\u0070 | p | \\u00DA | Ú |
| \\u0032 | 2 | \\u0051 | Q | \\u0071 | q | \\u00DB | Û |
| \\u0033 | 3 | \\u0052 | R | \\u0072 | r | \\u00E0 | à |
| \\u0034 | 4 | \\u0053 | S | \\u0073 | s | \\u00E1 | á |
| \\u0035 | 5 | \\u0054 | T | \\u0074 | t | \\u00E2 | â |
| \\u0036 | 6 | \\u0055 | U | \\u0075 | u | \\u00E3 | ã |
| \\u0037 | 7 | \\u0056 | V | \\u0076 | v | \\u00E7 | ç |
| \\u0038 | 8 | \\u0057 | W | \\u0077 | w | \\u00E8 | è |
| \\u0039 | 9 | \\u0058 | X | \\u0078 | x | \\u00E9 | é |
| \\u003B | ; | \\u0059 | Y | \\u0079 | y | \\u00EA | ê |
| \\u003C | < | \\u005A | Z | \\u007A | z | \\u00EC | ì |
| \\u003D | = | \\u005B | [ | \\u007B | { | \\u00ED | í |
| \\u003E | > | \\u005D | ] | \\u007C | \| | \\u00EE | î |
| \\u003F | ? | \\u005E | ^ | \\u007D | } | \\u00F1 | ñ |
| \\u0040 | @ | \\u005F | _ | \\u007E | ~ |  |  |
| \\u0060 | ` |  |  |  |  |  |  |

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
  Definir Alfa vaMensagem;
  @ Criptografa dados @
  Encriptar(vaDadosSensiveis, vaDadosCriptografados);
  vaMensagem = "Dados criptografados: " + vaDadosCriptografados;
  Mensagem(Retorna, vaMensagem);

  @ Descriptografa para uso @
  Desencriptar(vaDadosCriptografados, vaDadosRecuperados);
  
  @ Verifica integridade @
  Se (vaDadosRecuperados = vaDadosSensiveis) {
    Mensagem(Retorna, "Dados recuperados com sucesso!");
  } Senao {
    Mensagem(Erro, "Erro na integridade dos dados!");
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
  Definir Alfa vaMensagem;

  @ 1. Gera nonce para a sessão @
  GerarNonce(vaNonce);

  @ 2. Gera token de sessão @
  GeraToken(32, vaTokenSessao);

  @ 3. Gera senha temporária @
  GeraSenha(12, vaSenhaTemporaria);

  @ 4. Cria chave de segurança combinada @
  vaChaveSeguranca = vaUsuario + ":" + vaNonce + ":" + vaTokenSessao;
  
  @ 5. Registra sessão @
  vaMensagem = "Sessão criada para: " + vaUsuario;
  Mensagem(Retorna, vaMensagem);
  vaMensagem = "Token: " + vaTokenSessao;
  Mensagem(Retorna, vaMensagem);
  vaMensagem = "Senha temporária: " + vaSenhaTemporaria;
  Mensagem(Retorna, vaMensagem);
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

  @ 2. Data/hora atual formatada para WS-Security @
  Definir Data vdDataAtual;
  DataHoje(vdDataAtual);
  FormatarData(vdDataAtual, "yyyy-MM-ddTHH:mm:ssZ", vaCreated);

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
    Mensagem(Retorna, " Transmissão segura concluída!");
  } Senao {
    Mensagem(Erro, "Falha na integridade dos dados!");
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

**⚠️ Importante:** Para grids/tabelas, use variável intermediária como mostrado em `AlfaParaDecimal`.

### AlfaParaDecimal

Converte um valor alfanumérico para o tipo Decimal.

**Sintaxe:**

```lsp
AlfaParaDecimal(<texto>, <decimal>);
```

**Parâmetros:**
- `texto`: Valor alfanumérico a ser convertido (formato brasileiro com vírgula)
- `decimal`: Variável que receberá o valor convertido

**Exemplo:**

```lsp
Definir Alfa vaTexto;
Definir Numero vnDecimal;

vaTexto = "123,45";  @ Formato brasileiro com vírgula @
AlfaParaDecimal(vaTexto, vnDecimal); @ vnDecimal será 123.45 @
```

**⚠️ Importante para Grids/Tabelas:**

```lsp
@ INCORRETO - Não funciona diretamente em campos de grid @
AlfaParaDecimal(vaTexto, MinhaGrid.CampoDecimal);

@  CORRETO - Use variável intermediária @
Definir Numero vnValor;
AlfaParaDecimal(vaTexto, vnValor);
MinhaGrid.CampoDecimal = vnValor;
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

**⚠️ Importante:** Para grids/tabelas, use variável intermediária como mostrado em `AlfaParaDecimal`.

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

### StrParaInt

Converte um valor alfanumérico (string) para o tipo Inteiro. Esta função é equivalente a `AlfaParaInt` e é mantida para compatibilidade.

**Sintaxe:**

```lsp
StrParaInt(<texto>, <inteiro>);
```

**Parâmetros:**
- `texto`: Valor alfanumérico a ser convertido
- `inteiro`: Variável que receberá o valor convertido

**Exemplo:**

```lsp
Definir Alfa vaTexto;
Definir Numero vnInteiro;

vaTexto = "456";
StrParaInt(vaTexto, vnInteiro); @ vnInteiro será 456 @
```

**⚠️ Importante:** Para grids/tabelas, use variável intermediária como mostrado em `AlfaParaDecimal`.

### IntParaStr

Converte um valor inteiro para o tipo String (Alfanumérico). Esta função é equivalente a `IntParaAlfa` e é mantida para compatibilidade.

**Sintaxe:**

```lsp
IntParaStr(<inteiro>, <texto>);
```

**Parâmetros:**
- `inteiro`: Valor inteiro a ser convertido
- `texto`: Variável alfanumérica que receberá o resultado da conversão

**Exemplo:**

```lsp
Definir Numero vnInteiro;
Definir Alfa vaTexto;

vnInteiro = 789;
IntParaStr(vnInteiro, vaTexto); @ vaTexto será "789" @
```

**⚠️ Importante:** Para grids/tabelas, use variável intermediária como mostrado em `AlfaParaDecimal`.

### ConverteMascara

Esta função converte um valor de entrada (numérico, data, hora ou cadeia de caracteres) para o tipo de dado cadeia de caracteres.

**Sintaxe:**

```lsp
ConverteMascara(<tipoDado>, <valorOrigem>, <alfaDestino>, <mascara>);
```

**Parâmetros:**
- `tipoDado`: Código que determina o tipo do valor de origem
  - `1`: Número
  - `2`: Dinheiro (valor)
  - `3`: Data
  - `4`: Hora
  - `5`: Alfa
- `valorOrigem`: Campo/Variável/Valor a ser convertido
- `alfaDestino`: Variável que receberá o resultado da conversão
- `mascara`: Especifica o formato de apresentação do resultado

**Exemplo de CPF e CNPJ:**

```lsp
Definir Alfa vaInscricaoStr;
Definir Numero vnNumCgc;
Definir Numero vnTipoInscricao;

vnNumCgc = 12345678901;
vnTipoInscricao = 3; @ CPF @

Se (vnTipoInscricao = 1) { @ CNPJ @
  ConverteMascara(1, vnNumCgc, vaInscricaoStr, "99.999.999/9999-99");
} Senao Se (vnTipoInscricao = 3) { @ CPF @
  ConverteMascara(1, vnNumCgc, vaInscricaoStr, "999.999.999-99");
}
@ vaInscricaoStr será "123.456.789-01" @
```

**Observação:** No caso de o tipo de dado ser 5 (Alfa), o parâmetro `valorOrigem` é passado como 0 (zero) e o parâmetro `alfaDestino` receberá o campo do tipo Alfa a ser convertido, e após a conversão, receberá o resultado da conversão.

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

Retorna um número fracionário onde a parte inteira é a data e a fração são as horas. A parte inteira é a quantidade de dias e a parte fracionada representa as horas do dia.

**Sintaxe:**

```lsp
DataHora(<numeroDataHora>);
```

**Parâmetros:**
- `numeroDataHora`: Variável do tipo Numero que receberá a data e hora corrente

**Observação:** Para adicionar horas, minutos e segundos na data, use as frações:
- 1 Hora: 1/24 = 0.04166666666
- 1 Minuto: 1/24/60 = 0.00069444444  
- 1 Segundo: 1/24/60/60 = 0.00001157407

#### DataHoraUTC

Retorna a data em um número fracionário (onde a parte inteira é a data e a fração são as horas) em UTC (Tempo Universal Coordenado).

**Sintaxe:**

```lsp
DataHoraUTC(<numeroDataHoraUTC>);
```

**Parâmetros:**
- `numeroDataHoraUTC`: Variável do tipo Numero que receberá a data e hora corrente UTC

**Observação:** Para adicionar horas, minutos e segundos na data, use as frações:
- 1 Hora: 1/24 = 0.04166666666
- 1 Minuto: 1/24/60 = 0.00069444444
- 1 Segundo: 1/24/60/60 = 0.00001157407

**Exemplo Completo de Obtenção de Datas:**

```lsp
Definir Funcao obterDatasAtuais();

@ Variáveis globais @
Definir Data vdDataAtual;
Definir Numero vnDataHoraAtual;
Definir Numero vnDataHoraUTC;
Definir Alfa vaDataFormatada;
Definir Alfa vaNumeroStr;

obterDatasAtuais();

Funcao obterDatasAtuais(); {
  Definir Alfa vaMensagem;

  @ 1. Obtém apenas a data @
  DataHoje(vdDataAtual);
  FormatarData(vdDataAtual, "dd/MM/yyyy", vaDataFormatada);
  
  @ 2. Obtém data e hora local (número fracionário) @
  DataHora(vnDataHoraAtual);
  IntParaAlfa(vnDataHoraAtual, vaNumeroStr);
  
  @ 3. Obtém data e hora UTC (número fracionário) @
  DataHoraUTC(vnDataHoraUTC);
  
  @ 4. Exibe resultados @
  vaMensagem = "Data atual: " + vaDataFormatada;
  Mensagem(Retorna, vaMensagem);
  vaMensagem = "Data/Hora local (número): " + vaNumeroStr;
  Mensagem(Retorna, vaMensagem);
  
  @ Exemplo de uso das frações para calcular horas @
  Definir Numero vnSomenteParte;
  Definir Numero vnHoras;
  
  @ Calcular apenas a parte fracionária (horas do dia) @
  vnSomenteParte = vnDataHoraAtual - Truncar(vnDataHoraAtual);
  vnHoras = vnSomenteParte * 24;
  
  IntParaAlfa(vnHoras, vaNumeroStr);
  vaMensagem = "Horas do dia: " + vaNumeroStr;
  Mensagem(Retorna, vaMensagem);
}
```

### Manipulação de Componentes de Hora

Existem duas abordagens principais para extrair e manipular componentes de hora do sistema:

#### **⚠️ ATENÇÃO: DataHora retorna NUMERO, não Data**

**DataHora** e **DataHoraUTC** retornam números fracionários, NÃO variáveis do tipo Data. Para formatação com FormatarData, use o número retornado por DataHora diretamente.

#### **🚨 ERRO COMUM: Confundir tipos para FormatarData**

```lsp
@ ❌ INCORRETO: FormatarData NÃO aceita tipo Data @
Definir Data vdData;
DataHoje(vdData);
FormatarData(vdData, "dd/MM/yyyy", vaData);  @ ERRO: FormatarData só aceita Numero @

@ ✅ CORRETO: FormatarData aceita apenas NUMERO (de DataHora) @
Definir Numero vnDataHora;         @ Correto: DataHora retorna Numero @
DataHora(vnDataHora);              @ Correto: Obtém número fracionário @
FormatarData(vnDataHora, "dd/MM/yyyy", vaData);  @ Correto: Funciona! @

@ ✅ ALTERNATIVA: Para datas simples, use DataHoje + outras funções @
Definir Data vdDataAtual;          @ Para comparações e operações @
DataHoje(vdDataAtual);             @ DataHoje retorna tipo Data @
@ Use DecodData, CodData, etc. para manipular vdDataAtual @
```

#### **📋 Guia Rápido: Quando Usar Cada Função**

| **Função** | **Retorna** | **Uso** | **Exemplo** |
|------------|-------------|---------|-------------|
| `DataHoje` | Tipo Data | Comparações, operações com datas | `Se (vdDataVencimento < vdDataAtual)` |
| `DataHora` | Tipo Numero | FormatarData, cálculos matemáticos | `FormatarData(vnDataHora, "dd/MM/yyyy", vaTexto)` |
| `DataHoraUTC` | Tipo Numero | Cálculos UTC, sincronização | `vnUTC = vnDataHoraUTC + (1/24)` @ +1 hora @ |

#### **Abordagem 1: Usando HorSis + CopiarAlfa (Recomendada)**

Método direto para obter componentes específicos da hora atual:

```lsp
Definir Funcao extrairComponentesHora();

@ Variáveis globais @
Definir Alfa vaHoraCompleta;
Definir Alfa vaApenasHora;
Definir Alfa vaApenasMinuto;
Definir Alfa vaApenasSegundo;
Definir Data vdDataAtual;
Definir Alfa vaDataFormatada;

extrairComponentesHora();

Funcao extrairComponentesHora(); {
  Definir Alfa vaMensagem;
  @ Obtém a hora do sistema no formato HH:MM:SS @
  vaHoraCompleta = HorSis;
  
  @ Obtém a data atual @
  DataHoje(vdDataAtual);
  @ Para formatação, use DataHora que retorna Numero @
  Definir Numero vnDataHora;
  DataHora(vnDataHora);
  FormatarData(vnDataHora, "dd/MM/yyyy", vaDataFormatada);
  
  @ Extrai componentes usando CopiarAlfa @
  vaApenasHora = vaHoraCompleta;
  CopiarAlfa(vaApenasHora, 1, 2);     @ Extrai hora (posição 1-2) @
  
  vaApenasMinuto = vaHoraCompleta;
  CopiarAlfa(vaApenasMinuto, 4, 2);   @ Extrai minuto (posição 4-5) @
  
  vaApenasSegundo = vaHoraCompleta;
  CopiarAlfa(vaApenasSegundo, 7, 2);  @ Extrai segundo (posição 7-8) @
  
  @ Exibe resultados @
  vaMensagem = "Data: " + vaDataFormatada;
  Mensagem(Retorna, vaMensagem);
  vaMensagem = "Hora completa: " + vaHoraCompleta;
  Mensagem(Retorna, vaMensagem);
  vaMensagem = "Hora: " + vaApenasHora;
  Mensagem(Retorna, vaMensagem);
  vaMensagem = "Minuto: " + vaApenasMinuto;
  Mensagem(Retorna, vaMensagem);
  vaMensagem = "Segundo: " + vaApenasSegundo;
  Mensagem(Retorna, vaMensagem);
}
```

#### **Abordagem 2: Usando DataHora com Número Fracionário**

Método usando o número fracionário retornado por DataHora para calcular componentes:

```lsp
Definir Funcao extrairComponentesDataHora();

@ Variáveis globais @
Definir Numero vnDataHora;
Definir Numero vnParteInteira;
Definir Numero vnParteFracionaria;
Definir Numero vnHoras;
Definir Numero vnMinutos;
Definir Numero vnSegundos;
Definir Alfa vaHoraFormatada;

extrairComponentesDataHora();

Funcao extrairComponentesDataHora(); {
  @ Obtém data e hora como número fracionário @
  DataHora(vnDataHora);
  
  @ Separa parte inteira (data) da fracionária (hora) @
@ Nota: LSP não tem função Truncar, use conversão para inteiro @
vnParteInteira = vnDataHora;
vnParteFracionaria = vnDataHora - vnParteInteira;

@ Calcula horas, minutos e segundos @
vnHoras = vnParteFracionaria * 24;
vnMinutos = (vnParteFracionaria * 24 - vnHoras) * 60;
vnSegundos = ((vnParteFracionaria * 24 - vnHoras) * 60 - vnMinutos) * 60;
  
  @ Formata resultado @
  Definir Alfa vaHorasStr;
  Definir Alfa vaMinutosStr;
  Definir Alfa vaSegundosStr;
  Definir Alfa vaDataStr;
  
  IntParaAlfa(vnParteInteira, vaDataStr);
  IntParaAlfa(vnHoras, vaHorasStr);
  IntParaAlfa(vnMinutos, vaMinutosStr);
  IntParaAlfa(vnSegundos, vaSegundosStr);
  
  vaHoraFormatada = vaHorasStr + ":" + vaMinutosStr + ":" + vaSegundosStr;
  
  @ Exibe resultados @
  Definir Alfa vaNumeroStr;
  Definir Alfa vaMensagem;
  IntParaAlfa(vnDataHora, vaNumeroStr);
  vaMensagem = "Número fracionário: " + vaNumeroStr;
  Mensagem(Retorna, vaMensagem);
  vaMensagem = "Parte inteira (data): " + vaDataStr;
  Mensagem(Retorna, vaMensagem);
  vaMensagem = "Hora calculada: " + vaHoraFormatada;
  Mensagem(Retorna, vaMensagem);
}
```

#### **Comparação das Abordagens:**

| Aspecto | HorSis + CopiarAlfa | DataHora + Cálculos |
|---------|---------------------|---------------------|
| **Flexibilidade** |  Formato padrão HH:MM:SS | ⚠️ Requer cálculos manuais |
| **Simplicidade** |  Direta e clara | Matemática complexa |
| **Performance** |  Rápida | ⚠️ Múltiplas operações |
| **Precisão** |  Hora formatada |  Cálculo exato |
| **Compatibilidade** |  Tradicional e confiável |  Usa função oficial |

**Recomendação:** Use a **Abordagem 1** (HorSis + CopiarAlfa) para simplicidade, ou **Abordagem 2** (DataHora) quando precisar de cálculos específicos com datas/horas.

### Construção e Decomposição de Datas

#### CodData

Possibilita a composição de uma data, montando-a através de dia, mês e ano.

**Sintaxe:**

```lsp
vdData = CodData(<dia>, <mes>, <ano>);
```

**Parâmetros:**
- `dia`: Valor correspondente ao dia
- `mes`: Valor correspondente ao mês  
- `ano`: Valor correspondente ao ano

**Exemplo:**

```lsp
Definir Data vdData;
Definir Numero vnDia;
Definir Numero vnMes;
Definir Numero vnAno;

vnDia = 10;
vnMes = 1;
vnAno = 2002;

vdData = CodData(vnDia, vnMes, vnAno);
```

#### MontaData

Esta função concatena três variáveis, formando uma data. É uma alternativa ao CodData com sintaxe diferente.

**Sintaxe:**

```lsp
MontaData(<dia>, <mes>, <ano>, <data>);
```

**Parâmetros:**
- `dia`: Dia da data a ser gerada
- `mes`: Mês da data a ser gerada
- `ano`: Ano da data a ser gerada (deve ter 4 dígitos, ex: 1998)
- `data`: Variável do tipo Número ou Data que receberá o resultado

**Exemplo:**

```lsp
Definir Numero vnDia;
Definir Numero vnMes;
Definir Numero vnAno;
Definir Data vdData;

vnDia = 1;
vnMes = 9;
vnAno = 1998;

MontaData(vnDia, vnMes, vnAno, vdData);
@ vdData conterá "01/09/1998" @
```

**Observação:** Quando a variável de retorno for numérica, não será necessário defini-la. No entanto, se for utilizada em um cursor, é obrigatório defini-la como Data.

#### DesMontaData

Esta função desmonta uma data, separando em três variáveis, as informações Dia/Mês/Ano da data.

**Sintaxe:**
```lsp
DesMontaData(<data>, <dia>, <mes>, <ano>);
```

**Parâmetros:**
- `data`: Campo/Variável a ser desmontada
- `dia`: Variável tipo Numero que receberá o dia da data a ser desmontada
- `mes`: Variável tipo Numero que receberá o mês da data a ser desmontada
- `ano`: Variável tipo Numero que receberá o ano da data a ser desmontada

**Exemplo:**
```lsp
Definir Data vdDataEmissao;
Definir Numero vnDia;
Definir Numero vnMes;
Definir Numero vnAno;

vdDataEmissao = E140NFV.DatEmi;
DesMontaData(vdDataEmissao, vnDia, vnMes, vnAno);
@ Se a data fosse 24/04/1995: vnDia=24, vnMes=04, vnAno=1995 @
```

#### ConverteDataBanco

Converter uma data qualquer, para o formato de data do banco de dados.

**Sintaxe:**
```lsp
ConverteDataBanco(<datNum>, <datAlf>);
```

**Parâmetros:**
- `datNum`: É o campo de tabela ou variável que se deseja converter
- `datAlf`: É uma variável que conterá o retorno da conversão

**Exemplo:**
```lsp
Definir Alfa vaDataStr;
Definir Data vdData;

vdData = 31/12/1900;
ConverteDataBanco(vdData, vaDataStr);
@ vaDataStr = "to_date('31/12/1900','DD/MM/YYYY')" ou formato do banco usado @
```

#### ConverteDataSqlSenior2

Converter datas para o formato SQL Senior 2.

**Sintaxe:**
```lsp
ConverteDataSqlSenior2(<datNum>, <datSql>);
```

**Parâmetros:**
- `datNum`: Data a ser convertida
- `datSql`: Data em formato SQL Senior 2 (retorno)

**Exemplo:**
```lsp
Definir Alfa vaSqlAux;
ConverteDataSqlSenior2(DatSis, vaSqlAux);
vaSqlAux = "E000LPA.DATINI = " + vaSqlAux;
InsClauSQLWhere("Detalhe_000LPA", vaSqlAux);
```

**Observações:** Esta função deve ser utilizada em lugar das funções ConverteDataToDB e ConverteDataBanco, quando for necessário inserir uma data em um comando SQL Senior 2.

#### ConverteDataToDB

Converter uma data qualquer, para o formato de data do banco de dados.

**Sintaxe:**
```lsp
ConverteDataToDB(<datNum>, <datAlf>);
```

**Parâmetros:**
- `datNum`: É o campo de tabela ou variável que se deseja converter
- `datAlf`: É uma variável tipo Alfa, que conterá o retorno da conversão

**Exemplo:**
```lsp
Definir Alfa vaDataStr;
Definir Data vdData;

vdData = 31/12/1900;
ConverteDataToDB(vdData, vaDataStr);
@ vaDataStr = "to_date('31/12/1900','DD/MM/YYYY')" ou formato do banco usado @
```

#### AnoBissexto

Esta função tem por objetivo retornar a informação se um ano é ou não bissexto tomando como base o ano da data passada.

**Sintaxe:**
```lsp
AnoBissexto(<data>, <bissexto>);
```

**Parâmetros:**
- `data`: Recebe a data base a ser verificada
- `bissexto`: Retorna a indicação se o ano é bissexto:
  - 0: se o ano não for bissexto
  - 1: se o ano for bissexto

**Exemplo:**
```lsp
Definir Data vdData;
Definir Numero vnBissexto;

vdData = 02/07/2018;
AnoBissexto(vdData, vnBissexto);
@ vnBissexto será 0 (não bissexto) @
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
    
    Definir Alfa vaIdadeStr;
    IntParaAlfa(vnIdade, vaIdadeStr);
    Definir Alfa vaMensagem;
    vaMensagem = "Data válida! Idade aproximada: " + vaIdadeStr;
    Mensagem(Retorna, vaMensagem);
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
  @ Para formatação, converta para número @
  Definir Numero vnDataVencimento;
  vnDataVencimento = vdDataVencimento;
  FormatarData(vnDataVencimento, "dd/MM/yyyy", vaDataVencimentoStr);

  @ Calcula limite (60 dias) @
  AdicionarDias(vdDataBase, 60, vdDataLimite);
  @ Para formatação, converta para número @
  Definir Numero vnDataLimite;
  vnDataLimite = vdDataLimite;
  FormatarData(vnDataLimite, "dd/MM/yyyy", vaDataLimiteStr);
  
  Definir Alfa vaMensagem;
  vaMensagem = "Vencimento: " + vaDataVencimentoStr;
  Mensagem(Retorna, vaMensagem);
  vaMensagem = "Limite: " + vaDataLimiteStr;
  Mensagem(Retorna, vaMensagem);
  
  @ Exemplo com subtração (data passada) @
  AdicionarDias(vdDataBase, -15, vdDataBase);
  @ Para formatação, converta para número @
  Definir Numero vnDataBase;
  vnDataBase = vdDataBase;
  FormatarData(vnDataBase, "dd/MM/yyyy", vaDataVencimentoStr);
    vaMensagem = "15 dias atrás: " + vaDataVencimentoStr;
    Mensagem(Retorna, vaMensagem);
  }
```

### Formatação Avançada de Datas

#### FormatarData

Formata a data em milissegundos gerada pela função DataHora.

**Sintaxe:**

```lsp
FormatarData(<data>, <formato>, <dataFormatada>);
```

**Parâmetros:**
- `data`: Valor numérico da data (tipo Numero)
- `formato`: Formato da data (tipo Alfa)  
- `dataFormatada`: Variável que receberá a data formatada (tipo Alfa)

**⚠️ CRÍTICO - Case Sensitivity das Máscaras:**
- **SEMPRE use letras minúsculas**: `yyyy` para ano, `dd` para dia
- **NUNCA use maiúsculas**: `YYYY` ou `DD` geram datas inválidas!

**Máscaras Suportadas:**
- `dd`: Dia (01-31) ⚠️ **Minúsculo obrigatório**
- `MM`: Mês (01-12)
- `yyyy`: Ano com 4 dígitos ⚠️ **Minúsculo obrigatório**
- `yy`: Ano com 2 dígitos
- `HH`: Hora (00-23)
- `mm`: Minuto (00-59)
- `ss`: Segundo (00-59)

**Exemplo Correto (conforme documentação oficial):**

```lsp
Definir Numero vnDataHora;        @ Tipo NUMERO obrigatório @
Definir Alfa vaDataFormatada;

@ DataHora retorna número fracionário @
DataHora(vnDataHora);

@ FormatarData aceita NUMERO, não Data @
FormatarData(vnDataHora, "yyyy-MM-dd'T'HH:mm:ss'Z'", vaDataFormatada);
@ Resultado: "2024-01-15T14:30:45Z" @
```

**⚠️ ERRO COMUM - Confundir tipos:**

```lsp
@ ❌ INCORRETO - FormatarData NÃO aceita tipo Data @
Definir Data vdData;
DataHoje(vdData);
FormatarData(vdData, "dd/MM/yyyy", vaFormatada); @ ERRO! @

@ ✅ CORRETO - Use DataHora (retorna Numero) @
Definir Numero vnDataHora;
DataHora(vnDataHora);
FormatarData(vnDataHora, "dd/MM/yyyy", vaFormatada); @ Funciona! @
```

**Exemplo de Formatações Diversas:**

⚠️ **IMPORTANTE**: Este exemplo está **INCORRETO** porque `DataHora` retorna um número fracionário, não uma variável do tipo Data. Para usar `FormatarData`, você precisa de variáveis do tipo Data obtidas com `DataHoje` ou `CodData`.

```lsp
Definir Funcao exemploFormatacoes();

@ Variáveis globais @
Definir Data vdDataAtual;
Definir Alfa vaFormatoBR;
Definir Alfa vaFormatoUS;
Definir Alfa vaFormatoISO;
Definir Alfa vaFormatoCompleto;
Definir Alfa vaApenasHora;

DataHoje(vdDataAtual);

exemploFormatacoes();

Funcao exemploFormatacoes(); {
  @ Para formatação, use DataHora que retorna Numero @
  Definir Numero vnDataHora;
  DataHora(vnDataHora);

  @ Formato brasileiro @
  FormatarData(vnDataHora, "dd/MM/yyyy", vaFormatoBR);

  @ Formato americano @
  FormatarData(vnDataHora, "MM/dd/yyyy", vaFormatoUS);

  @ Formato ISO 8601 @
  FormatarData(vnDataHora, "yyyy-MM-dd", vaFormatoISO);
  
  @ ⚠️ NOTA: FormatarData só formata datas, não horas para variáveis do tipo Data @
  @ Para hora atual, use HorSis ou outros métodos @
  vaFormatoCompleto = vaFormatoBR + " " + HorSis;  @ Concatena data + hora sistema @
  vaApenasHora = HorSis;                           @ Hora do sistema @
  
  @ Exibe resultados @
  Definir Alfa vaMensagem;
  vaMensagem = "Brasileiro: " + vaFormatoBR;
  Mensagem(Retorna, vaMensagem);
  vaMensagem = "Americano: " + vaFormatoUS;
  Mensagem(Retorna, vaMensagem);
  vaMensagem = "ISO 8601: " + vaFormatoISO;
  Mensagem(Retorna, vaMensagem);
  vaMensagem = "Completo: " + vaFormatoCompleto;
  Mensagem(Retorna, vaMensagem);
  vaMensagem = "Hora: " + vaApenasHora;
  Mensagem(Retorna, vaMensagem);
}
```

### Funções de Extenso

#### Extenso

Esta função gera o extenso de um valor.

**⚠️ Importante:** Esta função contempla no máximo duas casas decimais após a vírgula. Caso o valor tenha três ou mais casas decimais após a vírgula, ele será arredondado para o valor real de duas.

**Sintaxe:**
```lsp
Extenso(<valor>, <tamanhoLinha1>, <tamanhoLinha2>, <tamanhoLinha3>, <linha1>, <linha2>, <linha3>);
```

**Parâmetros:**
- `valor`: Campo/Variável do qual se deseja obter o extenso
- `tamanhoLinha1`: Quantidade de caracteres que será usado na primeira linha para geração do extenso
- `tamanhoLinha2`: Quantidade de caracteres que será usado na segunda linha para geração do extenso
- `tamanhoLinha3`: Quantidade de caracteres que será usado na terceira linha para geração do extenso
- `linha1`: Variável que receberá a primeira linha do extenso do valor (retorno)
- `linha2`: Variável que receberá a segunda linha do extenso do valor (retorno)
- `linha3`: Variável que receberá a terceira linha do extenso do valor (retorno)

**Exemplo:**
```lsp
Definir Alfa vaExtLin1;
Definir Alfa vaExtLin2;
Definir Alfa vaExtLin3;
Definir Numero vnQuantidade;

vnQuantidade = 1577350;
Extenso(vnQuantidade, 30, 30, 30, vaExtLin1, vaExtLin2, vaExtLin3);
@ vaExtLin1 = "Um milhao, quinhentos e ******" @
@ vaExtLin2 = "setenta e sete mil e *********" @
@ vaExtLin3 = "trezentos e cinquenta reais **" @
```

#### ExtensoMes

Esta função monta o extenso do mês de uma determinada data.

**Sintaxe:**
```lsp
ExtensoMes(<datMon>, <extMes>);
```

**Parâmetros:**
- `datMon`: Campo/Variável do qual se deseja obter o extenso do mês
- `extMes`: Variável tipo Alfa que receberá o extenso do mês

**Exemplo:**
```lsp
Definir Alfa vaMesExt;
Definir Data vdData;

DataHoje(vdData);
ExtensoMes(vdData, vaMesExt);
@ Se a data fosse 31/12/1900, vaMesExt seria "Dezembro" @
```

#### ExtensoMoeda

Esta função gera o extenso de um valor com a moeda informada.

**Sintaxe:**
```lsp
ExtensoMoeda(<vlrExt>, <tamLn1>, <tamLn2>, <tamLn3>, <moeIS>, <moeIP>, <moeDS>, <moeDP>, <extLn1>, <extLn2>, <extLn3>);
```

**Parâmetros:**
- `vlrExt`: Campo/Variável do qual se deseja obter o extenso
- `tamLn1`: Quantidade de caracteres que será usado na primeira linha para geração do extenso
- `tamLn2`: Quantidade de caracteres que será usado na segunda linha para geração do extenso
- `tamLn3`: Quantidade de caracteres que será usado na terceira linha para geração do extenso
- `moeIS`: Moeda, parte inteira no singular
- `moeIP`: Moeda, parte inteira no plural
- `moeDS`: Moeda, parte decimal no singular
- `moeDP`: Moeda, parte decimal no plural
- `extLn1`: Variável que receberá a primeira linha do extenso do valor (retorno)
- `extLn2`: Variável que receberá a segunda linha do extenso do valor (retorno)
- `extLn3`: Variável que receberá a terceira linha do extenso do valor (retorno)

**Exemplo:**
```lsp
Definir Alfa vaExtLin1;
Definir Alfa vaExtLin2;
Definir Alfa vaExtLin3;
Definir Numero vnValorSalario;

vnValorSalario = 1577.95;
ExtensoMoeda(vnValorSalario, 30, 30, 30, "dólar", "dólares", "cent", "cents", vaExtLin1, vaExtLin2, vaExtLin3);
@ vaExtLin1 = "um mil, quinhentos e setenta *" @
@ vaExtLin2 = "e sete dólares e noventa e ***" @
@ vaExtLin3 = "cinco cents ******************" @
```

#### ExtensoSemana

Esta função monta o extenso do dia da semana de uma determinada data.

**Sintaxe:**
```lsp
ExtensoSemana(<datMon>, <extSem>);
```

**Parâmetros:**
- `datMon`: Campo/Variável do qual se deseja obter o extenso da semana
- `extSem`: Variável que receberá o extenso da Semana

**Exemplo:**
```lsp
Definir Alfa vaSemExt;
Definir Data vdData;

DataHoje(vdData);
ExtensoSemana(vdData, vaSemExt);
@ Se a data fosse 31/12/1900, vaSemExt seria "Sexta-Feira" @
```

#### DataExtenso

Esta função gera o extenso de determinada data.

**Sintaxe:**
```lsp
DataExtenso(<data>, <extenso>);
```

**Parâmetros:**
- `data`: Campo/Variável a partir do qual se deseja gerar o extenso
- `extenso`: Variável que retornará o extenso da data

**Exemplo:**
```lsp
Definir Data vdData;
Definir Alfa vaExtenso;

vdData = E210MVP.DatMov;
DataExtenso(vdData, vaExtenso);
@ vaExtenso vai conter a data por extenso @
```

### Operações Matemáticas e Formatação

#### MultiplicaValor

Esta função multiplica um número no formato alfanumérico por um fator de multiplicação numérico e retorna o resultado desta multiplicação em uma variável alfanumérica.

**Sintaxe:**
```lsp
MultiplicaValor(<multiplicando>, <fator>, <retorno>);
```

**Parâmetros:**
- `multiplicando`: Campo/Variável que contém o valor a ser multiplicado
- `fator`: Campo/Variável que contém o fator de multiplicação
- `retorno`: Campo/Variável que retorna o resultado da multiplicação

**Exemplo:**
```lsp
Definir Alfa vaNumOriginal;
Definir Alfa vaNumMultiplicado;
Definir Numero vnFator;

vaNumOriginal = "0000237259400000216555";
vnFator = 5;
MultiplicaValor(vaNumOriginal, vnFator, vaNumMultiplicado);
@ vaNumMultiplicado será "1186297000001082775" @
```

#### ConverteUnidadeMedida

Calcula a quantidade convertida de uma unidade de medida (de) para outra unidade de medida (para).

**Sintaxe:**
```lsp
ConverteUnidadeMedida(<codPro>, <codDer>, <uniMedDe>, <uniMedPara>, <qtde>, <codFor>, <qtdDec>, <codEmp>, <qtdCnv>);
```

**Parâmetros:**
- `codPro`: Variável que indica o código de produto (opcional)
- `codDer`: Variável que indica o código da derivação (opcional)
- `uniMedDe`: Variável que indica a unidade de medida origem (obrigatório)
- `uniMedPara`: Variável que indica a unidade de medida destino (obrigatório)
- `qtde`: Variável que indica a quantidade a ser convertida (obrigatório)
- `codFor`: Variável que indica o código do fornecedor (opcional)
- `qtdDec`: Variável que indica a quantidade de decimais usada na conversão (obrigatório), se não sabe-se a precisão, informar 5
- `codEmp`: Variável que indica o código da empresa (opcional), caso for informado zero, será utilizado a empresa logada
- `qtdCnv`: Variável que retorna a quantidade convertida da unidade de medida origem para a unidade de medida destino

**Exemplo:**
```lsp
Definir Numero vnQtdConv;
ConverteUnidadeMedida("", "", "KM", "M", 100, 0, 3, 0, vnQtdConv);
@ vnQtdConv será 100000 (100 km = 100000 metros) @
```

#### Arredonda

Esta função arredonda um valor, conforme a precisão informada.

**Sintaxe:**
```lsp
Arredonda(<valor>, <decimais>);
```

**Parâmetros:**
- `valor`: Variável que será arredondada
- `decimais`: Variável numérica que indica a quantidade de casas decimais do arredondamento

**Exemplo:**
```lsp
Definir Numero vnValor;
vnValor = 1577.87;
Arredonda(vnValor, 1);
@ vnValor será 1577.90 @

Arredonda(vnValor, 0);
@ vnValor será 1578.00 @
```

#### ArredondaABNT

Esta função aplica a regra de arredondamento da ABNT, conforme a precisão informada.

**Sintaxe:**
```lsp
ArredondaABNT(<valor>, <decimais>);
```

**Parâmetros:**
- `valor`: Variável que será arredondada
- `decimais`: Variável numérica que indica a quantidade de casas decimais do arredondamento

**Regras ABNT:**
- Quando o algarismo a ser conservado for seguido de algarismo inferior a 5, o algarismo a ser conservado permanece sem alteração
- Quando o algarismo a ser conservado for seguido de algarismo superior a 5, ou igual a 5 seguindo de um algorismo diferente de zero, soma-se uma unidade ao algarismo a ser conservado
- Quando o algarismo a ser conservado for ímpar, seguido de 5 e posteriormente de zeros, soma-se uma unidade ao algarismo a ser conservado
- Quando o algarismo a ser conservado for par, seguido de 5 e posteriormente de zeros, o algarismo a ser conservado permanece sem alteração

**Exemplo:**
```lsp
Definir Numero vnValor;
vnValor = 1577.87;
ArredondaABNT(vnValor, 1);
@ vnValor será 1577.90 @

ArredondaABNT(vnValor, 0);
@ vnValor será 1578.00 @
```

#### ArredondarValor

Esta função arredonda determinado valor, conforme a precisão informada.

**Sintaxe:**
```lsp
ArredondarValor(<valorVariavel>, <precisao>);
```

**Parâmetros:**
- `valorVariavel`: Campo ou variável que deseja-se arredondar
- `precisao`: Quantidade de casas decimais para precisão do arredondamento. Se for informado 0 (zero), faz o arredondamento na parte inteira do resultado

**Exemplo:**
```lsp
Definir Numero vnVlrNum;
vnVlrNum = 1577.87;
ArredondarValor(vnVlrNum, 1); @ Retorno será 1577.90 @
ArredondarValor(vnVlrNum, 0); @ Retorno será 1578.00 @
```

#### Arredonda Valor Tipo Acerto

Esta função arredonda um valor tipo acerto, conforme a precisão informada.

**Sintaxe:**
```lsp
Arredonda Valor Tipo Acerto(<valor>, <tipoAcerto>);
```

**Parâmetros:**
- `valor`: Qualquer valor que se deseja arredondar
- `tipoAcerto`: 
  - Tipo 1: O valor passado por parâmetro será arredondado para duas casas decimais
  - Tipo 2: O valor passado por parâmetro será arredondado ignorando a terceira casa decimais

**Exemplo:**
```lsp
Definir Numero vnValor;
vnValor = 1475.12845;
Arredonda Valor Tipo Acerto(vnValor, 1); @ Retorna 1475.13 @
Arredonda Valor Tipo Acerto(vnValor, 2); @ Retorna 1475.12 @
```

#### Formatar

Formata números de acordo com os parâmetros definidos. O formato é o mesmo usado no Borland Delphi 2.0.

**Sintaxe:**
```lsp
<variável> = Formatar(<dado>, "<formato>");
```

**Parâmetros:**
- `dado`: Variável tipo numérica a ser convertida
- `formato`: Formato de conversão. Por exemplo, %3.0f para converter o valor 354 e %3.2f para converter o valor 345,43

**Exemplo:**
```lsp
Definir Alfa vaFmt;
vaFmt = Formatar(123, "%s");
```

#### FormatarN

Formata números com casas decimais de acordo com os parâmetros definidos. O formato é o mesmo usado no Borland Delphi 2.0.

**Sintaxe:**
```lsp
FormatarN(<dado>, "<formato>", "<separador decimal>", <variável>);
```

**Parâmetros:**
- `dado`: Variável tipo numérica a ser convertida
- `formato`: Formato de conversão
- `separador decimal`: Qual será o separador de casas decimais
- `variável`: Armazena o resultado da formatação

**Exemplo:**
```lsp
Definir Alfa vaFmt;
FormatarN(123, "%3.2f", ".", vaFmt);
```

### Arrays e Listas

#### LimpaGerTabAlf

Limpa o conteúdo do Registro GerTabAlf.

**Sintaxe:**
```lsp
LimpaGerTabAlf();
```

**Exemplo:**
```lsp
GerTabAlf[1] = "xxx";
LimpaGerTabAlf();
@ Todos os elementos do GerTabAlf serão limpos @
```

#### LimpaGerTabNum

Limpa o conteúdo do Registro GerTabNum.

**Sintaxe:**
```lsp
LimpaGerTabNum();
```

**Exemplo:**
```lsp
GerTabNum[1] = 1;
LimpaGerTabNum();
@ Todos os elementos do GerTabNum serão limpos @
```

**⚠️ Observação sobre Arrays:** A estrutura do GerTabAlf e GerTabNum não permite múltiplos arrays simultâneos. Como fica em memória, não é possível atribuir valores diferentes para o mesmo indexador. Para trabalhar com múltiplos arrays, é necessário vincular valores diferentes em indexadores diferentes ou considerar o uso de listas dinâmicas.

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
    Mensagem(Retorna, "Período ainda não iniciado");
  } Senao Se ((vdDataAtual >= vdDataInicio) e (vdDataAtual <= vdDataFim)) {
    Mensagem(Retorna, "Período ativo");
  } Senao {
    Mensagem(Retorna, "Fora do período");
  }
}
```

## Manipulação Dinâmica de Variáveis

A LSP oferece funções especializadas para trabalhar com variáveis cujos nomes são construídos dinamicamente durante a execução. Essas funções são úteis quando o nome da variável não é conhecido em tempo de desenvolvimento.

### Verificação de Tipo de Variável

#### PegarTipoVar

Retorna o tipo de uma variável qualquer, passada como string.

**Sintaxe:**

```lsp
PegarTipoVar(<nomeVariavel>, <tipo>);
```

**Parâmetros:**
- `nomeVariavel`: String contendo o nome da variável a ser verificada
- `tipo`: Variável numérica que receberá o código do tipo (retorno)

**Códigos de Retorno:**
- `-1`: Variável não encontrada
- `0`: Variável do tipo Numero
- `1`: Variável do tipo Data
- `2`: Variável do tipo Alfa
- `9`: Variável de outros tipos (Cursor, Lista, etc.)

**Exemplo:**

```lsp
Definir Numero vNum;
Definir Data vDat;
Definir Alfa vAlf;
Definir Cursor vCur;
Definir Numero vTipo;

PegarTipoVar("vNum", vTipo); @ vTipo = 0 @
PegarTipoVar("vDat", vTipo); @ vTipo = 1 @
PegarTipoVar("vAlf", vTipo); @ vTipo = 2 @
PegarTipoVar("vCur", vTipo); @ vTipo = 9 @
PegarTipoVar("vXXX", vTipo); @ vTipo = -1 @
```

### Obtenção de Valores de Variáveis

#### PegarValorVarAlf

Retorna o valor de uma variável alfanumérica identificada por nome.

**Sintaxe:**

```lsp
PegarValorVarAlf(<nomeVariavel>, <valorRetorno>);
```

**Parâmetros:**
- `nomeVariavel`: String contendo o nome da variável
- `valorRetorno`: Variável alfa que receberá o valor

**Exemplo:**

```lsp
Definir Alfa vTexto;
Definir Alfa vValor;
Definir Alfa vNomeVar;

vTexto = "Conteúdo da variável";
vNomeVar = "vTexto";

PegarValorVarAlf(vNomeVar, vValor);
@ vValor será "Conteúdo da variável" @

@ Erro se tentar acessar variável de tipo diferente @
@ PegarValorVarAlf("vnNumero", vValor); @ Gerará erro @
```

#### PegarValorVarNum

Retorna o valor de uma variável numérica ou de data identificada por nome.

**Sintaxe:**

```lsp
PegarValorVarNum(<nomeVariavel>, <valorRetorno>);
```

**Parâmetros:**
- `nomeVariavel`: String contendo o nome da variável
- `valorRetorno`: Variável numérica que receberá o valor

**Exemplo:**

```lsp
Definir Numero vNumero;
Definir Data vData;
Definir Numero vValor;

vNumero = 15;
vData = 39647;

PegarValorVarNum("vNumero", vValor); @ vValor = 15 @
PegarValorVarNum("vData", vValor);   @ vValor = 39647 @
```

### Atribuição de Valores a Variáveis

#### SetarValorVarAlf

Define o valor de uma variável alfanumérica identificada por nome.

**Sintaxe:**

```lsp
SetarValorVarAlf(<nomeVariavel>, <valor>);
```

**Parâmetros:**
- `nomeVariavel`: String contendo o nome da variável
- `valor`: Valor alfa a ser atribuído à variável

**Exemplo:**

```lsp
Definir Alfa vTexto;
Definir Alfa vNovoValor;

vNovoValor = "Novo conteúdo";
SetarValorVarAlf("vTexto", vNovoValor);
@ vTexto agora contém "Novo conteúdo" @
```

#### SetarValorVarNum

Define o valor de uma variável numérica ou de data identificada por nome.

**Sintaxe:**

```lsp
SetarValorVarNum(<nomeVariavel>, <valor>);
```

**Parâmetros:**
- `nomeVariavel`: String contendo o nome da variável
- `valor`: Valor numérico a ser atribuído à variável

**Exemplo:**

```lsp
Definir Numero vNumero;
Definir Data vData;

SetarValorVarNum("vNumero", 100);   @ vNumero = 100 @
SetarValorVarNum("vData", 39685);   @ vData = 39685 @
```

### Exemplo Prático: Acesso Dinâmico a Variáveis

```lsp
Definir Funcao exemploAcessoDinamico();

@ Variáveis globais @
Definir Alfa vaTexto1;
Definir Alfa vaTexto2;
Definir Alfa vaTexto3;
Definir Numero vnNumero1;
Definir Numero vnNumero2;

exemploAcessoDinamico();

Funcao exemploAcessoDinamico(); {
  Definir Numero vnContador;
  Definir Alfa vaNomeVar;
  Definir Alfa vaValor;
  Definir Numero vnTipo;
  Definir Numero vnValorNum;

  @ Inicializar algumas variáveis @
  vaTexto1 = "Primeiro texto";
  vaTexto2 = "Segundo texto";
  vnNumero1 = 100;
  vnNumero2 = 200;

  @ Loop dinâmico para acessar variáveis @
  Para (vnContador = 1; vnContador <= 2; vnContador++) {
    @ Construir nome da variável dinamicamente @
    IntParaAlfa(vnContador, vaValor);
    vaNomeVar = "vaTexto" + vaValor;

    @ Verificar se variável existe e seu tipo @
    PegarTipoVar(vaNomeVar, vnTipo);
    
    Se (vnTipo = 2) { @ Tipo Alfa @
      PegarValorVarAlf(vaNomeVar, vaValor);
      Definir Alfa vaMensagem;
      vaMensagem = "Variável " + vaNomeVar + ": " + vaValor;
      Mensagem(Retorna, vaMensagem);
    } Senao Se (vnTipo = 0) { @ Tipo Numero @
      PegarValorVarNum(vaNomeVar, vnValorNum);
      IntParaAlfa(vnValorNum, vaValor);
      vaMensagem = "Variável " + vaNomeVar + ": " + vaValor;
      Mensagem(Retorna, vaMensagem);
    } Senao Se (vnTipo = -1) {
      vaMensagem = "Variável " + vaNomeVar + " não encontrada";
      Mensagem(Retorna, vaMensagem);
    }
  }
}
```

**⚠️ Observações Importantes:**
- Essas funções devem ser usadas apenas quando o acesso direto não for possível
- Para situações simples, use acesso direto: `vVar = valor` em vez de `SetarValorVarAlf("vVar", valor)`
- Úteis para sistemas de configuração dinâmica e processamento de formulários genéricos
- Sempre verifique o tipo da variável antes de tentar acessar seu valor

## Validação e Verificação

A LSP oferece funções especializadas para validação de dados, verificação de abrangências e controle de qualidade de informações.

### Verificação de Nulidade e Limpeza de Dados

#### EstaNulo

Verifica se uma variável está nula (vazia ou não inicializada).

**Sintaxe:**

```lsp
EstaNulo(<variavel>, <resultado>);
```

**Parâmetros:**
- `variavel`: Variável a ser verificada
- `resultado`: Variável numérica que receberá 1 se nula, 0 se não nula

**Exemplo:**

```lsp
Definir Alfa vaTexto;
Definir Numero vnEhNulo;

EstaNulo(vaTexto, vnEhNulo);
Se (vnEhNulo = 1) {
  Mensagem(Retorna, "Variável está nula");
} Senao {
  Mensagem(Retorna, "Variável contém dados");
}
```

#### DeixaNumeros

Remove todos os caracteres não numéricos de uma string, mantendo apenas os dígitos.

**Sintaxe:**

```lsp
DeixaNumeros(<texto>);
```

**Parâmetros:**
- `texto`: Variável alfa que será modificada, mantendo apenas números

**Exemplo:**

```lsp
Definir Alfa vaCEP;
Definir Alfa vaTelefone;

vaCEP = "86710-180";
DeixaNumeros(vaCEP);
@ vaCEP será "86710180" @

vaTelefone = "(43) 3234-5678";
DeixaNumeros(vaTelefone);
@ vaTelefone será "4332345678" @
```

**Observação:** A função modifica diretamente a variável passada como parâmetro.

### Verificação de Abrangências

#### VrfAbrA

Verifica se um valor alfanumérico está dentro de uma abrangência especificada.

**Sintaxe:**

```lsp
VrfAbrA(<valor>, <abrangencia>, <resultado>);
```

**Parâmetros:**
- `valor`: Valor a ser verificado
- `abrangencia`: Abrangência especificada
- `resultado`: Variável que receberá 1 se válido, 0 se inválido

#### VrfAbrN

Verifica se um valor numérico está dentro de uma abrangência especificada.

**Sintaxe:**

```lsp
VrfAbrN(<valor>, <abrangencia>, <resultado>);
```

**Parâmetros:**
- `valor`: Valor numérico a ser verificado
- `abrangencia`: Abrangência especificada
- `resultado`: Variável que receberá 1 se válido, 0 se inválido

#### MontaAbrangencia

Função utilizada para retornar uma cláusula SQL de acordo com um campo e uma abrangência de valores.

Para montar abrangências de local quando existem valores especiais ("1.1.111==", por exemplo), deve ser utilizado o campo NumLoc nesta função. O campo CodLoc não é tratado pela função nesta situação.

**Sintaxe:**

```lsp
MontaAbrangencia(<tabela>, <valores>, <sqlAbr>);
```

**Parâmetros:**
- `tabela`: Variável que recebe o campo da tabela que vai ser montada a abrangência
- `valores`: Variável que contém a faixa de valores na forma de abrangência
- `sqlAbr`: Variável alfa que retorna a cláusula SQL correspondente à abrangência informada

**Exemplo:**

```lsp
Definir Alfa xCodMot;
Definir Alfa xAbrMot;
Definir Numero Xnumemp;
Definir Numero Xtipcol;
Definir Numero Xnumcad;
Definir Alfa ECodMot;

Xnumemp = R034FUN.NumEmp;
Xtipcol = R034FUN.TipCol;
Xnumcad = R034FUN.NumCad;
ECodMot = "001..999"; @ Exemplo de abrangência @

MontaAbrangencia("R038HSA.CodMot", ECodMot, xCodMot);
XAbrMot = "";

Se (xCodMot <> "( )") {
  XAbrMot = " And " + xCodMot;
}

Chsa.SQL "SELECT * FROM R038HSA WHERE NUMEMP = :xnumemp AND TIPCOL = :xtipcol AND NUMCAD = :xnumcad __Inserir(:xAbrMot) ORDER BY DESC, SEQALT DESC";
```

**Observações:**
- Caso não seja informado nada na variável de abrangência na tela de entrada, esta retornará "( )"
- O comando MontaAbrangencia retorna "( )" quando a abrangência está vazia
- Utilização: Gerador de Relatórios e Regras

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
  Definir Alfa vaMensagem;

vaCodigo = "B";
vnNumero = 150;
vaAbrangenciaAlfa = "A..Z";
vaAbrangenciaNum = "100..200";

validarCodigos();

Funcao validarCodigos(); {
  @ Verifica abrangência alfanumérica @
  VrfAbrA(vaCodigo, vaAbrangenciaAlfa, vnResultadoAlfa);
  Se (vnResultadoAlfa = 1) {
    Definir Alfa vaMensagemCodigo;
    vaMensagemCodigo = "Código '" + vaCodigo + "' válido na abrangência " + vaAbrangenciaAlfa;
    Mensagem(Retorna, vaMensagemCodigo);
  } Senao {
    vaMensagemCodigo = "Código '" + vaCodigo + "' fora da abrangência " + vaAbrangenciaAlfa;
    Mensagem(Erro, vaMensagemCodigo);
  }
  
  @ Verifica abrangência numérica @
  VrfAbrN(vnNumero, vaAbrangenciaNum, vnResultadoNum);
  Se (vnResultadoNum = 1) {
    Definir Alfa vaNumeroStr;
    IntParaAlfa(vnNumero, vaNumeroStr);
    Definir Alfa vaMensagemNumero;
    vaMensagemNumero = " Número " + vaNumeroStr + " válido na abrangência " + vaAbrangenciaNum;
    Mensagem(Retorna, vaMensagemNumero);
  } Senao {
    IntParaAlfa(vnNumero, vaNumeroStr);
    vaMensagemNumero = "Número " + vaNumeroStr + " fora da abrangência " + vaAbrangenciaNum;
    Mensagem(Erro, vaMensagemNumero);
  }
}
```

### Validação de Arquivos

#### ArqExiste

Verifica se um arquivo físico existe no local especificado.

**Sintaxe:**

```lsp
ArqExiste(<caminhoArquivo>, <existe>);
```

**Parâmetros:**
- `caminhoArquivo`: Caminho completo do arquivo
- `existe`: Variável que receberá 1 se existe, 0 se não existe

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
  Definir Alfa vaMensagem;

vaCaminhoArquivo = "C:\\temp\\dados.txt";
vaCaminhoConfig = "C:\\config\\app.ini";
vaCaminhoLog = "C:\\logs\\sistema.log";

verificarArquivos();

Funcao verificarArquivos(); {
  @ Verifica arquivo de dados @
  ArqExiste(vaCaminhoArquivo, vnExisteArquivo);
  Se (vnExisteArquivo = 1) {
    Mensagem(Retorna, "Arquivo de dados encontrado");
  } Senao {
    Definir Alfa vaMensagem;
    vaMensagem = "Arquivo de dados não encontrado: " + vaCaminhoArquivo;
    Mensagem(Erro, vaMensagem);
  }
  
  @ Verifica arquivo de configuração @
  ArqExiste(vaCaminhoConfig, vnExisteConfig);
  Se (vnExisteConfig = 1) {
    Mensagem(Retorna, "Arquivo de configuração encontrado");
  } Senao {
    Mensagem(Retorna, "Arquivo de configuração não encontrado, usando padrão");
  }
  
  @ Verifica arquivo de log @
  ArqExiste(vaCaminhoLog, vnExisteLog);
  Se (vnExisteLog = 0) {
    vaMensagem = "Arquivo de log será criado: " + vaCaminhoLog;
    Mensagem(Retorna, vaMensagem);
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
  Definir Alfa vaMensagem;
  TamanhoAlfa(vaDadosEntrada, vnTamanhoOriginal);
  
  @ Remove expressões perigosas @
  RemoveExpressoesProibidas(vaDadosEntrada, vaDadosLimpos);
  
  TamanhoAlfa(vaDadosLimpos, vnTamanhoLimpo);
  
  Se (vnTamanhoOriginal <> vnTamanhoLimpo) {
    vaMensagem = "Expressões perigosas removidas!";
    Mensagem(Retorna, vaMensagem);
    vaMensagem = "Original: " + vaDadosEntrada;
    Mensagem(Retorna, vaMensagem);
    vaMensagem = "Limpo: " + vaDadosLimpos;
    Mensagem(Retorna, vaMensagem);
  } Senao {
    vaMensagem = " Dados seguros: " + vaDadosLimpos;
    Mensagem(Retorna, vaMensagem);
  }
}
```

### Verificação de Abas Ativas

#### VerificaAbaAtiva

Verifica se uma aba específica está ativa na interface.

**Sintaxe:**

```lsp
VerificaAbaAtiva(<descricaoAba>, <ativa>);
```

**Parâmetros:**
- `descricaoAba`: Descrição da aba a ser verificada
- `ativa`: Variável que receberá 1 se ativa, 0 se não ativa

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
  VerificaAbaAtiva(vaAbaClientes, vnAbaClientesAtiva);
  VerificaAbaAtiva(vaAbaProdutos, vnAbaProdutosAtiva);
  
  Se (vnAbaClientesAtiva = 1) {
    Mensagem(Retorna, "Contexto: Gestão de Clientes");
    @ Lógica específica para clientes @
  } Senao Se (vnAbaProdutosAtiva = 1) {
    Mensagem(Retorna, "Contexto: Gestão de Produtos");
    @ Lógica específica para produtos @
  } Senao {
    Mensagem(Retorna, "Contexto: Genérico");
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
  Definir Alfa vaMensagem;

vaNomeArquivo = "C:\\dados\\cliente.txt";
vaCodigo = "CLI001";
vnNumero = 1500;
DataHoje(vdData);

validacaoCompleta();

Funcao validacaoCompleta(); {
  vnValidacaoGeral = 1; @ Assume válido inicialmente @
  
  @ 1. Verifica arquivo @
  Definir Numero vnArquivoExiste;
  ArqExiste(vaNomeArquivo, vnArquivoExiste);
  Se (vnArquivoExiste = 0) {
    Definir Alfa vaMensagem;
    vaMensagem = "Arquivo não encontrado: " + vaNomeArquivo;
    Mensagem(Erro, vaMensagem);
    vnValidacaoGeral = 0;
  }
  
  @ 2. Verifica código na abrangência @
  Definir Numero vnCodigoValido;
  VrfAbrA(vaCodigo, "CLI001..CLI999", vnCodigoValido);
  Se (vnCodigoValido = 0) {
    vaMensagem = "Código fora da abrangência: " + vaCodigo;
    Mensagem(Erro, vaMensagem);
    vnValidacaoGeral = 0;
  }
  
  @ 3. Verifica número na faixa @
  Definir Numero vnNumeroValido;
  VrfAbrN(vnNumero, "1000..2000", vnNumeroValido);
  Se (vnNumeroValido = 0) {
    Definir Alfa vaNumeroStr;
    IntParaAlfa(vnNumero, vaNumeroStr);
    vaMensagem = "Número fora da faixa: " + vaNumeroStr;
    Mensagem(Erro, vaMensagem);
    vnValidacaoGeral = 0;
  }
  
  @ 4. Resultado final @
  Se (vnValidacaoGeral = 1) {
    Mensagem(Retorna, "Todas as validações passaram!");
  } Senao {
    Mensagem(Erro, "Falha na validação geral do sistema");
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
  Definir Alfa vaMensagem;

vnValorOriginal = 1234.6789;
vnPorcentagem = 15.5;

calculosFinanceiros();

Funcao calculosFinanceiros(); {
  @ Arredonda para 2 casas decimais (padrão monetário) @
  Arredondar(vnValorOriginal, 2, vnValorArredondado);
  Definir Alfa vaValorArredondadoStr;
  IntParaAlfa(vnValorArredondado, vaValorArredondadoStr);
  Definir Alfa vaMensagem;
  vaMensagem = "Valor arredondado: R$ " + vaValorArredondadoStr;
  Mensagem(Retorna, vaMensagem);
  
  @ Trunca para inteiro @
  Truncar(vnValorOriginal, vnValorTruncado);
  Definir Alfa vaValorTruncadoStr;
  IntParaAlfa(vnValorTruncado, vaValorTruncadoStr);
  vaMensagem = "Valor truncado: R$ " + vaValorTruncadoStr;
  Mensagem(Retorna, vaMensagem);
  
  @ Calcula desconto @
  vnDesconto = (vnValorOriginal * vnPorcentagem) / 100;
  Arredondar(vnDesconto, 2, vnDesconto);
  
  @ Valor final @
  vnValorFinal = vnValorOriginal - vnDesconto;
  Arredondar(vnValorFinal, 2, vnValorFinal);
  
  Definir Alfa vaDescontoStr;
  Definir Alfa vaValorFinalStr;
  IntParaAlfa(vnDesconto, vaDescontoStr);
  IntParaAlfa(vnValorFinal, vaValorFinalStr);
  
  vaMensagem = "Desconto aplicado: R$ " + vaDescontoStr;
  Mensagem(Retorna, vaMensagem);
  vaMensagem = "Valor final: R$ " + vaValorFinalStr;
  Mensagem(Retorna, vaMensagem);
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

#### HoraParaMinuto

Converte em minutos os valores que representam hora e minuto.

**Sintaxe:**

```lsp
HoraParaMinuto(<hora>, <minuto>, <minutos>);
```

**Parâmetros:**
- `hora`: Valor correspondente à hora inteira
- `minuto`: Valor correspondente aos minutos de uma hora
- `minutos`: Variável que receberá o total em minutos

**Exemplo:**

```lsp
Definir Numero vnResultado;
Definir Alfa vaResultadoStr;
Definir Alfa vaMensagem;

HoraParaMinuto(1, 30, vnResultado);
IntParaAlfa(vnResultado, vaResultadoStr);

@ vnResultado será 90 (1 hora e 30 minutos = 90 minutos) @
vaMensagem = "Resultado: " + vaResultadoStr + " minutos";
Mensagem(Retorna, vaMensagem);
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
      @ Preparar mensagem da divisão @
  Definir Alfa vaDividendoStr;
  Definir Alfa vaDivisorStr;
  Definir Alfa vaResultadoStr;
  Definir Alfa vaRestoStr;
  Definir Alfa vaMensagem;
  
  IntParaAlfa(vnDividendo, vaDividendoStr);
  IntParaAlfa(vnDivisor, vaDivisorStr);
  IntParaAlfa(vnResultado, vaResultadoStr);
  
  vaMensagem = "Divisão: " + vaDividendoStr + " ÷ " + vaDivisorStr + " = " + vaResultadoStr;
  Mensagem(Retorna, vaMensagem);
  
  @ Resto da divisão @
  RestoDivisao(vnDividendo, vnDivisor, vnResto);
  IntParaAlfa(vnResto, vaRestoStr);
  vaMensagem = "Resto: " + vaRestoStr;
  Mensagem(Retorna, vaMensagem);
  } Senao {
    Mensagem(Erro, "Divisão por zero não permitida!");
  }
  
  @ Verificação de número par/ímpar @
  RestoDivisao(vnNumero, 2, vnResto);
  Definir Alfa vaNumeroStr;
  IntParaAlfa(vnNumero, vaNumeroStr);
  
  Se (vnResto = 0) {
    vaMensagem = " " + vaNumeroStr + " é par";
    Mensagem(Retorna, vaMensagem);
  } Senao {
    vaMensagem = " " + vaNumeroStr + " é ímpar";
    Mensagem(Retorna, vaMensagem);
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
    Definir Alfa vaTotalRegistrosStr;
    IntParaAlfa(vnTotalRegistros, vaTotalRegistrosStr);
    vaMensagem = "Processando registro " + vaRegistroStr + " de " + vaTotalRegistrosStr;
    
    @ Atualiza barra @
    AtualizaBarraProgresso(vnPercentual, vaMensagem);
    
    @ Simula tempo de processamento @
    sleep(50); @ Pausa 50ms @
    
    @ Simula erro no meio do processo @
    Se (vnRegistroAtual = 50) {
      AtualizaBarraProgresso(50, "Problema detectado, continuando...");
      sleep(1000); @ Pausa 1 segundo @
    }
  }
  
  @ Finaliza @
  AtualizaBarraProgresso(100, " Processamento concluído!");
  sleep(1000);
  FinalizaBarraProgresso();
  
  IntParaAlfa(vnTotalRegistros, vaTotalRegistrosStr);
  vaMensagem = "Processamento de " + vaTotalRegistrosStr + " registros concluído!";
  Mensagem(Retorna, vaMensagem);
}
```

### Controle de Interface

#### ObterVersaoSistema

Esta função retorna a versão do sistema Senior.

**Sintaxe:**

```lsp
ObterVersaoSistema(<majorVersion>, <minorVersion>, <release>, <build>);
```

**Parâmetros:**
- `majorVersion`: Versão de primeiro dígito do sistema
- `minorVersion`: Versão de segundo dígito do sistema
- `release`: Versão de terceiro dígito do sistema (release)
- `build`: Versão de quarto dígito do sistema (build)

**Exemplo:**

```lsp
Definir Numero vnMajorVersion;
Definir Numero vnMinorVersion;
Definir Numero vnRelease;
Definir Numero vnBuild;
Definir Alfa vaMensagem;

ObterVersaoSistema(vnMajorVersion, vnMinorVersion, vnRelease, vnBuild);

@ Após a chamada da função as variáveis conterão a versão do sistema @
Definir Alfa vaMajorStr;
Definir Alfa vaMinorStr;
Definir Alfa vaReleaseStr;
Definir Alfa vaBuildStr;

IntParaAlfa(vnMajorVersion, vaMajorStr);
IntParaAlfa(vnMinorVersion, vaMinorStr);
IntParaAlfa(vnRelease, vaReleaseStr);
IntParaAlfa(vnBuild, vaBuildStr);

vaMensagem = "Versão: " + vaMajorStr + "." + vaMinorStr + "." + vaReleaseStr + "." + vaBuildStr;
Mensagem(Retorna, vaMensagem);
```

#### ObtemIdiomaAtivo

Retorna o código do idioma utilizado pelo usuário.

**Sintaxe:**

```lsp
ObtemIdiomaAtivo(<valorIdioma>);
```

**Parâmetros:**
- `valorIdioma`: Campo ou variável que receberá o valor de retorno do idioma utilizado (ex: "PTBRN")

**Exemplo:**

```lsp
Definir Alfa vaValorIdioma;

ObtemIdiomaAtivo(vaValorIdioma);
Definir Alfa vaMensagemIdioma;
vaMensagemIdioma = "Idioma ativo: " + vaValorIdioma;
Mensagem(Retorna, vaMensagemIdioma);
```

#### sleep

Pausa a execução por um número especificado de milissegundos. Útil para simular tempo de processamento, aguardar operações ou criar delays controlados.

**Sintaxe:**

```lsp
sleep(<milissegundos>);
```

**Parâmetros:**
- `milissegundos`: Número de milissegundos para pausar a execução

**Exemplos:**

```lsp
@ Pausa de 1 segundo @
sleep(1000);

@ Pausa de 5 segundos @
sleep(5000);

@ Pausa de 100 milissegundos @
sleep(100);
```

**Exemplo com Barra de Progresso:**

```lsp
Definir Funcao exemploComSleep();

exemploComSleep();

Funcao exemploComSleep(); {
  IniciaBarraProgresso("Processamento", "Iniciando...");
  
  @ Simula processamento em etapas @
  AtualizaBarraProgresso(25, "Processando etapa 1...");
  sleep(2000); @ Pausa de 2 segundos @
  
  AtualizaBarraProgresso(50, "Processando etapa 2...");
  sleep(2000); @ Pausa de 2 segundos @
  
  AtualizaBarraProgresso(75, "Processando etapa 3...");
  sleep(2000); @ Pausa de 2 segundos @
  
  AtualizaBarraProgresso(100, "Concluído!");
  sleep(1000); @ Pausa de 1 segundo @
  
  FinalizaBarraProgresso();
  Mensagem(Retorna, "Processamento concluído!");
}
```

**Observações:**
- Use com moderação para não impactar a performance
- Útil em simulações e testes
- Valores muito altos podem travar a interface do usuário

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
  Definir Alfa vaEnter;
  CaracterParaAlfa(13, vaEnter);
  
  vaInformacoes = "=== INFORMAÇÕES DO SISTEMA ===" + vaEnter;
  vaInformacoes = vaInformacoes + "Versão: " + vaVersaoSistema + vaEnter;
  vaInformacoes = vaInformacoes + "Idioma: " + vaIdiomaAtivo + vaEnter;
  vaInformacoes = vaInformacoes + "Usuário: " + NomUsu + vaEnter;
  vaInformacoes = vaInformacoes + "Empresa: " + Empresa + vaEnter;
  vaInformacoes = vaInformacoes + "Data: " + ExtSis;
  
  Mensagem(Retorna, vaInformacoes);
}
```

### Gerenciamento de Configuração

#### RetornaValorCFG

Responsável por retornar para a regra o valor de uma determinada chave da Central de Configuração Senior que está sendo utilizada pelo sistema.

**Sintaxe:**

```lsp
RetornaValorCFG(<chave>, <retorno>);
```

**Parâmetros:**
- `chave`: Nome da chave de configuração. Pode conter:
  - Nome completo da chave
  - Parte final de uma chave
  - Diretórios especiais: LOGS, TBS, IMAGENS, ARQUIVOS, GRAFICOS, IMPEXP, CONSULTAS, REGRAS, CUBOS, MODELOS, TBS_TRANSLATION_FILTER_FILE
- `retorno`: Variável que receberá o valor da chave

**Exemplos:**

```lsp
Definir Alfa vaChave;
Definir Alfa vaRetorno;
Definir Alfa vaMensagem;

@ Obter diretório de logs @
vaChave = "LOGS";
RetornaValorCFG(vaChave, vaRetorno);
@ Retorna algo como "\\servidor\ERP\Sapiens\Logs" @
vaMensagem = "Diretório de logs: " + vaRetorno;
Mensagem(Retorna, vaMensagem);

@ Obter chave específica @
vaChave = "com.senior.printers.path";
RetornaValorCFG(vaChave, vaRetorno);
@ Retorna algo como "\\servidor\ERP\Impressoras" @
vaMensagem = "Diretório de impressoras: " + vaRetorno;
Mensagem(Retorna, vaMensagem);
```

**Observações:**
- Caso o valor da chave esteja em branco, o valor retornado é "( NULO )"
- Se informada apenas a parte final do nome da chave, será retornado o valor da primeira chave localizada que contenha a parte final informada
- Não é permitida a visualização da chave PASSWORD do arquivo CFG

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
  Definir Alfa vaMensagem;
  @ Carrega timeout da requisição @
  RetornaValorCFG(vaChaveTimeout, vaValorTimeout);
  Se (TamanhoAlfa(vaValorTimeout) > 0) {
    AlfaParaInt(vaValorTimeout, vnTimeout);
    vaMensagem = "Timeout configurado: " + vaValorTimeout + "ms";
    Mensagem(Retorna, vaMensagem);
  } Senao {
    vnTimeout = 30000; @ Padrão: 30 segundos @
    Mensagem(Retorna, "Timeout não configurado, usando padrão: 30000ms");
  }
  
  @ Carrega modo debug @
  RetornaValorCFG(vaChaveDebug, vaValorDebug);
  Se (vaValorDebug = "true") {
    Mensagem(Retorna, "Modo debug ativado");
  } Senao {
    Mensagem(Retorna, "Modo debug desativado");
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

Conta o número de linhas em um arquivo através de parâmetro de retorno.

**Sintaxe:**

```lsp
LinhasArquivo(<caminhoArquivo>, <linhas>);
```

**Parâmetros:**
- `caminhoArquivo`: Caminho do arquivo a ser analisado
- `linhas`: Variável que receberá a quantidade de linhas

**Exemplo de Processamento de Arquivo Temporário:**

```lsp
Definir Funcao processarArquivoTemporario();

  @ Variáveis globais @
  Definir Alfa vaCaminhoTemp;
  Definir Numero vnArquivo;
  Definir Numero vnLinhas;
  Definir Alfa vaConteudo;
  Definir Numero vnContador;
  Definir Alfa vaQuantidadeStr;
  Definir Alfa vaMensagem;

processarArquivoTemporario();

Funcao processarArquivoTemporario(); {
  @ 1. Cria arquivo temporário @
  CriarArquivoTemporario("processamento_", vaCaminhoTemp);
  vaMensagem = "Arquivo temporário criado: " + vaCaminhoTemp;
  Mensagem(Retorna, vaMensagem);
  
  @ 2. Escreve dados no arquivo @
  vnArquivo = Abrir(vaCaminhoTemp, Gravarnl);
  Para (vnContador = 1; vnContador <= 10; vnContador++) {
    vaConteudo = "Linha " + IntParaAlfa(vnContador) + " do arquivo temporário";
    Gravarnl(vnArquivo, vaConteudo);
  }
  Fechar(vnArquivo);
  
  @ 3. Verifica o arquivo criado @
  LinhasArquivo(vaCaminhoTemp, vnLinhas);
  IntParaAlfa(vnLinhas, vaQuantidadeStr);
  vaMensagem = "Arquivo criado com " + vaQuantidadeStr + " linhas";
  Mensagem(Retorna, vaMensagem);
  
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
  Mensagem(Retorna, "Arquivo temporário removido");
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
  Definir Alfa vaMensagem;
  @ 1. Abre arquivo no Bloco de Notas @
  vaComando = "notepad.exe";
  vaParametros = vaCaminhoArquivo;
  
  Se (ArqExiste(vaCaminhoArquivo) = 1) {
    ExecProg(vaComando, vaParametros, 0); @ Não aguarda terminar @
    vaMensagem = "Arquivo aberto no Bloco de Notas";
    Mensagem(Retorna, vaMensagem);
  } Senao {
    vaMensagem = "Arquivo não encontrado: " + vaCaminhoArquivo;
    Mensagem(Erro, vaMensagem);
  }
  
  @ 2. Abre explorador de arquivos @
  vaComando = "explorer.exe";
  vaParametros = "C:\\temp";
  ExecProg(vaComando, vaParametros, 0);
  Mensagem(Retorna, "Explorador de arquivos aberto");
  
  @ 3. Executa comando do sistema @
  vaComando = "cmd.exe";
  vaParametros = "/c dir C:\\temp > C:\\temp\\listagem.txt";
  ExecProg(vaComando, vaParametros, 1); @ Aguarda terminar @
  Mensagem(Retorna, "Listagem de arquivos gerada");
}
```

## ⚠️ **LIMITAÇÕES CRÍTICAS DA LSP**

> **🚨 ATENÇÃO:** Esta seção é **OBRIGATÓRIA** para todos os desenvolvedores LSP!

### **📚 Resumo Executivo das Limitações**

| **Limitação** | **Problema** | ** Solução** |
|---|---|---|
| **Parâmetros** | Não aceita operações dentro de parâmetros | Faça operações antes, passe resultado |
| **Retorno** | Funções usam parâmetros de retorno | Use variável de retorno, não `=` |
| **Grids** | Conversões diretas falham | Use variável intermediária |
| **Nomenclatura** | Nomes devem seguir padrão | Use prefixos: va, vn, vd |

---

### **🚫 Limitação #1: Manipulação em Parâmetros**

**A LSP NÃO suporta manipulações/operações dentro dos parâmetros de funções**

#### **❌ Operações NÃO Permitidas nos Parâmetros:**

- **Concatenação** com operador `+`
- **Chamadas de função** dentro de parâmetros
- **Operações matemáticas** (`*`, `/`, `-`, etc.)
- **Conversões de tipo** (`IntParaAlfa`, `AlfaParaInt`, etc.)

### **❌ Exemplos INCORRETOS:**

```lsp
@ ERRO: Concatenação no parâmetro @
Mensagem(Retorna, "Resultado: " + vaValor + " pontos");

@ ERRO: Função dentro de parâmetro @
Mensagem(Retorna, "Idade: " + IntParaAlfa(vnIdade));

@ ERRO: Operação matemática no parâmetro @
SubstAlfa("]}", vaObjeto + "]}", vaTexto);

@ ERRO: Múltiplas concatenações @
Mensagem(Retorna, vaNome + " - " + vaEmail + " (" + IntParaAlfa(vnId) + ")");
```

### **✅ Forma CORRETA:**

```lsp
@ CORRETO: Fazer manipulações antes @
Definir Alfa vaMensagem;
Definir Alfa vaIdade;

IntParaAlfa(vnIdade, vaIdade);
vaMensagem = "Resultado: " + vaValor + " pontos";
Mensagem(Retorna, vaMensagem);

@ CORRETO: Para SubstAlfa @
vaObjeto = vaObjeto + "]}";
SubstAlfa("]}", vaObjeto, vaTexto);

@ CORRETO: Para múltiplas concatenações @
vaMensagem = vaNome + " - " + vaEmail + " (" + vaIdade + ")";
Mensagem(Retorna, vaMensagem);
```

### **🎯 Regra de Ouro:**
**Sempre faça as manipulações ANTES de passar para a função!**

### **⚠️ ATENÇÃO ESPECIAL: Função Mensagem**

A função `Mensagem` é **extremamente sensível** a esta limitação. É muito fácil cometer erro:

```lsp
@ MUITO COMUM mas INCORRETO @
Mensagem(Retorna, "Total: " + vaTexto + " itens");
Mensagem(Erro, "Erro no produto: " + vaProduto);
Mensagem(Retorna, "Valor: " + IntParaAlfa(vnValor));

@  CORRETO @
Definir Alfa vaMensagem;
vaMensagem = "Total: " + vaTexto + " itens";
Mensagem(Retorna, vaMensagem);

vaMensagem = "Erro no produto: " + vaProduto;
Mensagem(Erro, vaMensagem);

Definir Alfa vaValorStr;
IntParaAlfa(vnValor, vaValorStr);
vaMensagem = "Valor: " + vaValorStr;
Mensagem(Retorna, vaMensagem);
```

### **🚨 LIMITAÇÃO CRÍTICA: JSON e Dados Grandes**

**NUNCA** passe dados JSON grandes ou strings muito extensas para `Mensagem`:

```lsp
@ PERIGOSO - Pode travar o sistema @
Mensagem(Retorna, vaJSONResposta);  @ JSON grande @
Mensagem(Retorna, vaXMLCompleto);   @ XML grande @
Mensagem(Retorna, vaLogCompleto);   @ Log extenso @

@  SEGURO - Mostrar apenas informações resumidas @
Definir Alfa vaMensagem;
Definir Numero vnTamanho;
Definir Alfa vaTamanhoStr;
TamanhoAlfa(vaJSONResposta, vnTamanho);
IntParaAlfa(vnTamanho, vaTamanhoStr);
vaMensagem = "JSON recebido com " + vaTamanhoStr + " caracteres";
Mensagem(Retorna, vaMensagem);

@  SEGURO - Mostrar apenas parte do conteúdo @
Definir Alfa vaJSONTrecho;
vaJSONTrecho = vaJSONResposta;
CopiarAlfa(vaJSONTrecho, 1, 50);
vaMensagem = "JSON início: " + vaJSONTrecho + "...";
Mensagem(Retorna, vaMensagem);
```

### **🚫 Retorno Direto de Funções**

**A maioria das funções LSP NÃO retorna valores diretamente - elas usam parâmetros de retorno**

#### **❌ Sintaxe INCORRETA:**

```lsp
@ ERRO: Tentativa de retorno direto @
vnTamanho = TamanhoAlfa(vaTexto);
vnPosicao = PosicaoAlfa("@", vaEmail);
vnLinhas = LinhasArquivo(vaCaminho);
vnExiste = ArqExiste(vaCaminho);
vnQuantidade = ListaQuantidade(vaLista, ",");
vnResultado = HoraParaMinuto(1, 30);
vnValido = VrfAbrA(vaCodigo, "A..Z");
vnAtiva = VerificaAbaAtiva(vaDescricao);

@ ERRO MUITO COMUM: Usar em condicionais @
Se (TamanhoAlfa(vaCNPJ) <> 14) {
  Mensagem(Erro, "CNPJ deve ter 14 dígitos");
}

Se (ArqExiste(vaCaminho)) {
  Mensagem(Retorna, "Arquivo encontrado");
}
```

#### ** Sintaxe CORRETA:**

```lsp
@ CORRETO: Usar parâmetro de retorno @
TamanhoAlfa(vaTexto, vnTamanho);
PosicaoAlfa("@", vaEmail, vnPosicao);
LinhasArquivo(vaCaminho, vnLinhas);
ArqExiste(vaCaminho, vnExiste);
ListaQuantidade(vaLista, ",", vnQuantidade);
HoraParaMinuto(1, 30, vnResultado);
VrfAbrA(vaCodigo, "A..Z", vnValido);
VerificaAbaAtiva(vaDescricao, vnAtiva);

@ CORRETO: Usar em condicionais @
Definir Numero vnTamanhoCNPJ;
TamanhoAlfa(vaCNPJ, vnTamanhoCNPJ);
Se (vnTamanhoCNPJ <> 14) {
  Mensagem(Erro, "CNPJ deve ter 14 dígitos");
}

Definir Numero vnArquivoExiste;
ArqExiste(vaCaminho, vnArquivoExiste);
Se (vnArquivoExiste = 1) {
  Mensagem(Retorna, "Arquivo encontrado");
}
```

#### ** Exceções - Funções que RETORNAM diretamente:**

```lsp
@ Estas funções SIM retornam valores diretamente @
vnRetorno = ConverteCodificacaoString(vaTexto, "UTF-8", vaDestino);
vnArquivo = Abrir("arquivo.txt", Ler);
vdData = CodData(vnDia, vnMes, vnAno);
vnRetorno = Mensagem(Retorna, "Mensagem [&Ok,&Cancelar]");
vnNulo = SQL_RetornarSeNulo(xCursor, "CAMPO");
vnTem = Lst.Primeiro();
vnTem = Lst.Proximo();
```

#### **📋 Resumo - Funções que usam PARÂMETRO DE RETORNO:**

| **Categoria** | **Funções** |
|---|---|
| **Strings** | `TamanhoAlfa`, `TamanhoStr`, `PosicaoAlfa`, `PosicaoStr`, `ListaQuantidade` |
| **Validação** | `VrfAbrA`, `VrfAbrN`, `ArqExiste`, `VerificaAbaAtiva`, `EstaNulo` |
| **Sistema** | `LinhasArquivo`, `HoraParaMinuto`, `ObtemIdiomaAtivo`, `RetornaValorCFG` |
| **Conversão** | `AlfaParaDecimal`, `AlfaParaInt`, `AlfaParaData`, `IntParaAlfa` |
| **Manipulação Dinâmica** | `PegarTipoVar`, `PegarValorVarAlf`, `PegarValorVarNum` |

### **🚫 Atribuição Direta em Grids/Tabelas**

**Funções de conversão NÃO podem atribuir diretamente para campos de grids ou tabelas**

#### **Operações NÃO Permitidas:**

- **Atribuição direta** em campos de grid/tabela
- **Conversões diretas** para propriedades de objetos
- **Funções de cast** diretamente em campos estruturados

#### **Exemplos INCORRETOS:**

```lsp
@ ERRO: Atribuição direta em grid @
AlfaParaDecimal(vaTexto, MinhaGrid.CampoDecimal);
AlfaParaInt(vaTexto, MinhaTabela.CampoInteiro);
AlfaParaData(vaTexto, MinhaGrid.CampoData);
```

#### ** Forma CORRETA:**

```lsp
@ CORRETO: Usar variável intermediária @
Definir Numero vnValorDecimal;
Definir Numero vnValorInteiro;
Definir Data vdDataConvertida;

AlfaParaDecimal(vaTexto, vnValorDecimal);
MinhaGrid.CampoDecimal = vnValorDecimal;

AlfaParaInt(vaTexto, vnValorInteiro);
MinhaTabela.CampoInteiro = vnValorInteiro;

AlfaParaData(vaTexto, vdDataConvertida);
MinhaGrid.CampoData = vdDataConvertida;
```

#### **🎯 Regra de Ouro para Grids:**
**Sempre use variável intermediária para conversões em grids/tabelas!**

## Mensagens

A função `Mensagem` é utilizada para exibir mensagens ao usuário. Existem diferentes tipos de mensagens, como `Retorna`, `Erro`, e `Refaz`.

**📋 Regras Importantes:**
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

**⚠️ FUNDAMENTAL:** A função `Mensagem` **NÃO aceita concatenação ou qualquer manipulação** dentro de seus parâmetros. **Sempre** faça a concatenação em uma variável separada primeiro.

**🚨 CRÍTICO:** **NUNCA** passe variáveis contendo **JSON grandes** para `Mensagem`. Pode causar **travamento do sistema Senior**.

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
@ ERRO: Concatenação no parâmetro - NÃO FUNCIONA @
Mensagem(Retorna, "Aluno: " + vaNome + vaEnter + "Média: " + vaMedia);
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

✅ **Sempre termine uma instrução de código com `;`.**
✅ **Evite duplicação de código, reutilize funções sempre que possível.**
✅ **Mantenha o código modularizado e organizado em funções.**
✅ **Utilize nomes descritivos para funções.**
✅ **Teste o código extensivamente para garantir que ele funcione corretamente em todas as situações esperadas.**

### Declaração de Variáveis

✅ **Declare as variáveis no início do código ou da função.**
✅ **Inicialize as variáveis sempre que possível no início do código ou da função.**
✅ **Em relatórios, declare e inicialize variáveis nos eventos de Inicialização ou Pré-Seleção.**

### Padrão de Nomenclatura de Variáveis

✅ **Utilize nomes descritivos para as variáveis.**
✅ **Utilize o padrão CamelCase nos nomes das variáveis.**
✅ **Utilize o padrão "v + inicial do tipo de dado" antes do nome da variável:**
  - `va` para variáveis do tipo `Alfa`
  - `vn` para variáveis do tipo `Numero`
  - `vd` para variáveis do tipo `Data`
❌ **Evite usar nomes de variáveis que possam ser confundidos com palavras reservadas ou nomes de funções.**

### Identação e Espaçamento

✅ **Utilize 2 espaços para identação.**
✅ **Mantenha o código organizado e legível, evitando linhas de código muito longas.**

### Estruturas de Bloco

✅ **Utilize `{` para abrir um bloco e `}` para fechar um bloco, delimitando assim os blocos de código.**
✅ **Se o bloco contiver apenas uma linha, não é necessário informar `{ }`, basta adicionar o código identado na linha de baixo.**

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

✅ **Utilize comentários para explicar o código e facilitar a manutenção.**
✅ **Utilize `@` para comentários de uma linha e `/* */` para comentários de múltiplas linhas.**

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

### **📋 Resumo das Estruturas de Controle**

| **Estrutura** | **Uso** | **Sintaxe** |
|---|---|---|
| **🔀 Se/Senao** | Decisões | `Se (condição) { } Senao { }` |
| **🔄 Para** | Loop contado | `Para (i=1; i<=10; i++) { }` |
| **🔁 Enquanto** | Loop condicional | `Enquanto (condição) { }` |
| **⏹️ Pare** | Interromper loop | `Pare;` |
| **↩️ VaPara** | Pular para rótulo | `VaPara etiqueta;` |

### **🎯 Condicionais Progressivos**

#### **Nível 1: Condicional Simples**
```lsp
Definir Numero vnIdade;
vnIdade = 20;

Se (vnIdade >= 18) {
  Mensagem(Retorna, "Maior de idade");
} Senao {
  Mensagem(Retorna, "Menor de idade");
}
```

#### **Nível 2: Múltiplas Condições**
```lsp
Definir Numero vnNota;
Definir Alfa vaConceito;
Definir Alfa vaMensagem;

vnNota = 85;

Se (vnNota >= 90) {
  vaConceito = "Excelente";
} Senao Se (vnNota >= 80) {
  vaConceito = "Bom";
} Senao Se (vnNota >= 70) {
  vaConceito = "Regular";
} Senao Se (vnNota >= 60) {
  vaConceito = "Suficiente";
} Senao {
  vaConceito = "Insuficiente";
}

vaMensagem = "Conceito: " + vaConceito;
Mensagem(Retorna, vaMensagem);
```

#### **Nível 3: Condições Complexas**
```lsp
Definir Numero vnIdade;
Definir Alfa vaCategoria;
Definir Numero vnRenda;
Definir Numero vnPontuacao;

vnIdade = 25;
vaCategoria = "PREMIUM";
vnRenda = 5000;

Se ((vnIdade >= 18) e (vnIdade <= 65) e (vaCategoria = "PREMIUM") e (vnRenda > 3000)) {
  vnPontuacao = 100;
  Mensagem(Retorna, " Cliente aprovado com pontuação máxima!");
} Senao Se ((vnIdade >= 18) e (vnRenda > 1500)) {
  vnPontuacao = 70;
  Mensagem(Retorna, "Cliente aprovado com restrições");
} Senao {
  vnPontuacao = 0;
  Mensagem(Retorna, "Cliente não aprovado");
}
```

### Estrutura de Repetição

As estruturas de repetição são utilizadas para executar blocos de código repetidamente.

Exemplo de uso do `Enquanto`:

```lsp
Definir Numero vnContador;
Definir Alfa vaContadorStr;
vnContador = 0;

Enquanto (vnContador < 10) {
  IntParaAlfa(vnContador, vaContadorStr);
  Mensagem(Retorna, vaContadorStr);
  vnContador++;
}
```

Exemplo de uso do `Para`:

```lsp
Definir Alfa vaIStr;
Para (i = 0; i < 10; i++) {
  IntParaAlfa(i, vaIStr);
  Mensagem(Retorna, vaIStr);
}
```

### Pare

O comando `Pare` é utilizado para interromper a execução de um bloco de repetição.

Exemplo de uso do `Pare`:

```lsp
Definir Alfa vaContadorStr;
Para (vnContador = 0; vnContador < 10; vnContador++) {
  Se (vnContador = 5) {
    Pare;
  }
  IntParaAlfa(vnContador, vaContadorStr);
  Mensagem(Retorna, vaContadorStr);
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
Definir Alfa vaIdadeStr;
IntParaAlfa(vnIdades[1], vaIdadeStr);
Mensagem(Retorna, vaIdadeStr); @ Exibe 30 @
Mensagem(Retorna, vdDatas[2]); @ Exibe "10/10/2022" @
```

### Iteração sobre Arrays

Os arrays podem ser iterados utilizando estruturas de repetição como `Para` ou `Enquanto`.

Exemplo de iteração sobre arrays:

```lsp
Definir Alfa vaIdadeStr;

Para (i = 0; i < 3; i++) {
  Mensagem(Retorna, vaNomes[i]);
}

Definir Numero j;
j = 0;
Enquanto (j < 3) {
  IntParaAlfa(vnIdades[j], vaIdadeStr);
  Mensagem(Retorna, vaIdadeStr);
  j++;
}
```

### Exemplo Completo

Aqui está um exemplo completo de declaração, atribuição, acesso e iteração sobre arrays:

```lsp
Definir Alfa vaNomes[3];
Definir Numero vnIdades[3];
Definir Data vdDatas[3];
Definir Alfa vaIdadeStr;

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
  IntParaAlfa(vnIdades[j], vaIdadeStr);
  Mensagem(Retorna, vaIdadeStr);
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

### Disponibilização do Recurso

Recurso disponível para SVCL em todas as ferramentas e telas que utilizem regras.

### Cursores vs Listas em Memória

#### Cursores

Os cursores são melhores utilizados quando precisa-se de dados atualizados ou que serão lidos apenas uma vez.

**Vantagens:**
✅ **Permite acesso a dados atualizados**
✅ **Permite filtragem dos dados diretamente no banco de dados**
✅ **Filtros elaborados através de expressões (cláusula where)**

**Desvantagens:**
❌ **A performance de resposta depende da rede e do banco de dados**
❌ **Não suporta o comando Anterior, permitindo que os registros sejam lidos de trás para a frente**
❌ **Para se alterar a ordenação, precisa-se executar outro comando SQL**

#### Listas em Memória

As listas em memória podem ser usadas quando precisa-se navegar muitas vezes nos dados ou quando é necessário armazenar dados calculados. Também pode ser usada quando é necessário armazenar valores durante um processamento (onde não se sabe o número total de registros) e que, posteriormente, precisam ser recuperados para uma impressão ou algum outro processamento.

**Vantagens:**
✅ **Acesso rápido aos dados**
✅ **A liberação da memória é de responsabilidade da lista, não cabendo ao usuário a chamada de um comando para isto. Pode-se apenas excluir os registros. Isto pode ser feito individualmente, ou através do comando Limpar (que remove todos os registros da lista)**
✅ **A ordenação pode ser realizada em qualquer momento, apenas configurando a chave da lista**
✅ **Ordenação facilitada através da definição de uma chave, sem a necessidade de ler novamente os dados**
✅ **Permite a inserção, atualização e exclusão de registros durante o uso**
✅ **Permite a definição de campos customizados. Os campos não precisam seguir um padrão estipulado em alguma tabela**
✅ **Pode-se navegar pela lista tanto para frente quanto para trás quantas vezes forem necessárias**
✅ **Permite a procura de registros através de uma chave**
✅ **Acesso aos campos tem a mesma sintaxe do acesso aos campos do cursor**

**Desvantagens:**
❌ **A lista não pode ser preenchida automaticamente por um cursor**
❌ **Não é possível filtrar os dados depois de inseridos na lista**
❌ **Não permitem interação direta com o sistema, ou seja, os valores da lista não podem ser preenchidos através de rotinas desenvolvidas do sistema**

### ⚠️ IMPORTANTE - Observações Críticas de Uso

#### No Gerador de Relatórios

**🚨 OBRIGATÓRIO:**
- Coloque a **definição, adição e efetivação dos campos** no evento **"Funções Globais do Modelo Gerador"**, pois esta é a primeira regra a ser compilada para os modelos
- Se os campos das listas forem utilizados em uma regra que é compilada antes da adição dos campos da lista, o compilador não reconhece os mesmos dando **erro de compilação**
- **Sempre redeclare** a definição das listas nas regras em que elas forem utilizadas

#### Em Web Services de Geração de Relatórios

**🚨 CRÍTICO - Access Violation:**
- Na execução através de web service (exemplo: `com.senior.g5.co.ger.relatorio` do Gestão Empresarial | ERP)
- Se não houver a **redeclaração da lista** em todas as regras onde são utilizadas, pode ocorrer **erro de Access Violation**
- O Access Violation pode não ocorrer em modo "2 - Sincrono", mas **sempre ocorre** em modo "1 - Local"
- **Solução:** Sempre redeclare as variáveis independentemente do modo de execução

#### No Gerador de Importação e Exportação

**📋 Regra Obrigatória:**
- Coloque a **definição, adição e efetivação dos campos** no evento **"Início da Execução"**
- **Redeclare** a definição da lista nas demais regras onde ela for utilizada

**Exemplo de Declaração Correta:**

```lsp
@ ==> NO EVENTO "Funções Globais" (Gerador) ou "Início da Execução" (Import/Export) @
Definir Lista LstDados;
LstDados.DefinirCampos();
LstDados.AdicionarCampo("Codigo", numero);
LstDados.AdicionarCampo("Nome", alfa, 50);
LstDados.EfetivarCampos();

@ ==> EM CADA REGRA QUE USA A LISTA @
Definir Lista LstDados;  @ OBRIGATÓRIO: Redeclarar @

@ Agora pode usar a lista normalmente @
LstDados.Adicionar();
LstDados.Codigo = 123;
LstDados.Nome = "Exemplo";
LstDados.Gravar();
```

## Funções de Lista de Regras

As funções de Lista de Regras (ListaRegra*) são utilizadas para manipular listas especiais que podem carregar dados diretamente de estruturas JSON ou outras fontes de dados estruturados. Essas funções oferecem uma forma simplificada de processar dados complexos.

### Criação e Carregamento de Listas

#### ListaRegraCriarLista

Cria uma nova lista de regras para armazenar dados estruturados.

**Sintaxe:**

```lsp
ListaRegraCriarLista(<numeroLista>);
```

**Parâmetros:**
- `numeroLista`: Variável numérica que receberá o identificador da lista criada

**Exemplo:**

```lsp
Definir Numero nLista;

ListaRegraCriarLista(nLista);
@ nLista agora contém o identificador da lista criada @
```

#### ListaRegraCarregarJson

Carrega dados de uma estrutura JSON diretamente em uma lista de regras.

**Sintaxe:**

```lsp
ListaRegraCarregarJson(<numeroLista>, <jsonString>, <grupo>, <campos>);
```

**Parâmetros:**
- `numeroLista`: Identificador da lista criada com ListaRegraCriarLista
- `jsonString`: String contendo o JSON a ser processado
- `grupo`: Nome do grupo/objeto dentro do JSON (use "" para raiz)
- `campos`: Lista de campos separados por ponto-e-vírgula (;)

**Exemplo:**

```lsp
Definir Numero nLista;
Definir Alfa vaJSON;
Definir Alfa vaJSONModificado;

@ JSON de exemplo (array de objetos) @
vaJSON = "[{\"nome\":\"João\",\"idade\":\"30\"},{\"nome\":\"Maria\",\"idade\":\"25\"}]";

@ Encapsular array em objeto para compatibilidade @
vaJSONModificado = "{\"pessoas\":" + vaJSON + "}";

@ Criar e carregar lista @
ListaRegraCriarLista(nLista);
ListaRegraCarregarJson(nLista, vaJSONModificado, "pessoas", "nome;idade");
```

**⚠️ Limitação Importante:** A função `ListaRegraCarregarJson` espera um objeto JSON que comece com `{`. Se você tiver um array JSON que comece com `[`, precisa encapsulá-lo em um objeto:

```lsp
@ Array original @
vaArrayJSON = "[{\"campo1\":\"valor1\"},{\"campo2\":\"valor2\"}]";

@ Encapsular em objeto @
vaJSONObjeto = "{\"dados\":" + vaArrayJSON + "}";

@ Agora pode usar ListaRegraCarregarJson @
ListaRegraCarregarJson(nLista, vaJSONObjeto, "dados", "campo1;campo2");
```

### Navegação em Listas de Regras

#### ListaRegraPrimeiro

Posiciona a lista no primeiro registro.

**Sintaxe:**

```lsp
ListaRegraPrimeiro(<numeroLista>, <achou>);
```

**Parâmetros:**
- `numeroLista`: Identificador da lista
- `achou`: Variável alfa que receberá "S" se encontrou registro, "N" se não encontrou

**Exemplo:**

```lsp
Definir Numero nLista;
Definir Alfa vaAchou;

ListaRegraPrimeiro(nLista, vaAchou);
Se (vaAchou = "S") {
  @ Lista posicionada no primeiro registro @
  Mensagem(Retorna, "Primeiro registro encontrado");
} Senao {
  @ Lista vazia @
  Mensagem(Retorna, "Lista vazia");
}
```

#### ListaRegraProximo

Move para o próximo registro da lista.

**Sintaxe:**

```lsp
ListaRegraProximo(<numeroLista>, <achou>);
```

**Parâmetros:**
- `numeroLista`: Identificador da lista
- `achou`: Variável alfa que receberá "S" se encontrou registro, "N" se chegou ao fim

**Exemplo:**

```lsp
Definir Numero nLista;
Definir Alfa vaAchou;

ListaRegraProximo(nLista, vaAchou);
Se (vaAchou = "S") {
  @ Moveu para próximo registro @
  Mensagem(Retorna, "Próximo registro encontrado");
} Senao {
  @ Chegou ao fim da lista @
  Mensagem(Retorna, "Fim da lista");
}
```

### Obtenção de Dados

#### ListaRegraObterValorAlfa

Obtém o valor de um campo específico do registro atual da lista.

**Sintaxe:**

```lsp
ListaRegraObterValorAlfa(<numeroLista>, <nomeCampo>, <valor>, <obteve>);
```

**Parâmetros:**
- `numeroLista`: Identificador da lista
- `nomeCampo`: Nome do campo a ser obtido
- `valor`: Variável alfa que receberá o valor do campo
- `obteve`: Variável alfa que receberá "S" se obteve valor, "N" se não obteve

**Exemplo:**

```lsp
Definir Numero nLista;
Definir Alfa vaNome;
Definir Alfa vaIdade;
Definir Alfa vaObteve;

@ Obter nome do registro atual @
ListaRegraObterValorAlfa(nLista, "nome", vaNome, vaObteve);
Se (vaObteve = "S") {
  Mensagem(Retorna, "Nome: " + vaNome);
}

@ Obter idade do registro atual @
ListaRegraObterValorAlfa(nLista, "idade", vaIdade, vaObteve);
Se (vaObteve = "S") {
  Mensagem(Retorna, "Idade: " + vaIdade);
}
```

### Exemplo Prático Completo: Processamento de JSON

```lsp
Definir Funcao processarUsuariosJSON();

@ Variáveis globais @
Definir Alfa vaJSONResposta;
Definir Numero nListaUsuarios;

@ JSON de exemplo vindo de API @
vaJSONResposta = "[{\"id\":\"1\",\"nome\":\"João Silva\",\"email\":\"joao@exemplo.com\"},{\"id\":\"2\",\"nome\":\"Maria Santos\",\"email\":\"maria@exemplo.com\"}]";

processarUsuariosJSON();

Funcao processarUsuariosJSON(); {
  Definir Alfa vaJSONModificado;
  Definir Alfa vaAchou;
  Definir Alfa vaObteve;
  Definir Alfa vaId;
  Definir Alfa vaNome;
  Definir Alfa vaEmail;
  Definir Numero vnContador;
  
  @ Encapsular array em objeto @
  vaJSONModificado = "{\"usuarios\":" + vaJSONResposta + "}";
  
  @ Criar e carregar lista @
  ListaRegraCriarLista(nListaUsuarios);
  ListaRegraCarregarJson(nListaUsuarios, vaJSONModificado, "usuarios", "id;nome;email");
  
  @ Verificar se carregou dados @
  ListaRegraPrimeiro(nListaUsuarios, vaAchou);
  
  Se (vaAchou = "S") {
    vnContador = 0;
    
    @ Processar todos os registros @
    Enquanto (vaAchou = "S") {
      vnContador++;
      
      @ Obter dados do registro atual @
      ListaRegraObterValorAlfa(nListaUsuarios, "id", vaId, vaObteve);
      ListaRegraObterValorAlfa(nListaUsuarios, "nome", vaNome, vaObteve);
      ListaRegraObterValorAlfa(nListaUsuarios, "email", vaEmail, vaObteve);
      
      @ Processar dados @
      Definir Alfa vaMensagem;
      Definir Alfa vaContadorStr;
      IntParaAlfa(vnContador, vaContadorStr);
      vaMensagem = "Usuário " + vaContadorStr + ": " + vaNome + " (" + vaEmail + ")";
      Mensagem(Retorna, vaMensagem);
      
      @ Mover para próximo @
      ListaRegraProximo(nListaUsuarios, vaAchou);
    }
    
    IntParaAlfa(vnContador, vaContadorStr);
    vaMensagem = "Total de usuários processados: " + vaContadorStr;
    Mensagem(Retorna, vaMensagem);
  } Senao {
    Mensagem(Erro, "Falha ao carregar dados JSON na lista");
  }
}
```

### Casos de Uso Comuns

1. **Processamento de Respostas de API**: Carregar e processar dados JSON retornados por APIs REST
2. **Integração de Sistemas**: Processar arquivos de dados estruturados
3. **Transformação de Dados**: Converter estruturas complexas em dados tabulares
4. **Validação em Lote**: Processar múltiplos registros para validação

### Vantagens das Listas de Regras

- **Simplicidade**: Carregamento direto de JSON sem parsing manual
- **Performance**: Processamento otimizado para estruturas de dados
- **Flexibilidade**: Suporte a estruturas JSON complexas
- **Manutenibilidade**: Código mais limpo comparado ao parsing manual

**⚠️ Observações Importantes:**
- Sempre encapsule arrays JSON em objetos antes de usar `ListaRegraCarregarJson`
- Verifique sempre o retorno das funções de navegação (`vaAchou`)
- Use nomes de campos consistentes entre o JSON e a lista de campos
- A lista deve ser criada antes de tentar carregar dados

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
curExemplo.SQL "SELECT * FROM Tabela";
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
Definir Data vdData; MontaData(1,1,2000, vdData);

vSql = "SELECT * FROM Tabela WHERE Condicao";

SQL_Criar(xCursor);
SQL_UsarSQLSenior2(xCursor, 0);
SQL_UsarAbrangencia(xCursor, 0);
SQL_DefinirComando(xCursor, vSql);
SQL_DefinirInteiro(xCursor, "vnNumero", 1);
SQL_DefinirBoleano(xCursor, "vbBoleano", 1);
SQL_DefinirFlutuante(xCursor, "vnFlutuante", 1.6);
SQL_DefinirData(xCursor, "vdData", vdData);
SQL_DefinirAlfa(xCursor, "vaAlfa", "João da Silva");

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
✅ **Simplicidade na definição e uso.**
✅ **Menor quantidade de funções necessárias.**
✅ **Ideal para consultas simples e rápidas.**

**Desvantagens:**
❌ **Menos flexível para consultas complexas.**
❌ **Não suporta múltiplos parâmetros ou tipos de dados avançados.**
❌ **Não permite o uso de determinadas funções SQL.**

#### Cursor Completo

**Vantagens:**
✅ **Permite acesso a dados atualizados.**
✅ **Permite filtragem dos dados diretamente no banco de dados.**
✅ **Suporta operações complexas com múltiplos parâmetros.**
✅ **Pode utilizar ou não a sintaxe SQL Senior 2.**

**Desvantagens:**
❌ **A performance de resposta depende da rede e do banco de dados.**
❌ **Requer mais funções e configurações em comparação ao cursor simples.**

### Funções de Retorno SQL

As funções de retorno SQL são utilizadas para extrair dados dos registros retornados pelo cursor. Cada função é específica para um tipo de dado e permite recuperar valores dos campos da consulta SQL.

#### Exemplo Completo com Todos os Tipos de Retorno

```lsp
Definir Funcao exemploCompletoRetornoSQL();

@ Variáveis globais @
Definir Alfa xCursor;
Definir Alfa vaNomeFuncionario;      @ Para SQL_RetornarAlfa @
Definir Numero vnCodigoFilial;       @ Para SQL_RetornarInteiro @
Definir Data vdDataNascimento;       @ Para SQL_RetornarData @
Definir Numero vnSalario;            @ Para SQL_RetornarFlutuante @
Definir Numero vnDeficienteFisico;   @ Para SQL_RetornarBoleano @
Definir Alfa vaFotoFuncionario;      @ Para SQL_RetornarBlob @
Definir Numero vnContadorRegistros;

exemploCompletoRetornoSQL();

Funcao exemploCompletoRetornoSQL(); {
  vnContadorRegistros = 0;
  
  SQL_Criar(xCursor);
  SQL_DefinirComando(xCursor, "SELECT NOMFUN, CODFIL, DATNAS, VALSALARIO, DEFFIS FROM R034FUN WHERE NUMEMP = 1");
  
  SQL_AbrirCursor(xCursor);
  Enquanto (SQL_EOF(xCursor) = 0) {
    
    @ ===== TODOS OS TIPOS DE RETORNO EM UM ÚNICO EXEMPLO ===== @
    
    @ 1. SQL_RetornarAlfa - Para campos de texto @
    SQL_RetornarAlfa(xCursor, "NOMFUN", vaNomeFuncionario);
    
    @ 2. SQL_RetornarInteiro - Para campos numéricos inteiros @
    SQL_RetornarInteiro(xCursor, "CODFIL", vnCodigoFilial);
    
    @ 3. SQL_RetornarData - Para campos de data @
    SQL_RetornarData(xCursor, "DATNAS", vdDataNascimento);
    
    @ 4. SQL_RetornarFlutuante - Para campos numéricos com decimais @
    SQL_RetornarFlutuante(xCursor, "VALSALARIO", vnSalario);
    
    @ 5. SQL_RetornarBoleano - Para campos boolean (1/0) @
    SQL_RetornarBoleano(xCursor, "DEFFIS", vnDeficienteFisico);
    
    @ 6. SQL_RetornarSeNulo - Para verificar campos NULL @
    Se (SQL_RetornarSeNulo(xCursor, "NOMFUN") = 0) {
      @ Campo não é nulo, processa normalmente @
      vnContadorRegistros++;
      
      @ Exemplo de processamento dos dados obtidos @
      Se (vnDeficienteFisico = 1) {
        Definir Alfa vaMensagem;
        vaMensagem = vaNomeFuncionario + " - PCD";
        Mensagem(Retorna, vaMensagem);
      } Senao {
        Definir Alfa vaCodigoFilialStr;
        Definir Alfa vaMensagem;
        IntParaAlfa(vnCodigoFilial, vaCodigoFilialStr);
        vaMensagem = vaNomeFuncionario + " - Filial: " + vaCodigoFilialStr;
        Mensagem(Retorna, vaMensagem);
      }
    }
    
    SQL_Proximo(xCursor);
  }
  
  SQL_FecharCursor(xCursor);
  SQL_Destruir(xCursor);
  
  IntParaAlfa(vnContadorRegistros, vaNomeFuncionario);
  Mensagem(Retorna, "Total processado: " + vaNomeFuncionario + " funcionários");
}

@ ===== EXEMPLO ADICIONAL PARA SQL_RetornarBlob ===== @
Funcao exemploRetornarBlob(); {
  Definir Alfa xCursorBlob;
  
  SQL_Criar(xCursorBlob);
  SQL_DefinirComando(xCursorBlob, "SELECT FOTEMP FROM R034FOT WHERE NUMEMP = 1");
  
  SQL_AbrirCursor(xCursorBlob);
  Enquanto (SQL_EOF(xCursorBlob) = 0) {
    @ 7. SQL_RetornarBlob - Para campos binários/arquivos @
    SQL_RetornarBlob(xCursorBlob, "FOTEMP", vaFotoFuncionario);
    
    @ Processar arquivo blob @
    Se (TamanhoAlfa(vaFotoFuncionario) > 0) {
      Mensagem(Retorna, "Foto encontrada");
    }
    
    SQL_Proximo(xCursorBlob);
  }
  
  SQL_FecharCursor(xCursorBlob);
  SQL_Destruir(xCursorBlob);
}
```

#### Referência Rápida das Funções

| **Função** | **Tipo de Campo** | **Sintaxe** | **Uso** |
|------------|-------------------|-------------|---------|
| `SQL_RetornarAlfa` | Texto/String | `SQL_RetornarAlfa(cursor, "CAMPO", variavel)` | Nomes, descrições, códigos texto |
| `SQL_RetornarInteiro` | Número Inteiro | `SQL_RetornarInteiro(cursor, "CAMPO", variavel)` | IDs, códigos, quantidades |
| `SQL_RetornarFlutuante` | Número Decimal | `SQL_RetornarFlutuante(cursor, "CAMPO", variavel)` | Valores monetários, percentuais |
| `SQL_RetornarData` | Data | `SQL_RetornarData(cursor, "CAMPO", variavel)` | Datas de nascimento, cadastro |
| `SQL_RetornarBoleano` | Boolean | `SQL_RetornarBoleano(cursor, "CAMPO", variavel)` | Flags verdadeiro/falso (1/0) |
| `SQL_RetornarBlob` | Binário/Arquivo | `SQL_RetornarBlob(cursor, "CAMPO", variavel)` | Imagens, documentos, anexos |
| `SQL_RetornarSeNulo` | Verificação NULL | `resultado = SQL_RetornarSeNulo(cursor, "CAMPO")` | Valida se campo é nulo |

#### Funções de Controle de Posicionamento do Cursor

Além das funções de retorno, existem funções importantes para controlar e verificar a posição do cursor durante a navegação pelos registros.

##### SQL_BOF

Verifica se o cursor está na posição inicial (antes do primeiro registro: posição BOF - Beginning of File).

**Sintaxe:** `SQL_BOF(Alfa Objeto);`

**Retorno:**
- `1`: Cursor está na posição BOF (antes do primeiro registro)
- `0`: Cursor NÃO está na posição BOF

**Importante:** Na posição BOF, todos os registros estarão nulos.

**Exemplo Prático - Proteção de Contador:**

```lsp
Definir Alfa xCursor;
Definir Numero xFormula;

xFormula = 0;
SQL_Criar(xCursor);
SQL_DefinirComando(xCursor, "SELECT R034FUN.CODFIL FROM R034FUN WHERE R034FUN.CODFIL = 1 AND R034FUN.NUMEMP = 1");

@ Teste para proteger o contador @
@ Se não está em BOF (posição inicial), processa normalmente @
Se (SQL_BOF(xCursor) = 0) {
  SQL_Proximo(xCursor);
  xFormula++;
}

SQL_FecharCursor(xCursor);
SQL_Destruir(xCursor);
```

##### SQL_EOF

Verifica se o cursor está na posição final (depois do último registro: posição EOF - End of File).

**Sintaxe:** `SQL_EOF(Alfa Objeto);`

**Retorno:**
- `1`: Cursor está na posição EOF (depois do último registro)
- `0`: Cursor NÃO está na posição EOF

**Importante:** Na posição EOF, todos os registros estarão nulos.

**Exemplo Prático - Loop de Contagem:**

```lsp
Definir Alfa xCursor;
Definir Numero xFormula;

xFormula = 0;
SQL_Criar(xCursor);
SQL_DefinirComando(xCursor, "SELECT R034FUN.CODFIL FROM R034FUN WHERE R034FUN.CODFIL = 1 AND R034FUN.NUMEMP = 1");
SQL_AbrirCursor(xCursor);

@ Loop enquanto não chegou no fim dos registros @
Enquanto (SQL_EOF(xCursor) = 0) {
  SQL_Proximo(xCursor);
  xFormula++;
}

SQL_FecharCursor(xCursor);
SQL_Destruir(xCursor);
```

#### Observações Importantes

**SQL_RetornarInteiro vs SQL_RetornarFlutuante:**
- `SQL_RetornarInteiro`: Se o campo tem valor `5.45`, retorna apenas `5`
- `SQL_RetornarFlutuante`: Retorna o valor completo `5.45`
- Para campos tipo Double, use **obrigatoriamente** `SQL_RetornarFlutuante`

**SQL_RetornarBoleano:**
- Retorna `1` para verdadeiro e `0` para falso
- Útil para campos de status, flags, indicadores

**SQL_RetornarSeNulo:**
- Retorna `1` se campo é NULL, `0` se não é NULL  
- Não detecta campos vazios (`""`) ou zero (`0`), apenas NULL
- Use para validação antes de processar dados

**SQL_BOF vs SQL_EOF:**
- **SQL_BOF**: Verifica início do cursor (Before Of File)
- **SQL_EOF**: Verifica fim do cursor (End Of File)
- Ambas retornam `1` quando na posição correspondente, `0` caso contrário
- Em ambas as posições (BOF/EOF), todos os registros estarão nulos
- Use para proteger contadores e controlar loops de navegação



### Otimizações para Cursores com Múltiplos Tipos

**❓ Pergunta Comum:** "Não há como otimizar o uso de todos os tipos de retorno em um mesmo cursor?"

** Resposta:** A sequência de `SQL_Retornar*` **é obrigatória** para cada campo, mas podemos otimizar a lógica de processamento:

#### **🚀 Versão Otimizada - Verificação Prévia de NULLs**

```lsp
Definir Funcao consultarFuncionariosOtimizado();

@ Variáveis globais @
Definir Alfa xCursor;
Definir Alfa vaNomeFuncionario;
Definir Numero vnCodigoFilial;
Definir Data vdDataNascimento;
Definir Numero vnSalario;
Definir Numero vnDeficienteFisico;
Definir Numero vnContadorValidos;
Definir Numero vnContadorTotal;

consultarFuncionariosOtimizado();

Funcao consultarFuncionariosOtimizado(); {
  vnContadorValidos = 0;
  vnContadorTotal = 0;
  
  SQL_Criar(xCursor);
  SQL_DefinirComando(xCursor, "SELECT NOMFUN, CODFIL, DATNAS, VALSALARIO, DEFFIS FROM R034FUN WHERE NUMEMP = 1");
  
  SQL_AbrirCursor(xCursor);
  Enquanto (SQL_EOF(xCursor) = 0) {
    vnContadorTotal++;
    
    @ 1. PRIMEIRA OTIMIZAÇÃO: Verificar NULLs ANTES de recuperar dados @
    Se ((SQL_RetornarSeNulo(xCursor, "NOMFUN") = 0) e (SQL_RetornarSeNulo(xCursor, "VALSALARIO") = 0)) {
      
      @ 2. SEGUNDA OTIMIZAÇÃO: Só recupera dados se necessário @
      SQL_RetornarAlfa(xCursor, "NOMFUN", vaNomeFuncionario);
      SQL_RetornarFlutuante(xCursor, "VALSALARIO", vnSalario);
      
      @ 3. TERCEIRA OTIMIZAÇÃO: Recupera dados opcionais só se precisar @
      Se (vnSalario > 5000) { @ Só pega outros dados para salários altos @
        SQL_RetornarInteiro(xCursor, "CODFIL", vnCodigoFilial);
        SQL_RetornarData(xCursor, "DATNAS", vdDataNascimento);
        SQL_RetornarBoleano(xCursor, "DEFFIS", vnDeficienteFisico);
        
        @ Processamento completo @
        vnContadorValidos++;
      }
    }
    
    SQL_Proximo(xCursor);
  }
  
  SQL_FecharCursor(xCursor);
  SQL_Destruir(xCursor);
  
  Definir Alfa vaContadorValidosStr;
  Definir Alfa vaContadorTotalStr;
  Definir Alfa vaMensagem;
  IntParaAlfa(vnContadorValidos, vaContadorValidosStr);
  IntParaAlfa(vnContadorTotal, vaContadorTotalStr);
  vaMensagem = "Registros processados: " + vaContadorValidosStr + " de " + vaContadorTotalStr;
  Mensagem(Retorna, vaMensagem);
}
```

#### **⚡ Técnicas de Otimização Aplicadas**

**1. Verificação Prévia de NULLs**
```lsp
@ Evita recuperar dados desnecessários @
Se ((SQL_RetornarSeNulo(xCursor, "NOMFUN") = 0) e (SQL_RetornarSeNulo(xCursor, "VALSALARIO") = 0)) {
  @ Só recupera dados se campos essenciais existem @
}
```

**2. Recuperação Condicional**
```lsp
@ Recupera dados básicos primeiro @
SQL_RetornarAlfa(xCursor, "NOMFUN", vaNomeFuncionario);
SQL_RetornarFlutuante(xCursor, "VALSALARIO", vnSalario);

@ Só recupera dados extras se condição atendida @
Se (vnSalario > 5000) {
  SQL_RetornarInteiro(xCursor, "CODFIL", vnCodigoFilial);
  @ ... outros dados @
}
```

**3. Agrupamento por Uso**
```lsp
@ Agrupa recuperação por necessidade @
@ Campos obrigatórios: sempre recupera @
SQL_RetornarAlfa(xCursor, "NOMFUN", vaNomeFuncionario);
SQL_RetornarFlutuante(xCursor, "VALSALARIO", vnSalario);

@ Campos opcionais: recupera condicionalmente @
Se (precisaDetalhes = 1) {
  SQL_RetornarData(xCursor, "DATNAS", vdDataNascimento);
  SQL_RetornarBoleano(xCursor, "DEFFIS", vnDeficienteFisico);
}
```

#### **🎯 Resumo das Limitações e Soluções**

| **Aspecto** | **Limitação** | **Solução** |
|-------------|---------------|-------------|
| **Tipos de Dados** | Cada tipo precisa de função específica |  **Obrigatório** - Use SQL_Retornar correto |
| **Performance** | Recuperar dados desnecessários |  **Otimizável** - Verificar NULLs primeiro |
| **Lógica** | Processamento sequencial |  **Otimizável** - Recuperação condicional |
| **Memória** | Muitas variáveis |  **Otimizável** - Reutilizar variáveis |

**📌 Conclusão:** A sequência de `SQL_Retornar*` **não pode ser simplificada** (é obrigatória), mas a **lógica de quando e como recuperar** pode ser muito otimizada!

## Definição de Funções

É um conjunto de comandos que tem como objetivo calcular um ou mais valores e retorná-los para uso na regra. Havendo uma operação que se repita, pode-se criar a função e chamá-la em cada regra, sem precisar reimplementá-la.

Nota:
Como boa prática, é recomendável que se reserve a regra 001 apenas para implementar funções.

Uma função pode receber parâmetros e retornar valores.

**⚠️ Importante:**
- Valores alterados dentro da função também serão alterados fora dela.
- **Os parâmetros definidos para as funções devem obrigatoriamente ser Numéricos**
- **Parâmetros do tipo Alfanuméricos (Alfa) NÃO são suportados por funções definidas nas regras**

**Incorreto - NÃO funciona:**
```lsp
Funcao alterarNome(Alfa vaNome); {
   vaNome = "Nome Alterado"; @ ERRO: Parâmetro Alfa não suportado @
}
```

** Correto - Usar variáveis globais:**
```lsp
Definir Alfa vaNome;

vaNome = "João Silva";

Funcao alterarNome(); {
  vaNome = "João da Silva"; @ Correto: variável global @
}
```

**Exemplo Oficial da Senior:**
```lsp
@ Definição/declaração da função criada pelo usuário @
Definir Funcao Somar(Numero pNum1, Numero pNum2, Numero End pResultado);

Definir Numero vNum1;
Definir Numero vNum2;
Definir Numero vResultado;
Definir Alfa vResultadoMensagem;

vNum1 = 50;
vNum2 = 100;
Somar(vNum1, vNum2, vResultado);

IntParaAlfa(vResultado, vResultadoMensagem);
vResultadoMensagem = "O resultado da soma é " + vResultadoMensagem;
Mensagem(Retorna, vResultadoMensagem);

@ Função criada pelo usuário para realizar a soma de dois números @
Funcao Somar(Numero pNum1, Numero pNum2, Numero End pResultado); {
  pResultado = pNum1 + pNum2;
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

**Incorreto - NÃO funciona:**
```lsp
Funcao minhaFuncao(); {
  @ Corpo da função @
}

minhaFuncao(); @ ERRO: Chamada após declaração @
```

** Correto - Ordem obrigatória:**
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
| StrParaInt                  | Converte um valor alfanumérico (string) para o tipo Inteiro. Equivalente a AlfaParaInt.|
| ArqExiste                   | Verifica se um arquivo físico existe no local especificado.               |
| AtualizaBarraProgresso      | Atualiza as mensagens apresentadas na tela da barra de progresso.         |
| CaracterParaAlfa            | Converte um caracter (que fica armazenado pelo código ASCII) para o valor Alfanumérico correspondente. |
| CodData                     | Possibilita a composição de uma data, montando-a através de dia, mês e ano.|
| DesMontaData                | Desmonta uma data, separando em três variáveis, as informações Dia/Mês/Ano da data. |
| ConverteDataBanco           | Converte uma data qualquer, para o formato de data do banco de dados. |
| ConverteDataSqlSenior2      | Converte datas para o formato SQL Senior 2. |
| ConverteDataToDB            | Converte uma data qualquer, para o formato de data do banco de dados. |
| AnoBissexto                 | Retorna a informação se um ano é ou não bissexto tomando como base o ano da data passada. |
| ConverteCodificacaoString   | Esta função converte a codificação de um texto para o formato definido pelo usuário. |
| ConverteMascara             | Esta função converte um valor de entrada (numérico, data, hora ou cadeia de caracteres), para o tipo de dado cadeia de caracteres. |
| ConverteParaMaiusculo       | Converte o conteúdo de uma variável do tipo Alfa para maiúsculo.          |
| ConverteParaMinusculo       | Converte o conteúdo de uma variável do tipo Alfa para minúsculo.          |
| ConverteTexto               | Substitui os caracteres especiais informados no texto de acordo com a codificação do padrão informada, retorna em uma nova variável o texto convertido. |
| CopiarAlfa                  | Esta função copia parte do conteúdo de uma variável/campo alfanumérico para a variável alfanumérica Retorno. |
| CriarArquivoTemporario      | Cria um arquivo temporário de nome aleatório e único prefixado com o valor do parâmetro prefixo. |
| DataHoje                    | Retorna a data atual do sistema operacional.                              |
| DataHora                    | Retorna data e hora atual como número fracionário.                        |
| DecodData                   | Permite a separação de uma data em dia, mês e ano para que os dados possam ser usados separadamente. |
| DeletarAlfa                 | Esta função apaga uma determinada quantidade de caracteres de uma variável/campo a partir da posição informada. |
| DeletarStr                  | Elimina parte de um texto a partir de uma posição específica. |
| InserirAlfa                 | Insere um ou mais caracteres em uma variável/campo, a partir da posição indicada. |
| InserirStr                  | Insere um ou mais caracteres em uma variável/campo, a partir da posição indicada. |
| LimpaEspacos                | Limpa os espaços em branco à direita e à esquerda de uma variável alfanumérica. |
| LimpaEspacosDireita         | Limpa os espaços em branco à direita de uma variável alfanumérica. |
| LimpaEspacosEsquerda        | Limpa os espaços em branco à esquerda de uma variável alfanumérica. |
| QuebraTexto                 | Quebra texto em linhas conforme o tamanho especificado. |
| ProcuraEnter                | Procura caracteres de quebra de linha (#13 ou #10) em uma string. |
| CalculaAlfa                 | Realiza operações matemáticas com valores alfanuméricos. |
| CarregarTextoArq            | Carrega o conteúdo de um arquivo texto para uma variável alfanumérica. |
| Concatena                   | Concatena até 3 campo/variáveis tipo alfa, formando uma só variável. |
| Desencriptar                | Função para descriptografar uma cadeia de caracteres.                     |
| Dividir                     | Função disponível para dividir um valor por outro.                        |
| Encriptar                   | Criptografa a cadeia de caracteres.                                       |
| ExcluirArquivoTemporario    | Exclui um arquivo criado pela função CriarArquivoTemporario.              |
| ExecProg                    | Permite a execução de aplicativos durante a execução de regras.           |
| Extenso                     | Gera o extenso de um valor. |
| ExtensoMes                  | Monta o extenso do mês de uma determinada data. |
| ExtensoMoeda                | Gera o extenso de um valor com a moeda informada. |
| ExtensoSemana               | Monta o extenso do dia da semana de uma determinada data. |
| DataExtenso                 | Gera o extenso de determinada data. |
| FormatarData                | Formata a data.                                                           |
| GeraHash                    | Retorna um Hash do texto informado.                                       |
| GerarNonce                  | Gera o valor do campo Nonce, um número aleatório.                         |
| GerarPwdDigest              | Gera o Digest da senha, a partir do Nonce, Data e senha, em formato base64.|
| GeraSenha                   | Retorna uma sequência de caracteres alfanuméricos aleatoriamente.         |
| GeraToken                   | Retorna um token criptografado.                                           |
| MultiplicaValor             | Multiplica um número no formato alfanumérico por um fator de multiplicação numérico. |
| ConverteUnidadeMedida       | Calcula a quantidade convertida de uma unidade de medida (de) para outra unidade de medida (para). |
| Arredonda                   | Arredonda um valor, conforme a precisão informada. |
| ArredondaABNT               | Aplica a regra de arredondamento da ABNT, conforme a precisão informada. |
| ArredondarValor             | Arredonda determinado valor, conforme a precisão informada. |
| Arredonda Valor Tipo Acerto | Arredonda um valor tipo acerto, conforme a precisão informada. |
| Formatar                    | Formata números de acordo com os parâmetros definidos (formato Delphi). |
| FormatarN                   | Formata números com casas decimais de acordo com os parâmetros definidos (formato Delphi). |
| HoraParaMinuto              | Converte em minutos os valores que representam hora e minuto.             |
| IniciaBarraProgresso        | Inicia a barra de progresso utilizada para mostrar ao usuário o andamento de um processo mais extenso. |
| OcultaBarraProgressoRelatorio | Oculta a barra de progresso padrão durante a execução de relatórios.    |
| FinalizaBarraProgresso      | Finaliza a tela de barra de progresso.                                    |
| IntParaAlfa                 | Converte um número para formato alfanumérico, desprezando as casas decimais.|
| IntParaStr                  | Converte um valor inteiro para o tipo String (Alfanumérico). Equivalente a IntParaAlfa.|
| LerPosicaoAlfa              | Identifica qual caracter está em determinada posição do campo/variável de origem. |
| LinhasArquivo               | Leitura da quantidade de linhas existentes em um determinado arquivo.     |
| ListaItem                   | Retorna o valor de um item de uma lista de valores concatenados por um caracter separador. |
| ListaQuantidade             | Retorna a quantidade de itens de uma lista de valores concatenados por um caracter separador em um texto. |
| Mensagem                    | Apresenta a mensagem em tela de acordo com a parametrização do tipo de retorno e da mensagem que será visualizada. |
| MontaAbrangencia            | Função utilizada para retornar uma cláusula SQL de acordo com um campo e uma abrangência de valores. |
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
| **Manipulação Dinâmica de Variáveis** |
| PegarTipoVar                | Retorna o tipo de uma variável qualquer, passada como string. |
| PegarValorVarAlf            | Retorna o valor de uma variável alfanumérica identificada por nome. |
| PegarValorVarNum            | Retorna o valor de uma variável numérica ou de data identificada por nome. |
| SetarValorVarAlf            | Define o valor de uma variável alfanumérica identificada por nome. |
| SetarValorVarNum            | Define o valor de uma variável numérica ou de data identificada por nome. |
| **Verificação e Limpeza** |
| EstaNulo                    | Verifica se uma variável está nula (vazia ou não inicializada). |
| DeixaNumeros                | Remove todos os caracteres não numéricos de uma string. |
| **Funções de Lista de Regras** |
| ListaRegraCriarLista        | Cria uma nova lista de regras para armazenar dados estruturados. |
| ListaRegraCarregarJson      | Carrega dados de uma estrutura JSON diretamente em uma lista de regras. |
| ListaRegraPrimeiro          | Posiciona a lista no primeiro registro. |
| ListaRegraProximo           | Move para o próximo registro da lista. |
| ListaRegraObterValorAlfa    | Obtém o valor de um campo específico do registro atual da lista. |
| **Arrays** |
| LimpaGerTabAlf              | Limpa o conteúdo do Registro GerTabAlf. |
| LimpaGerTabNum              | Limpa o conteúdo do Registro GerTabNum. |

Para mais detalhes sobre cada função, consulte a @documentação da Senior.

## Funções SQL

As funções a seguir podem ser utilizadas para manipulação de comandos SQL e o resultado dos comandos (cursores) em regras. A partir destas funções podem ser executados comandos DML (INSERT, UPDATE, DELETE) e também comandos SELECT que retornam cursores que poderão ser manipulados também.

| Nome                | Descrição                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------|
| SQL_AbrirCursor     | Função que abre o cursor (depois de informado o comando SQL a ser utilizado, que é definido na função SQL_DefinirComando). |
| SQL_Criar           | A partir de uma variável criada como alfa, é criado um cursor para trabalhar com informações da base de dados. |
| SQL_DefinirAlfa     | Função que define um valor do tipo alfa para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_DefinirBlob     | Função que define um valor do tipo alfa (que representa o arquivo blob) para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_DefinirBoleano  | Função que define um valor do tipo boolean (Número 1 para verdadeiro e 0 para falso) para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_DefinirComando  | Função que aplica o comando SQL para o cursor passado como parâmetro. |
| SQL_DefinirData     | Função que define um valor do tipo data ou date para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_DefinirFlutuante| Função que define um valor do tipo flutuante ou float (Fracionado Ex: 1,5) para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_DefinirInteiro  | Função que define um valor do tipo inteiro para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_Destruir        | Função que elimina um cursor e deve ser chamada quando o cursor não for mais utilizado. |
| SQL_BOF             | Função que retorna a informação se o cursor está na posição inicial (antes do primeiro registro: posição BOF). |
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

- **Certificados digitais**: As funções HTTP LSP **NÃO oferecem suporte** ao uso de certificados digitais
- ** Parâmetros suportados**: Apenas parâmetros que compõem as requisições (headers, content-type, autenticação básica, etc.)

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

✅ **Sempre configure timeouts** para evitar travamentos em requisições lentas
✅ **Use HttpDesabilitaErroResposta** para controle manual de erros HTTP
✅ **Configure cabeçalhos adequados** para cada tipo de API (Accept, Content-Type, etc.)
✅ **Valide códigos de status HTTP** antes de processar respostas
✅ **Use HTTPS** sempre que possível para garantir segurança
✅ **Trate erros de rede** adequadamente com mensagens claras
✅ **Para arquivos grandes**, use `HttpDownload` em vez de `HttpGet`
✅ **Mantenha credenciais seguras** e nunca faça hardcode em produção
✅ **Use Base64Encode/Base64Decode** para autenticação básica e decodificação de tokens
✅ **Configure User-Agent** para identificar sua aplicação
✅ **Configure proxy adequadamente** em ambientes corporativos
✅ **Use exceções de proxy** para acessos internos sem proxy
✅ **Habilite SNI** para sites que requerem certificados modernos
✅ **Configure codificação UTF-8** para suporte internacional
✅ **Use cookies** para manter sessões em aplicações web

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

### Manipulação de JSON

#### ValorElementoJson

Função para extrair valores de elementos específicos de um objeto JSON.

**Sintaxe:**

```lsp
ValorElementoJson(<json>, <grupo>, <elemento>, <valor>);
```

**Parâmetros:**
- `json`: String contendo o JSON de origem
- `grupo`: Nome do grupo/objeto dentro do JSON (use "" para raiz)
- `elemento`: Nome do elemento/propriedade a ser extraído
- `valor`: Variável que receberá o valor extraído

**Exemplos:**

```lsp
Definir Alfa vaJSON;
Definir Alfa vaToken;
Definir Alfa vaNome;
Definir Alfa vaEmail;

@ JSON simples @
vaJSON = "{\"token\": \"abc123\", \"usuario\": \"joao\"}";

@ Extrair o elemento "token" do JSON @
ValorElementoJson(vaJSON, "", "token", vaToken);
@ vaToken será "abc123" @

@ JSON com objeto aninhado @
vaJSON = "{\"data\": {\"first_name\": \"João\", \"email\": \"joao@exemplo.com\"}, \"token\": \"xyz789\"}";

@ Extrair elementos do grupo "data" @
ValorElementoJson(vaJSON, "data", "first_name", vaNome);
ValorElementoJson(vaJSON, "data", "email", vaEmail);

@ Extrair elemento da raiz @
ValorElementoJson(vaJSON, "", "token", vaToken);

Mensagem(Retorna, "Nome: " + vaNome + ", Email: " + vaEmail + ", Token: " + vaToken);
```

**Exemplo Prático com API:**

```lsp
Funcao processarRespostaAPI(); {
  Definir Alfa vaHTTP;
  Definir Alfa vaJSON;
  Definir Alfa vaStatus;
  Definir Alfa vaMensagem;
  Definir Alfa vaUsuario;
  
  HttpObjeto(vaHTTP);
  HttpGet(vaHTTP, "https://reqres.in/api/users/2", vaJSON);
  
  @ JSON retornado: {"data":{"id":2,"email":"janet.weaver@reqres.in","first_name":"Janet","last_name":"Weaver"},"support":{"url":"https://reqres.in/#support-heading","text":"To keep ReqRes free..."}} @
  
  @ Extrair dados do usuário @
  ValorElementoJson(vaJSON, "data", "first_name", vaUsuario);
  ValorElementoJson(vaJSON, "data", "email", vaStatus);
  
  vaMensagem = "Usuário: " + vaUsuario + " - Email: " + vaStatus;
  Mensagem(Retorna, vaMensagem);
}
```

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
    vaMensagem = " Usuário encontrado: " + vaNome + " (" + vaEmail + ")";
    Mensagem(Retorna, vaMensagem);
  } Senao Se (vnCodRes = 404) {
    Mensagem(Retorna, "Usuário não encontrado");
  } Senao {
    IntParaAlfa(vnCodRes, vaId);
    Mensagem(Erro, "Erro na requisição: " + vaId);
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
    vaMensagem = " Usuário criado! ID: " + vaId;
    Mensagem(Retorna, vaMensagem);
  } Senao {
    IntParaAlfa(vnCodRes, vaId);
    Mensagem(Erro, "Erro ao criar: " + vaId);
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
    Mensagem(Retorna, " Usuário " + vaIdStr + " atualizado completamente");
  } Senao {
    IntParaAlfa(vnCodRes, vaIdStr);
    Mensagem(Erro, "Erro ao atualizar: " + vaIdStr);
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
    Mensagem(Retorna, " Cargo atualizado para: " + vaNovoCargo);
  } Senao {
    IntParaAlfa(vnCodRes, vaIdStr);
    Mensagem(Erro, "Erro ao atualizar cargo: " + vaIdStr);
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
    Mensagem(Retorna, " Usuário " + vaIdStr + " excluído com sucesso");
  } Senao {
    IntParaAlfa(vnCodRes, vaIdStr);
    Mensagem(Erro, "Erro ao excluir: " + vaIdStr);
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
    Mensagem(Retorna, " Autenticação Basic Auth: " + vaUsuarioRetornado);
  } Senao Se (vnCodRes = 401) {
    Mensagem(Retorna, "Credenciais inválidas - 401 Unauthorized");
  } Senao {
    IntParaAlfa(vnCodRes, vaAuth);
    Mensagem(Erro, "Erro inesperado: " + vaAuth);
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
    Mensagem(Retorna, " Autenticação Bearer: " + vaTokenRetornado);
  } Senao Se (vnCodRes = 401) {
    Mensagem(Retorna, "Token inválido - 401 Unauthorized");
  } Senao {
    IntParaAlfa(vnCodRes, vaAuth);
    Mensagem(Erro, "Erro inesperado: " + vaAuth);
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
    Mensagem(Retorna, " Login realizado! Token: " + vaToken);

    @ 2. USA TOKEN - Em requisição subsequente @
    vaAuth = "Bearer " + vaToken;
    HttpAlteraCabecalhoRequisicao(vaHTTP, "Authorization", vaAuth);

    @ 3. OPERAÇÃO AUTENTICADA - Buscar usuários @
    HttpGet(vaHTTP, "https://reqres.in/api/users?page=1", vaJSON);
    HttpLeCodigoResposta(vaHTTP, vnCodRes);

    Se (vnCodRes = 200) {
      Mensagem(Retorna, " Dados obtidos com token de autenticação!");
    } Senao {
      Mensagem(Erro, "Erro ao usar token autenticado");
    }
  } Senao {
    Mensagem(Erro, "Falha no login");
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

###  **Resumo das APIs Utilizadas**

| API | Funcionalidade | Autenticação | Status |
|-----|---------------|--------------|--------|
| **ReqRes** | CRUD completo funcional | Não requer |  Real |
| **HTTPBin Basic** | Teste Basic Auth |  user:pass |  Real |
| **HTTPBin Bearer** | Teste Bearer Token |  Bearer token |  Real |

**💡 Vantagens desta abordagem:**
- 🎯 **Foco didático**: Um exemplo claro de cada conceito
-  **Funcionalidade real**: Todas as operações funcionam de verdade
- 🔐 **Autenticação completa**: Basic Auth e Bearer Token reais
- 📚 **Progressão lógica**: Do básico ao avançado

---

## 📝 **Cheat Sheet LSP (Cola Rápida)**

### **🚀 Essenciais para Todo Projeto**

```lsp
@ === ESTRUTURA BÁSICA === @
Definir Alfa vaMensagem;
Definir Numero vnContador;
Definir Data vdDataAtual;

@ === MENSAGENS === @
vaMensagem = "Processamento concluído!";
Mensagem(Retorna, vaMensagem);
Mensagem(Erro, "Erro crítico!");

@ === LOOPS COMUNS === @
Para (vnContador = 1; vnContador <= 10; vnContador++) {
  @ código repetido @
}

Enquanto (vnContador > 0) {
  vnContador--;
}

@ === CONDICIONAIS === @
Se (vnContador > 0) {
  @ código @
} Senao Se (vnContador = 0) {
  @ código alternativo @
} Senao {
  @ código padrão @
}
```

### **🔧 Manipulação de Dados Comuns**

```lsp
@ === STRINGS === @
TamanhoAlfa(vaTexto, vnTamanho);
PosicaoAlfa("busca", vaTexto, vnPosicao);
SubstAlfa("antigo", "novo", vaTexto);
SubstAlfaUmaVez("antigo", "novo", vaTexto);  @ Apenas primeira ocorrência @
ConverteParaMaiusculo(vaTexto);
CopiarAlfa(vaTexto, 1, 5);                   @ Extrai 5 chars da posição 1 @
DeletarAlfa(vaTexto, 1, 3);                  @ Remove 3 chars da posição 1 @
InserirAlfa("texto", vaTexto, 5);            @ Insere na posição 5 @
LimpaEspacos(vaTexto);                       @ Remove espaços laterais @
DeixaNumeros(vaTexto);                       @ Remove não-números @

@ === CONVERSÕES === @
IntParaAlfa(vnNumero, vaTexto);
IntParaStr(vnNumero, vaTexto);      @ Equivalente a IntParaAlfa @
AlfaParaInt(vaTexto, vnNumero);
StrParaInt(vaTexto, vnNumero);      @ Equivalente a AlfaParaInt @
AlfaParaDecimal(vaTexto, vnDecimal);

@ === DATAS === @
DataHoje(vdDataAtual);
DataHora(vnDataHoraAtual);         
@ Para formatação, converta para número @
Definir Numero vnData;
vnData = vdData;
FormatarData(vnData, "dd/MM/yyyy", vaDataFormatada);
MontaData(1, 1, 2024, vdData);      @ Monta data a partir de componentes @
DesMontaData(vdData, vnDia, vnMes, vnAno); @ Desmonta data em componentes @
AnoBissexto(vdData, vnBissexto);    @ Verifica se ano é bissexto @

@ === VALIDAÇÕES === @
EstaNulo(vaVariavel, vnEhNulo);
ArqExiste(vaCaminho, vnExiste);
VrfAbrA(vaCodigo, "A..Z", vnValido);

@ === MATEMÁTICA === @
Arredonda(vnValor, 2);              @ Arredonda para 2 casas decimais @
ArredondaABNT(vnValor, 2);          @ Arredonda seguindo regra ABNT @
MultiplicaValor(vaNumero, vnFator, vaResultado); @ Multiplica string numérica @

@ === EXTENSO === @
Extenso(vnValor, 30, 30, 30, vaLin1, vaLin2, vaLin3); @ Gera extenso do valor @
ExtensoMes(vdData, vaMesExt);       @ Gera extenso do mês @
ExtensoSemana(vdData, vaSemExt);    @ Gera extenso do dia da semana @
```

### **🌐 HTTP e APIs**

```lsp
@ === HTTP BÁSICO === @
HttpObjeto(vaHTTP);
HttpDesabilitaErroResposta(vaHTTP);
HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json");
HttpGet(vaHTTP, vaURL, vaResposta);
HttpLeCodigoResposta(vaHTTP, vnStatus);

@ === JSON === @
ValorElementoJson(vaJSON, "", "campo", vaValor);
ValorElementoJson(vaJSON, "grupo", "campo", vaValor);

@ === AUTENTICAÇÃO === @
vaCredenciais = vaUsuario + ":" + vaSenha;
Base64Encode(vaCredenciais, vaBase64);
vaAuth = "Basic " + vaBase64;
```

### **🗃️ Banco de Dados**

```lsp
@ === CURSOR SIMPLES === @
Definir Cursor curDados;
curDados.SQL "SELECT * FROM TABELA WHERE ID = 1";
curDados.AbrirCursor();
Enquanto (curDados.Achou) {
  @ processar curDados.CAMPO @
  curDados.Proximo();
}
curDados.FecharCursor();

@ === CURSOR COMPLETO === @
SQL_Criar(xCursor);
SQL_DefinirComando(xCursor, "SELECT * FROM TABELA");
SQL_AbrirCursor(xCursor);
Enquanto (SQL_EOF(xCursor) = 0) {
  SQL_RetornarAlfa(xCursor, "CAMPO", vaValor);
  SQL_Proximo(xCursor);
}
SQL_FecharCursor(xCursor);
SQL_Destruir(xCursor);
```

### **⚠️ Armadilhas Comuns**

```lsp
@ NUNCA FAÇA @
Mensagem(Retorna, "Valor: " + IntParaAlfa(vnNumero));  @ Erro! @
vnTamanho = TamanhoAlfa(vaTexto);                      @ Erro! @
AlfaParaDecimal(vaTexto, Grid.Campo);                  @ Erro! @

@  SEMPRE FAÇA @
IntParaAlfa(vnNumero, vaNumeroStr);
vaMensagem = "Valor: " + vaNumeroStr;
Mensagem(Retorna, vaMensagem);

TamanhoAlfa(vaTexto, vnTamanho);

AlfaParaDecimal(vaTexto, vnValor);
Grid.Campo = vnValor;
```

---

## 🚨 **LEMBRETE FINAL: Regra de Ouro da LSP**

### **🎯 Manipule primeiro, chame a função depois!**

**Esta é a regra mais importante da LSP. Memorize e aplique sempre:**

1. **Faça todas as operações** (concatenação, conversões, cálculos)
2. **Armazene em variáveis** 
3. **Passe as variáveis** para as funções

**Errado:**
```lsp
Mensagem(Retorna, "Total: " + IntParaAlfa(vnSoma + vnExtra));
```

** Correto:**
```lsp
vnTotal = vnSoma + vnExtra;
IntParaAlfa(vnTotal, vaTotalStr);
vaMensagem = "Total: " + vaTotalStr;
Mensagem(Retorna, vaMensagem);
```

---

**📚 Fim da Documentação LSP - Linguagem Sênior de Programação**

*Desenvolvido em colaboração | Atualizado em 2025*
