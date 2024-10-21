---
layout: default
title: Banco de questões
nav_order: 2
---

# Banco de questões
{: .no_toc }

Projeto: Sistema de Quiz para Questões de Vestibular
{: .fs-6 .fw-300 }

Link para o [respositório no GitHub](https://github.com/leticiacamilodosreis/banco-de-questoes)

## Funcionalidades:

1. Tem conexão com um banco de dados PostgreSQL contendo as perguntas;
2. Apresenta perguntas ao usuário e permite a entrada de respostas;
3. Verifica se a resposta fornecida está correta;
4. Repete a pergunta até que o usuário acerte;
5. Exibe uma mensagem de conclusão ao final de todas as perguntas.


## Estrutura:

O projeto é composto por três arquivos principais:

1. main.py: O ponto de entrada do programa.
2. database.py: Define a classe responsável pela conexão e operações com o banco de dados.
3. questao.py: Define a classe que representa uma questão e sua lógica de verificação de resposta.

## Como executar o projeto


### Requisitos:

1. Python 3.x
2. PostgreSQL
3. Biblioteca psycopg2 para Python (instale com "pip install psycopg2" no terminal)

### Configuração do banco de dados:

Será necessário criar um banco de dados PostgreSQL chamado banco_questoes.
Dentro desse banco, crie uma tabela chamada questoes com as colunas id, pergunta, e resposta_correta.
Insira suas perguntas e respostas no banco de dados.

Exemplo de criação da tabela e inserção de dados:


```yaml
CREATE TABLE questoes (
    id SERIAL PRIMARY KEY,
    pergunta TEXT NOT NULL,
    resposta_correta TEXT NOT NULL
);

INSERT INTO questoes (pergunta, resposta_correta) VALUES
('Qual é a capital do Brasil?', 'Brasília'),
('Quanto é 5 + 7?', '12'),
('Qual é o maior planeta do Sistema Solar?', 'Júpiter');

```


### Como rodar:

1. Certifique-se de que o banco de dados PostgreSQL está rodando.
2. Execute o script main.py
3. O sistema então buscará as questões no banco de dados e iniciará o quiz no terminal.

