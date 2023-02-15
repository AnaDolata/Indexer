# Indexador de Palavras em C
## Ana Carolina Dolata e Guilherme de Morais Janke

O trabalho consiste na criação de um programa capaz de indexar palavras de um ou mais documentos de texto. Tal programa deverá ser nomeado como indexer.

## Arquivos para testes

* http://200.236.3.126:8999/ds143-texts/

## Funcionamento

```
NOME
    indexer - indexa palavras de documentos de texto

SINOPSE
    indexer --freq N ARQUIVO
    indexer --freq-word PALAVRA ARQUIVO
    indexer --search TERMO ARQUIVO [ARQUIVO ...]

DESCRIÇÃO
    O programa **indexer** realiza uma contagem de palavras em documentos de 
    texto. A partir dessa contagem, ele ainda permite uma busca pelo número de 
    ocorrências de uma palavra específica em um documento, ou a seleção de 
    documentos relevantes para um dado termo de busca.
    O programa **indexer** transforma todas as letras para minúsculas e ignora
    caracteres como números e pontuações.
    Quando executado com a opção --freq, o programa **indexer** irá exibir o 
    número de ocorrências das N palavras mais frequentes no documento passado 
    como parâmetro, em ordem decrescente de ocorrências.
    Quando executado com a opção --freq-word, o programa **indexer** exibe a 
    contagem de uma palavra específica no documento passado como parâmetro.
    Por fim, quando executado com a opção --search, o programa **indexer** 
    apresenta uma listagem dos documentos mais relevantes para um dado termo de 
    busca. Para tanto, o programa utiliza o cálculo TF-IDF (Term 
    Frequency-Inverse Document Frequency).

OPÇÕES
  --freq N ARQUIVO
    Exibe o número de ocorrência das N palavras que mais aparecem em ARQUIVO, em
    ordem decrescente de ocorrência.
  --freq-word PALAVRA ARQUIVO
    Exibe o número de ocorrências de PALAVRA em ARQUIVO. 
  --search TERMO ARQUIVO [ARQUIVO ...]
    Exibe uma listagem dos ARQUIVOS mais relevantes encontrados pela busca por 
    TERMO. A listagem é apresentada em ordem descrescente de relevância. 
    TERMO pode conter mais de uma palavra. Neste caso, deve ser indicado entre 
    àspas.
    
EXEMPLO
  ./indexer --freq 2 ARQUIVO
```

## Requisitos

O trabalho deve ser realizado em grupos de até 3 alunos.

O programa deve conter a implementação de uma estrutura de dados eficiente capaz
de atender às funcionalidades descritas acima, mesmo quando executado com
arquivos grandes (> 1GB). Tal estrutura deve ser implementada pelos próprios
alunos e deverá ser explicada no dia da defesa do trabalho.

O programa deve ser capaz de ser compilado, se for o caso, e executado em um ambiente Linux.
Isso não deve gerar maiores problemas para aqueles que programam em Windows ou
outro S.O.. Basta ter cuidado para não utilizar bibliotecas ou outras diretrizes
específicas desses S.O.'s.

Além disso, o repositório deverá conter um arquivo README.md com a
explicação do processo de execução do programa.
Como informado acima, o funcionamento da aplicação indexer tem as seguintes
peculiaridades:

- Transformar todas os caracteres em minúsculo, ou seja, comportamento de ignore-case;
- Ignorar palavras com menos de 2 caracteres;
- Ignorar caracteres que não sejam letras, como números e pontuações:
    - Por conta disso, palavras compostas como bem-vindo serão separadas em duas, bem e vindo.


