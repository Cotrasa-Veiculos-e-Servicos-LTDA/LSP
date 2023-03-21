
## Funções

###  Abrir (Open)
Abre o arquivo informado em nome do arquivo para o modo de abertura informado (Ler/Gravar). Se o arquivo não existir, ele é criado. Ele retorna um manipulador de arquivos.

**Sintaxe** 

    Abrir ("\<nome do arquivo\>",\<modo de abertura\>);

- **Exemplo**

      arq = Abrir ("Teste.txt",Ler);

###  Alfa (String)

Usado com o comando  **Definir**  para definir uma variável Alfanumérica com o  **tamanho**  determinado.

**Sintaxe**

    Definir Alfa <nome da variável>[<tamanho>];

- **Exemplo**

      Definir Alfa S[30];
 
### Atualizar campos (RefreshFields)

Atualiza os dados de todos os campos de uma tela de cadastramento.

- **Exemplo**

      AtualizarCampos();
