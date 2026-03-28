# Arquitetura e Modelagem de Dados - SPASB

## Racional do Modelo de Dados
O Diagrama Entidade-Relacionamento (DER) foi desenhado a partir de um aprofundamento rigoroso nas regras de negócio da SPASB, buscando não apenas resolver o problema atual de gestão de planilhas, mas também prever a escalabilidade da OSC.

Durante a modelagem lógica, tomamos as seguintes decisões arquiteturais:

### 1. Herança e escalabilidade de entidades
* **Desafio:** Identificamos que a relação da ONG com o público é complexa. Uma mesma pessoa pode ser "Tutora" (responsável por um animal), "Adotante" (paga taxas de adoção) ou "Doadora" (faz/fez doações sem possuir animais). 
* **Solução:** Em vez de criar tabelas separadas e duplicar cadastros (ex: cadastrar a mesma pessoa como tutora e depois como doadora), criamos uma superentidade `Pessoa`. Essa tabela centraliza dados comuns (Nome, CPF, Endereço, Telefone) e se ramifica conforme a interação da pessoa com a OSC, garantindo integridade e evitando redundância no banco.

### 2. Gestão Financeira
* **Desafio:** A OSC relatou dificuldade em gerenciar repasses de veterinárias parceiras e, principalmente, em separar a verba geral da OSC do "Repasse SOS" (Verba da Prefeitura), que não gera lucro e exige prestação de contas rigorosa.
* **Solução:** * O cálculo de 50% de repasse para a clínica parceira foi automatizado no modelo lógico. A tabela `Atendimento` registra os campos `parcela_SPASB` e `parcela_parceiro`, garantindo que o relatório final seja exato.
    * Criamos a entidade central `Conta`, permitindo que o sistema gerencie múltiplos "caixas" (Ex: Conta Geral vs. Conta Prefeitura). Toda `Entrada` e `Despesa` é amarrada ao ID de uma conta específica, automatizando o recálculo do `saldo_atual`.

### 3. Rastreabilidade e Transparência
* **Desafio:** A verba pública exige comprovação de cada centavo gasto.
* **Solução:** A entidade `Despesa` foi fortemente tipada (com categorias específicas) e vinculada obrigatoriamente a uma entidade `Nota_Fiscal`. Além disso, previmos o atributo `numero_parcela` na Despesa para compras a prazo, garantindo que o fluxo de caixa futuro seja rastreável.
