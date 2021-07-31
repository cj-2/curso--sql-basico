# SQL - Structured Query Language

## SGBD

Sistema de gerenciamento de banco de dados.

## DML - Data Manipulation Language

Linguagem de Manipulação de Dados

### Principais Comandos

- SELECT - Seleciona
- INSERT - Insere
  - INTO - Dentro de...
  - VALUES - Valores
- DELETE - Delta
- UPDATE - Atualiza
  - SET - "Seta" qual coluna

### Outros Comuns

- FROM - De qual coluna
- WHERE - Onde... x = y (condicional)
- LIKE - Que se pareça com... Útil: '%'
- LIMIT - Coloca um limite de resultados.
- ORDER BY - Orndena por... Modificadores: ASC, DESC
- OFFSET - Pula um número de resultados setados.
- DISTINCT(coluna) - Retorna os registros distintos, que não se repetem na coluna.
- CAST(coluna AS char) - Converte o tipo dos valores, no caso para char.
- AS - Pode ser usado para modificar uma coluna, ex: primeiro_nome AS nome

### Tipos de JOIN

Entender os JOINs é o caminho para os sucesso.

- JOIN - Combinar as linhas de tabelas diferentes, sem nenhuma condição. (Pouco comum)
- (INNER) JOIN - Usado quando existe uma condição de igualdade ligando duas ou mais tabelas.
- LEFT (OUTER) JOIN - Todos os dados da tabela esquerda junto com a da direita com os vazios preenchidos (da direita) com null.
- RIGHT (OUTER) JOIN - Parecido com a LEFT, porem com todos os dados da direita.
- ON - Expessifica qual a condição de igualdade.

### Exemplos Interessantes

Exemplo de uso de alias AS e INNER JOIN

    SELECT P.primeiro_nome, P.sigla_estado, E.nome_capital FROM pessoas AS P INNER JOIN estados AS E ON P.sigla_estado = E.sigla_estado

Exemplo de INSERT múltiplos:

    INSERT INTO pessoas (primeiro_nome, ultimo_nome, sigla_estado, camiseta_ou_chapeu, nome_time) 
    VALUES 
        ('DanimoneteiroDBA', 'Apelido', 'SP', 'camiseta', 'vermelho'),
        ('Teresa', 'Costa', 'MG', 'chapéu', 'azul')

Exemplo de UPDATE "seguro", contendo o WHERE.

    UPDATE pessoas SET primeiro_nome = 'Pedro'
    WHERE primeiro_nome = 'Vitor'

Exemplo DELETE

    DELETE FROM pessoas
    WHERE primeiro_nome = 'Pedro'

### Grupos

- GROUP BY ...

### Funções

- length(coluna) - Retorna a quantidade de caracteres do registro.
- count(*) - Conta quantos resultados retornaram.
- avg(coluna) - Retorna a média do grupo.
- min(coluna) - Retorna o menor valor de um grupo.
- max(coluna) - Maior valor.
- sun(coluna) - Soma.
- lower(coluna) - Deixa em minúsculo.
- upper(coluna) - Deixa em maiúscula.
- substr(coluna, charInicial, qtdChar)
- replace(coluna, 'substituido', 'praIsso')

## DDL - Linguagem de Definição de Dados

Usada para gerenciar a estrutura do banco de dados.

- CREATE
- ALTER
- DROP

## DCL Linguagem de Controle de Dados

- GRANT
- REVOKE

## DTL - Linguagem de Transação de Dados

- COMMIT
- ROLLBACK

## Erros Comuns & Dicas

- Sintaxe (leia os erros).
- Atenção com as aspas ''.
- Atenção aos nomes.
- Utilize interface gráfica para auxiliar.
- Teste comandos.
- Atenção aos NULLs.
- WHERE é muito importante.
- Salve e versione os scripts.
- Sempre utilize a documentação.
