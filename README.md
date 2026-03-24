# Solução Web para Gestão Financeira e Clínica da SPASB

## Descrição do projeto
Este repositório contém o desenvolvimento de uma aplicação web gerencial para a SPASB (Sociedade Protetora dos Animais de Santa Bárbara), com foco na organização de dados financeiros e clínicos da instituição.

O sistema tem como objetivo substituir controles manuais e planilhas dispersas por uma solução centralizada, com banco de dados relacional, priorizando alta usabilidade para os voluntários.

## Problema
A ausência de um sistema interno intuitivo para o registro de dados financeiros e clínicos gera perda de informações essenciais, prejudicando a gestão de recursos da organização.

## Objetivo
Desenvolver uma aplicação web com banco de dados relacional, focada na usabilidade, para centralizar e simplificar o controle de receitas, despesas e procedimentos veterinários da instituição.

## Escopo inicial

### Módulo financeiro
- registro de entradas financeiras;
- registro de despesas;
- taxa de adoção;
- compra de microchip;
- produtos de higiene e limpeza;
- ração;
- medicamentos;
- verba mensal de parceria com a prefeitura;
- divisão do valor de entrada:
  - 50% para a SPASB;
  - 50% para a veterinária parceira.

### Módulo clínico
- consultas;
- castrações;
- exames;
- procedimentos;
- acompanhamento de medicamentos e tratamentos.

## Público-alvo
Voluntários e responsáveis pela gestão da SPASB.

## Requisitos não funcionais iniciais
- interface intuitiva;
- alta usabilidade;
- atualização semanal dos dados;
- possibilidade de acesso em dispositivos móveis;
- estratégia de backup;
- geração de relatórios;
- visualização gráfica do desempenho financeiro e clínico.

## Arquitetura inicial do projeto
A solução será organizada em três camadas principais:

### 1. Front-end
Responsável pelas interfaces do sistema, priorizando simplicidade, clareza visual e facilidade de navegação para os voluntários.

### 2. Back-end
Responsável pela lógica do sistema, validação dos dados, processamento das informações e comunicação com o banco de dados.

### 3. Banco de dados relacional
Responsável pelo armazenamento estruturado das informações financeiras e clínicas, garantindo organização, integridade e rastreabilidade histórica.

## Organização do repositório
- `docs/`: documentação do projeto, requisitos, atas e wireframes;
- `backend/`: estrutura inicial da aplicação web e lógica do sistema;
- `database/`: scripts e definições do banco de dados;
- `frontend/`: protótipos, wireframes e materiais de interface.

## Tecnologias previstas
As tecnologias serão definidas oficialmente pela equipe, considerando:
- linguagem de programação para o back-end;
- framework web;
- SGBD relacional;
- tecnologias de interface para o front-end.

## Status do projeto
Projeto acadêmico em desenvolvimento no âmbito do Projeto Integrador da Univesp.

## Equipe
- Camila de Moraes Cristofoletti Calvo
- Daniela Bin
- Fernando Rodrigo da Silva
- Mirko Lerotic Filho
- Rafael Leandro Breviglieri
