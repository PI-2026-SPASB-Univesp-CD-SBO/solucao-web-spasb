
# Requisitos do Sistema

## 1. Requisitos funcionais

### RF01
O sistema deve permitir o registro de entradas financeiras.

### RF02
O sistema deve permitir o registro de despesas.

### RF03
O sistema deve permitir o cadastro de consultas veterinárias.

### RF04
O sistema deve permitir o cadastro de castrações.

### RF05
O sistema deve permitir o cadastro de exames.

### RF06
O sistema deve permitir o cadastro de procedimentos.

### RF07
O sistema deve permitir registrar taxa de adoção.

### RF08
O sistema deve permitir registrar compra de microchip.

### RF09
O sistema deve permitir registrar despesas com produtos de higiene e limpeza.

### RF10
O sistema deve permitir registrar despesas com ração.

### RF11
O sistema deve permitir registrar despesas com medicamentos.

### RF12
O sistema deve permitir registrar a verba mensal oriunda da parceria com a prefeitura.

### RF13
O sistema deve permitir separar automaticamente o valor de entrada em:
- 50% para a SPASB;
- 50% para a veterinária parceira.

### RF14
O sistema deve permitir consulta de registros por período.

### RF15
O sistema deve permitir a emissão de relatórios financeiros.

### RF16
O sistema deve permitir a visualização de gráficos de desempenho.

### RF17
O sistema deve permitir o registro de Notas Fiscais (NFs) vinculadas às despesas.

### RF18
O sistema deve atualizar automaticamente o saldo geral e o saldo da verba da prefeitura a cada nova entrada ou saída registrada.

## 2. Requisitos não funcionais

### RNF01
O sistema deve possuir interface intuitiva e simples de usar.

### RNF02
O sistema deve priorizar alta usabilidade para voluntários.

### RNF03
O sistema deve permitir uso em dispositivos móveis.

### RNF04
O sistema deve ter estratégia de backup para reduzir risco de perda de dados.

### RNF05
O sistema deve organizar as informações em banco de dados relacional.

### RNF06
O sistema deve permitir atualização semanal dos dados.

## 3. Regras de negócio iniciais

### RN01
Os dados financeiros devem ser atualizados semanalmente.

### RN02
O valor de entrada deverá ser dividido em 50% para a SPASB e 50% para a veterinária parceira.

### RN03
Os campos de exames e procedimentos deverão possuir opções selecionáveis para facilitar o preenchimento.

### RN04
A solução deverá apoiar a geração de relatórios e gráficos para acompanhamento da clínica.

### RN05
A verba da prefeitura (Repasse SOS) não gera lucro para a SPASB. O sistema deve descontar 50% do valor padrão das consultas terceirizadas quando pagas com essa verba, exigindo a apresentação de Nota Fiscal.

## 4. Observação
Estes requisitos são iniciais e poderão ser refinados após validação com a representante da SPASB e análise do protótipo.
