# Regras de Negócio — Meu Orçamento

## 1. Objetivo

Este documento apresenta as regras de negócio do aplicativo **Meu Orçamento**.

As regras de negócio definem comportamentos, cálculos e restrições que devem ser respeitados pelo sistema durante o cadastro, consulta e processamento das informações financeiras.

---

# 2. Regras Gerais

## RN01 — Associação dos dados ao usuário

Toda receita, despesa e planejamento cadastrado deverá estar associado ao usuário autenticado no aplicativo.

O usuário deverá visualizar apenas os registros relacionados à sua própria conta.

---

## RN02 — Identificação do período

Toda movimentação financeira deverá estar relacionada a um período de referência.

O período será determinado por:

- mês;
- ano.

Exemplo:

Setembro de 2026.

---

## RN03 — Valores financeiros positivos

Receitas, despesas, metas e limites de orçamento deverão possuir valores maiores que zero.

O sistema não deverá aceitar valores negativos.

---

## RN04 — Campos obrigatórios

Os registros somente poderão ser salvos quando os campos obrigatórios estiverem preenchidos corretamente.

---

# 3. Regras de Receitas

## RN05 — Receita considerada no mês

Uma receita deverá ser considerada no total mensal com base na data informada no cadastro.

Exemplo:

Uma receita cadastrada com data em 10/09/2026 será contabilizada no mês de setembro de 2026.

---

## RN06 — Salário como categoria de receita

O salário será tratado como um tipo de receita.

O usuário poderá possuir outras receitas no mesmo mês.

Exemplo:

- Salário;
- Freelancer;
- Venda;
- Reembolso;
- Outros.

---

## RN07 — Soma das receitas

O total de receitas do período deverá corresponder à soma de todas as receitas cadastradas para o mês e ano selecionados.

**Fórmula:**

Total de Receitas = Soma das Receitas do Período

---

# 4. Regras de Despesas

## RN08 — Classificação obrigatória da despesa

Toda despesa deverá possuir uma categoria.

Exemplos:

- Moradia;
- Alimentação;
- Transporte;
- Educação;
- Saúde;
- Lazer;
- Assinaturas;
- Contas;
- Outros.

---

## RN09 — Tipo da despesa

Toda despesa deverá ser classificada como:

- Fixa;
- Variável.

---

## RN10 — Despesa fixa

Uma despesa fixa representa um gasto recorrente ou previsível.

Exemplos:

- aluguel;
- internet;
- faculdade;
- assinatura.

A classificação como fixa não implicará, inicialmente, criação automática da despesa nos meses seguintes.

A recorrência automática poderá ser implementada em versões futuras.

---

## RN11 — Despesa variável

Uma despesa variável representa gastos cujo valor ou ocorrência pode mudar ao longo do tempo.

Exemplos:

- mercado;
- combustível;
- lazer;
- compras.

---

## RN12 — Status da despesa

Toda despesa deverá possuir um dos seguintes status:

- Pendente;
- Pago.

---

## RN13 — Despesa pendente

Uma despesa pendente representa uma obrigação financeira ainda não quitada.

---

## RN14 — Despesa paga

Uma despesa marcada como paga representa um gasto que já foi efetivamente realizado.

---

## RN15 — Alteração de status

O usuário poderá alterar o status de uma despesa de Pendente para Pago.

Também poderá alterar de Pago para Pendente em caso de correção de cadastro.

---

# 5. Regras de Cálculo

## RN16 — Total de despesas

O total de despesas do mês corresponderá à soma das despesas cadastradas no período selecionado.

**Fórmula:**

Total de Despesas = Soma das Despesas do Período

---

## RN17 — Saldo financeiro

O saldo disponível será calculado utilizando:

**Saldo = Total de Receitas − Total de Despesas**

Exemplo:

Receitas: R$ 5.000

Despesas: R$ 3.200

Saldo: R$ 1.800

---

## RN18 — Saldo negativo

Caso o total de despesas seja superior ao total de receitas, o saldo poderá assumir valor negativo.

Exemplo:

Receitas: R$ 4.000

Despesas: R$ 4.500

Saldo: -R$ 500

O sistema deverá apresentar visualmente que o orçamento foi excedido.

---

## RN19 — Percentual da renda utilizada

O percentual da renda utilizada deverá ser calculado utilizando:

**Percentual utilizado = (Total de Despesas ÷ Total de Receitas) × 100**

Exemplo:

Receitas: R$ 5.000

Despesas: R$ 3.000

Percentual utilizado: 60%

---

## RN20 — Receita igual a zero

Caso não existam receitas cadastradas no período, o sistema não deverá tentar calcular o percentual da renda utilizada utilizando divisão por zero.

Nessa situação, deverá apresentar valor igual a zero ou uma indicação de que não existem receitas cadastradas.

---

# 6. Planejamento Financeiro

## RN21 — Planejamento por período

Cada planejamento deverá estar associado a um mês e ano.

Exemplo:

Planejamento de setembro de 2026.

---

## RN22 — Um planejamento mensal ativo

O usuário deverá possuir apenas um planejamento principal para cada combinação de mês e ano.

---

## RN23 — Meta de economia

A meta de economia representa o valor que o usuário pretende manter disponível ao final do período.

---

## RN24 — Valor disponível para economia

O valor efetivamente disponível para economia será calculado por:

**Valor disponível = Total de Receitas − Total de Despesas**

---

## RN25 — Progresso da meta de economia

O sistema poderá comparar o saldo disponível com a meta definida.

Exemplo:

Meta de economia: R$ 1.000

Saldo atual: R$ 750

Progresso da meta: 75%

---

## RN26 — Meta atingida

A meta será considerada atingida quando:

**Saldo disponível ≥ Meta de economia**

---

# 7. Limites por Categoria

## RN27 — Limite de categoria

O usuário poderá definir um limite máximo de gastos para determinadas categorias.

Exemplo:

Alimentação: R$ 800.

---

## RN28 — Cálculo do gasto por categoria

O valor utilizado de cada categoria deverá ser calculado através da soma das despesas pertencentes àquela categoria no período selecionado.

---

## RN29 — Percentual utilizado da categoria

O percentual utilizado será calculado utilizando:

**Percentual = (Gasto da Categoria ÷ Limite da Categoria) × 100**

---

## RN30 — Limite excedido

Quando o valor gasto em uma categoria ultrapassar o limite definido, o sistema deverá indicar visualmente que o orçamento daquela categoria foi excedido.

---

# 8. Dashboard

## RN31 — Período padrão

Ao abrir o Dashboard, o sistema deverá utilizar inicialmente o mês e ano atuais.

---

## RN32 — Alteração do período

O usuário poderá alterar o período de visualização para consultar meses anteriores.

---

## RN33 — Atualização das informações

Ao alterar o período selecionado, todas as informações do Dashboard deverão ser recalculadas com base no novo período.

Isso inclui:

- receitas;
- despesas;
- saldo;
- percentual da renda utilizada;
- gastos por categoria;
- contas pendentes;
- progresso da meta.

---

## RN34 — Contas pendentes

A área de contas pendentes deverá apresentar apenas despesas cujo status seja Pendente.

---

# 9. Regras de Exclusão e Alteração

## RN35 — Confirmação de exclusão

Antes de excluir uma receita ou despesa, o sistema deverá solicitar confirmação do usuário.

---

## RN36 — Exclusão definitiva

Após a confirmação, o registro poderá ser excluído da fonte de dados.

Uma funcionalidade de lixeira ou recuperação poderá ser implementada futuramente.

---

## RN37 — Recalcular após alteração

Sempre que uma receita ou despesa for criada, editada ou excluída, os valores do Dashboard deverão refletir os dados atualizados.

---

# 10. Regras do MVP

## RN38 — Sem recorrência automática

Na primeira versão, despesas fixas não serão criadas automaticamente em meses futuros.

---

## RN39 — Sem integração bancária

Todas as receitas e despesas serão cadastradas manualmente pelo usuário no MVP.

---

## RN40 — Sem parcelamento automático

Compras parceladas não serão divididas automaticamente em parcelas na primeira versão.

Cada parcela poderá ser cadastrada manualmente caso necessário.

---

## RN41 — Sem notificações automáticas

O MVP não enviará notificações sobre vencimentos.

Essa funcionalidade poderá ser adicionada futuramente utilizando Power Automate.

---

# 11. Resumo dos Principais Cálculos

### Total de Receitas

**Soma das receitas do período.**

### Total de Despesas

**Soma das despesas do período.**

### Saldo

**Total de Receitas − Total de Despesas**

### Percentual da Renda Utilizada

**(Total de Despesas ÷ Total de Receitas) × 100**

### Progresso da Meta

**(Saldo Disponível ÷ Meta de Economia) × 100**

### Utilização de Categoria

**(Total Gasto na Categoria ÷ Limite da Categoria) × 100**
