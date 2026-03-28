Enum opcoes_tipo_animal{
  cachorro
  gato
  passaros
  coelho
  tartaruga
  repteis_geral
  animais_exoticos
  outros
}

Table animal{
  id_animal int [primary key]
  nome varchar
  raca varchar
  cor varchar
  tipo_animal opcoes_tipo_animal
  data_nascimento date
  id_tutor int
  id_adotante int
}

Enum opcoes_tipo_atendimento{
  Castracoes
  Consultas
  Exames
  Vacina
  Outros_procedimentos
  Outros
}

table atendimento{
  id_atendimento int [primary key]
  data_atendimento date
  tipo_atendimento opcoes_tipo_atendimento
  valor_total decimal
  parcela_sbpasb decimal
  parcela_parceiro decimal
  id_animal int
  id_entrada int
  id_parceiro int
}

Table pessoa {
  id_pessoa int [primary key]
  nome varchar
  endereco varchar
  telefone varchar
}

table fisica{
  id_pessoa int [primary key]
  cpf varchar
}

table juridica{
  id_pessoa int [primary key]
  cnpj varchar
  razao_social varchar
}

Table tutor {
  id_tutor int [primary key]
  id_pessoa int
  id_animal int
  // Aqui, no futuro, pode colocar dados que SÓ o tutor tem
}

Table doador {
  id_pessoa int [primary key]
  // Aqui entrariam dados específicos de doação, se houver
}

Table adotante {
  id_pessoa int
  id_adotante int [primary key]
  id_animal int
  // Aqui entrariam dados específicos da adoção
}

table entrada{
  id_entrada int [primary key]
  data_entrada date
  valor decimal
  nome_conta vachar
  id_origem int
  id_conta int
  id_pessoa int
  //nome_conta pode ser dropdown, mas, para isso, precisamos da informação
}

enum opcoes_categoria_origem{
  Doacoes
  Verbas_Publicas
  Atendimentos_Clinicos
  Taxas_Vendas
  Eventos_Campanhas
  Outros
}

enum opcoes_nome_origem{
  Doacao_PIX
  Doacao_Telemarketing
  Doacao_Recorrente
  Doacao_Apadrinhamento
  Doacao_Geral
  Repasse_Prefeitura_SOS
  Emendas_Parlamentares
  Taxa_Adocaoo
  Venda_Aplicacao_Microchip
  Eventos
  Serviços_Clinicos
  //O sistema vai puxar os detalhes lá da tabela de Atendimento)
  Outros
  //é preciso mapear outros campos que podem ser úteis a eles
}

enum opcoes_status{
  Ativo
  Inativo
}

table origem{
  id_origem int [primary key]
  nome_origem opcoes_nome_origem
  categoria_origem opcoes_categoria_origem
  status opcoes_status
}

enum opcoes_categoria_despesas{
  racoes
  medicamentos
  equipe
  transporte
  prestadores
  //aqui, também é ideal mapear mais a fundo.
}

table despesas{
  id_despesa int [primary key]
  valor decimal
  data_vencimento date
  data_pagamento date
  descricao varchar
  numero_parcela int
  id_conta int
  categoria_despesa opcoes_categoria_despesas
  id_nota int
}

table nota_fiscal {
  id_nota int [primary key]
  numero_nota int
  data_emissao date
  exercicio int
  descricao varchar
  valor_nota decimal
  chave_acesso varchar
  id_parceiro int
}

table parceiro{
  id_parceiro int
  especialidade varchar
  valor_tabela_social decimal
  observacoes_relacionamento varchar
  id_pessoa int [primary key]
}

table conta{
  id_conta int [primary key]
  numero_conta int
  nome_conta varchar
  //pode ser um dropdown, mas precisa de dados
  saldo_atual decimal(10,2)
}


// --- ESPECIALIZAÇÕES (1:1) ---
Ref: pessoa.id_pessoa - fisica.id_pessoa
Ref: pessoa.id_pessoa - juridica.id_pessoa
Ref: pessoa.id_pessoa - doador.id_pessoa
Ref: pessoa.id_pessoa - parceiro.id_pessoa
Ref: pessoa.id_pessoa - tutor.id_pessoa
Ref: pessoa.id_pessoa - adotante.id_pessoa

// --- RELACIONAMENTOS DE POSSE (1:N) ---
// Note que aqui a boca (<) abre para o Animal
Ref: tutor.id_pessoa < animal.id_tutor
Ref: adotante.id_pessoa < animal.id_adotante

// --- MOVIMENTAÇÕES E SAÚDE (1:N) ---
Ref: animal.id_animal < atendimento.id_animal
Ref: parceiro.id_pessoa < atendimento.id_parceiro // Usei id_pessoa para manter o padrão
Ref: entrada.id_entrada < atendimento.id_entrada // Muitas entradas podem pagar um atendimento (ou vice-versa)

// --- FINANCEIRO (1:N) ---
Ref: origem.id_origem < entrada.id_origem
Ref: conta.id_conta < entrada.id_conta
Ref: pessoa.id_pessoa < entrada.id_pessoa
Ref: conta.id_conta < despesas.id_conta
Ref: nota_fiscal.id_nota < despesas.id_nota
Ref: parceiro.id_pessoa < nota_fiscal.id_parceiro
Ref: parceiro.id_parceiro < conta.saldo_atual
