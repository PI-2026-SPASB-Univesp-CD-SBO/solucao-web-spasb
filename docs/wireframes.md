
# Wireframes Iniciais do Sistema

## Objetivo
Definir a estrutura inicial das telas do sistema web, priorizando alta usabilidade para os voluntários da SPASB.

---

## 1. Tela de Login

### Objetivo
Permitir acesso simples ao sistema.

### Elementos principais
- campo de e-mail ou usuário;
- campo de senha;
- botão "Entrar";
- link "Esqueci minha senha" (opcional).

### Estrutura sugerida
```text
----------------------------------------
|              Logo SPASB              |
|                                      |
| Usuário / E-mail: [______________]   |
| Senha:             [______________]  |
|                                      |
|           [   Entrar   ]             |
----------------------------------------

## 2. Tela Dashboard

### Objetivo
Apresentar uma visão geral rápida dos principais indicadores.

### Elementos principais
- total de consultas no mês;
- total de castrações no mês;
- total de entradas;
- total de despesas;
- saldo atual;
- gráfico de movimentação;
- lista de lançamentos recentes.

### Estrutura sugerida
```text
------------------------------------------------------
| Logo SPASB                     Usuário | Sair       |
------------------------------------------------------
| Menu: Dashboard | Financeiro | Clínico | Relatórios |
------------------------------------------------------
| Consultas no mês | Castrações | Saldo atual        |
------------------------------------------------------
| Entradas         | Despesas   | Verba prefeitura   |
------------------------------------------------------
|                Gráfico do período                   |
------------------------------------------------------
| Últimos lançamentos                                 |
| data | categoria | valor | tipo                     |
------------------------------------------------------

## 3. Tela de Lançamento Financeiro

### Objetivo
Registrar receitas e despesas de forma simples.

### Elementos principais
- data;
- tipo: entrada ou saída;
- categoria;
- descrição;
- valor;
- observação;
- botão salvar.

### Categorias iniciais
- valor de entrada;
- valor de exames;
- taxa de adoção;
- compra de microchip;
- higiene e limpeza;
- ração;
- medicamentos;
- verba da prefeitura.

### Estrutura sugerida
```text
------------------------------------------------------
| Financeiro > Novo lançamento                        |
------------------------------------------------------
| Data:        [____/____/______]                     |
| Tipo:        ( ) Entrada   ( ) Saída               |
| Categoria:   [ selecionar ]                         |
| Descrição:   [_______________________________]      |
| Valor:       [_______________________________]      |
| Observação:  [_______________________________]      |
|                                                      |
| [ Salvar ]                     [ Cancelar ]          |
------------------------------------------------------

## 4. Tela de Registro Clínico

### Objetivo
Registrar procedimentos clínicos realizados.

### Elementos principais
- data;
- tipo de atendimento;
- detalhe;
- valor relacionado;
- observação;
- botão salvar.

### Tipos de atendimento
- consulta;
- castração;
- exame;
- procedimento.

### Estrutura sugerida
```text
------------------------------------------------------
| Clínico > Novo registro                             |
------------------------------------------------------
| Data:               [____/____/______]              |
| Tipo de registro:   [ selecionar ]                  |
| Detalhe:            [ selecionar ]                  |
| Valor:              [____________________]          |
| Observação:         [____________________]          |
|                                                     |
| [ Salvar ]                 [ Cancelar ]             |
------------------------------------------------------

## 5. Tela de Relatórios

### Objetivo
Permitir a consulta e análise dos dados.

### Elementos principais
- filtro por período;
- filtro por categoria;
- resumo financeiro;
- gráfico;
- listagem dos resultados.

### Estrutura sugerida
```text
------------------------------------------------------
| Relatórios                                          |
------------------------------------------------------
| Período: [____] até [____]                          |
| Categoria: [ selecionar ]                           |
| Tipo clínico: [ selecionar ]                        |
|                                                     |
| [ Gerar relatório ]                                 |
------------------------------------------------------
| Total arrecadado: R$ ______                         |
| Total gasto:      R$ ______                         |
| Saldo:            R$ ______                         |
------------------------------------------------------
|                 Gráfico do período                  |
------------------------------------------------------
|                 Tabela de resultados                |
------------------------------------------------------

