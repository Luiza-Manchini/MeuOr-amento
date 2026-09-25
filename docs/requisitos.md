# Requisitos do Sistema — Meu Orçamento

## 1. Objetivo

Este documento apresenta os requisitos funcionais e não funcionais do aplicativo **Meu Orçamento**.

Os requisitos foram definidos com base no escopo inicial do MVP e servirão como referência para a criação dos épicos, User Stories, Tasks, regras de negócio e testes do sistema.

---

# 2. Requisitos Funcionais

Os requisitos funcionais representam as ações e funcionalidades que o sistema deverá oferecer ao usuário.

## Gestão de Usuário

### RF01 — Identificar o usuário

O sistema deve identificar o usuário autenticado por meio da conta Microsoft utilizada no Power Apps.

### RF02 — Exibir informações do usuário

O sistema deve permitir a exibição de informações básicas do usuário, como nome e e-mail.

---

# Gestão de Receitas

### RF03 — Cadastrar receita

O sistema deve permitir que o usuário cadastre uma nova receita.

A receita deverá possuir, no mínimo:

- descrição;
- valor;
- data;
- categoria ou tipo da receita.

### RF04 — Cadastrar salário

O sistema deve permitir que o usuário registre seu salário como uma receita.

### RF05 — Cadastrar receitas adicionais

O sistema deve permitir o cadastro de receitas diferentes do salário, como:

- renda extra;
- freelancer;
- reembolso;
- vendas;
- outros recebimentos.

### RF06 — Consultar receitas

O sistema deve permitir que o usuário visualize as receitas cadastradas.

### RF07 — Editar receita

O sistema deve permitir a alteração de uma receita cadastrada.

### RF08 — Excluir receita

O sistema deve permitir que o usuário exclua uma receita.

### RF09 — Filtrar receitas por período

O sistema deve permitir a visualização das receitas por mês e ano.

---

# Gestão de Despesas

### RF10 — Cadastrar despesa

O sistema deve permitir que o usuário registre uma nova despesa.

A despesa deverá possuir:

- descrição;
- valor;
- categoria;
- tipo;
- data;
- vencimento;
- status.

### RF11 — Classificar despesa por categoria

O sistema deve permitir classificar uma despesa em categorias como:

- Moradia;
- Alimentação;
- Transporte;
- Educação;
- Saúde;
- Lazer;
- Assinaturas;
- Contas;
- Outros.

### RF12 — Classificar despesa por tipo

O sistema deve permitir classificar a despesa como:

- fixa;
- variável.

### RF13 — Informar vencimento

O sistema deve permitir informar a data de vencimento de uma despesa.

### RF14 — Definir status da despesa

O sistema deve permitir classificar uma despesa como:

- Pendente;
- Pago.

### RF15 — Marcar despesa como paga

O sistema deve permitir alterar uma despesa pendente para o status Pago.

### RF16 — Consultar despesas

O sistema deve permitir que o usuário visualize as despesas cadastradas.

### RF17 — Editar despesa

O sistema deve permitir alterar os dados de uma despesa cadastrada.

### RF18 — Excluir despesa

O sistema deve permitir excluir uma despesa cadastrada.

### RF19 — Filtrar despesas por período

O sistema deve permitir filtrar as despesas por mês e ano.

### RF20 — Filtrar despesas por categoria

O sistema deve permitir consultar despesas utilizando sua categoria.

### RF21 — Filtrar despesas por status

O sistema deve permitir visualizar separadamente despesas:

- pagas;
- pendentes.

---

# Planejamento Financeiro

### RF22 — Criar planejamento mensal

O sistema deve permitir que o usuário defina seu planejamento financeiro para determinado mês.

### RF23 — Definir receita esperada

O sistema deve permitir informar o valor de receita esperado para o mês.

### RF24 — Definir meta de economia

O sistema deve permitir que o usuário informe quanto deseja economizar durante o mês.

### RF25 — Definir limite de gastos por categoria

O sistema deve permitir definir limites de gastos para determinadas categorias.

Exemplo:

Alimentação: R$ 800  
Lazer: R$ 400  
Transporte: R$ 500

### RF26 — Calcular utilização do orçamento

O sistema deve calcular quanto do orçamento mensal já foi utilizado.

### RF27 — Comparar gasto com limite da categoria

O sistema deve comparar o total gasto em uma categoria com o limite definido pelo usuário.

---

# Dashboard Financeiro

### RF28 — Exibir total de receitas

O sistema deve apresentar o valor total recebido no período selecionado.

### RF29 — Exibir total de despesas

O sistema deve apresentar o valor total de despesas no período selecionado.

### RF30 — Calcular saldo disponível

O sistema deve calcular o saldo utilizando:

**Saldo = Total de Receitas − Total de Despesas**

### RF31 — Exibir percentual da renda utilizada

O sistema deve calcular e apresentar o percentual da renda que já foi utilizado.

### RF32 — Exibir gastos por categoria

O sistema deve apresentar quanto foi gasto em cada categoria.

### RF33 — Exibir despesas pendentes

O sistema deve apresentar as contas que ainda não foram pagas.

### RF34 — Exibir progresso da meta de economia

O sistema deve permitir acompanhar o progresso da meta de economia definida pelo usuário.

### RF35 — Selecionar período do dashboard

O sistema deve permitir selecionar o mês e ano que serão utilizados para exibir as informações financeiras.

---

# Navegação e Interface

### RF36 — Navegar entre as telas

O sistema deve permitir a navegação entre:

- Dashboard;
- Receitas;
- Despesas;
- Planejamento;
- Perfil.

### RF37 — Exibir confirmação de cadastro

O sistema deve informar ao usuário quando um registro for salvo com sucesso.

### RF38 — Exibir mensagens de erro

O sistema deve informar quando ocorrer algum erro durante o cadastro ou alteração de informações.

### RF39 — Validar campos obrigatórios

O sistema não deve permitir a gravação de registros quando os campos obrigatórios não forem preenchidos.

### RF40 — Solicitar confirmação de exclusão

O sistema deve solicitar confirmação antes de excluir uma receita ou despesa.

---

# 3. Requisitos Não Funcionais

Os requisitos não funcionais descrevem características relacionadas à qualidade, desempenho, segurança e experiência de uso do sistema.

## RNF01 — Usabilidade

O aplicativo deve possuir uma interface simples e de fácil compreensão.

## RNF02 — Consistência visual

As telas devem utilizar padrões consistentes de:

- cores;
- fontes;
- botões;
- ícones;
- campos;
- espaçamentos.

## RNF03 — Responsividade

O aplicativo deve ser desenvolvido considerando diferentes tamanhos de tela suportados pelo Power Apps.

## RNF04 — Desempenho

As principais telas e consultas do sistema devem carregar as informações sem atrasos excessivos.

## RNF05 — Segurança

O usuário deve visualizar e manipular apenas os dados aos quais possuir acesso.

## RNF06 — Autenticação

O acesso ao aplicativo deverá utilizar a autenticação da conta Microsoft.

## RNF07 — Integridade dos dados

O sistema deve evitar o cadastro de informações inválidas em campos obrigatórios.

## RNF08 — Persistência dos dados

Os registros cadastrados devem permanecer armazenados mesmo após o usuário fechar o aplicativo.

## RNF09 — Manutenibilidade

A aplicação deve ser organizada de forma que novas funcionalidades possam ser adicionadas futuramente sem necessidade de reconstrução completa do sistema.

## RNF10 — Organização do código

As fórmulas Power Fx deverão ser escritas de forma organizada e com nomes de controles, variáveis e componentes que facilitem sua identificação.

## RNF11 — Padronização de nomenclatura

Os componentes deverão seguir uma convenção de nomenclatura.

Exemplos:

`btnSalvarDespesa`

`txtDescricaoDespesa`

`drpCategoria`

`lblSaldo`

`galDespesas`

## RNF12 — Feedback ao usuário

O sistema deve apresentar informações visuais após ações importantes, como:

- cadastro realizado;
- registro alterado;
- registro excluído;
- erro de preenchimento.

---

# 4. Priorização dos Requisitos

Para facilitar o desenvolvimento do MVP, os requisitos serão classificados utilizando três prioridades.

## Alta

Essenciais para o funcionamento do aplicativo.

Exemplos:

- cadastro de receitas;
- cadastro de despesas;
- consulta de registros;
- cálculo de saldo;
- dashboard básico.

## Média

Importantes, mas que podem ser desenvolvidos após as funcionalidades principais.

Exemplos:

- limites por categoria;
- filtros avançados;
- acompanhamento da meta de economia.

## Baixa

Melhorias que não impedem o funcionamento principal do MVP.

Exemplos:

- recursos visuais adicionais;
- personalizações;
- filtros complementares.

---

# 5. Critério de Entrada no MVP

Um requisito poderá fazer parte do MVP quando:

1. estiver relacionado diretamente ao controle financeiro básico;
2. possuir comportamento definido;
3. puder ser desenvolvido utilizando a arquitetura inicial do projeto;
4. não depender de integrações externas complexas;
5. contribuir diretamente para o objetivo principal do aplicativo.

---

