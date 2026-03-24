
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


