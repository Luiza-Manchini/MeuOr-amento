# Meu Orçamento

## 1. Visão Geral

O **Meu Orçamento** é um aplicativo de gestão financeira pessoal desenvolvido utilizando Microsoft Power Apps.

O objetivo principal do aplicativo é permitir que o usuário organize sua vida financeira de maneira simples e visual, registrando suas receitas, despesas e metas de economia.


---

## 2. Problema

O controle financeiro pessoal pode se tornar difícil quando receitas, despesas e contas são acompanhadas por diferentes meios, como anotações, planilhas ou aplicativos separados.

Além disso, nem sempre é fácil visualizar:

- quanto da renda mensal já foi comprometida;
- quais categorias possuem os maiores gastos;
- quais contas ainda precisam ser pagas;
- quanto dinheiro ainda está disponível;
- quanto foi possível economizar durante o mês.

O aplicativo pretende centralizar essas informações em um único ambiente.

---

## 3. Objetivo Geral

Desenvolver um aplicativo de orçamento pessoal que permita registrar, acompanhar e analisar receitas e despesas mensais.

O sistema deverá fornecer ao usuário uma visão clara da sua situação financeira atual e auxiliar no planejamento dos seus gastos.

---

## 4. Objetivos Específicos

O aplicativo deverá permitir ao usuário:

- cadastrar seu salário e outras receitas;
- cadastrar despesas;
- diferenciar despesas fixas e variáveis;
- organizar despesas por categorias;
- informar o vencimento das contas;
- identificar contas pagas e pendentes;
- visualizar o total de receitas;
- visualizar o total de despesas;
- calcular o saldo disponível;
- acompanhar quanto da renda já foi utilizado;
- estabelecer metas de economia;
- acompanhar limites de gastos;
- visualizar informações financeiras por meio de um dashboard.

---

## 5. Público-Alvo

O aplicativo será inicialmente desenvolvido para uso pessoal.

Entretanto, sua estrutura poderá permitir futuramente que diferentes usuários utilizem o sistema para organizar suas próprias finanças.

O público-alvo são pessoas que desejam acompanhar seus gastos e organizar seu orçamento mensal utilizando uma interface simples.

---

## 6. Proposta de Valor

O Meu Orçamento pretende oferecer uma forma simples de responder perguntas importantes sobre a vida financeira do usuário, como:

**Quanto eu recebi este mês?**

**Quanto eu já gastei?**

**Quanto ainda tenho disponível?**

**Onde estou gastando mais dinheiro?**

**Quais contas ainda não foram pagas?**

**Estou conseguindo atingir minha meta de economia?**

---

## 7. Escopo do MVP

A primeira versão funcional do aplicativo será considerada o **MVP — Minimum Viable Product**.

O MVP deverá possuir as seguintes funcionalidades:

### Gestão de Receitas

Cadastro de salário e outras receitas recebidas durante o mês.

### Gestão de Despesas

Cadastro de despesas com informações como:

- descrição;
- valor;
- categoria;
- data;
- vencimento;
- tipo da despesa;
- situação de pagamento.

### Categorias

As despesas poderão ser classificadas em categorias, como:

- Moradia;
- Alimentação;
- Transporte;
- Educação;
- Saúde;
- Lazer;
- Assinaturas;
- Contas;
- Outros.

### Status das despesas

As despesas poderão possuir inicialmente os status:

- Pendente;
- Pago.

### Planejamento mensal

O usuário poderá definir:

- receita esperada;
- meta de economia;
- limites de gastos por categoria.

### Dashboard

O aplicativo deverá apresentar um resumo contendo:

- total de receitas;
- total de despesas;
- saldo disponível;
- percentual da renda utilizada;
- despesas por categoria;
- contas pendentes.

---

## 8. Fora do Escopo do MVP

As seguintes funcionalidades não serão desenvolvidas inicialmente:

- integração automática com bancos;
- Open Finance;
- leitura automática de extratos;
- importação automática de transações bancárias;
- inteligência artificial;
- leitura de comprovantes;
- controle de investimentos;
- controle detalhado de cartão de crédito;
- divisão de despesas entre usuários;
- notificações automáticas;
- previsão financeira utilizando IA.

Essas funcionalidades poderão ser avaliadas para versões futuras.

---

## 9. Tecnologias Planejadas

O projeto utilizará inicialmente:

**Microsoft Power Apps**  
Responsável pelo desenvolvimento da interface e das funcionalidades do aplicativo.

**Power Fx**  
Utilizado para criação das regras, fórmulas e comportamentos dentro do Power Apps.

**Microsoft SharePoint Lists**  
Utilizado inicialmente como fonte de dados da aplicação.

**GitHub**  
Utilizado para documentação e organização do projeto.

**GitHub Projects**  
Utilizado para gerenciamento do backlog, épicos, User Stories, Tasks e acompanhamento do desenvolvimento utilizando Kanban.

Em versões futuras poderá ser utilizado:

**Power Automate**  
Para automações e notificações.

---

## 10. Tipo da Aplicação

O aplicativo será desenvolvido como um **Canvas App** no Microsoft Power Apps.

A escolha permite maior liberdade para construção da interface, organização das telas e estudo dos componentes da plataforma.

---

## 11. Estrutura Inicial de Telas

O aplicativo deverá possuir inicialmente:

### Dashboard

Tela principal contendo o resumo financeiro do mês.

### Receitas

Tela responsável pelo cadastro e consulta das entradas financeiras.

### Despesas

Tela responsável pelo cadastro, edição e consulta dos gastos.

### Planejamento

Tela responsável pela definição de orçamento e metas financeiras.

### Perfil

Área destinada às informações e preferências do usuário.

---

## 12. Metodologia de Desenvolvimento

O projeto será organizado utilizando conceitos de desenvolvimento ágil.

As funcionalidades serão divididas em:

**Épicos → User Stories → Tasks**

O desenvolvimento será acompanhado utilizando um quadro Kanban no GitHub Projects.

Os principais status serão:

**Backlog → Ready → In Progress → Testing → Done**

---

## 13. Critério de Sucesso do MVP

O MVP será considerado concluído quando o usuário conseguir:

1. registrar sua renda;
2. cadastrar suas despesas;
3. consultar despesas cadastradas;
4. identificar despesas pagas e pendentes;
5. visualizar quanto recebeu;
6. visualizar quanto gastou;
7. visualizar seu saldo disponível;
8. acompanhar os principais gastos por categoria;
9. definir uma meta de economia;
10. acompanhar essas informações por meio de um dashboard.

---

## 14. Evolução do Projeto

Após a conclusão do MVP, novas funcionalidades poderão ser planejadas em versões futuras.

O objetivo será evoluir o aplicativo gradualmente, utilizando cada nova funcionalidade como oportunidade para estudar novos recursos do ecossistema Microsoft Power Platform.
