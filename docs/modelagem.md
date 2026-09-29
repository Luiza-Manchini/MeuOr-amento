# 05 — Modelagem de dados do MVP



## Visão geral

O aplicativo terá quatro listas no SharePoint:

| Lista | O que guarda |
| --- | --- |
| Receitas | Salário e outras entradas de dinheiro |
| Despesas | Gastos, vencimentos e situação do pagamento |
| Planejamentos | Planejamento e meta de economia de cada mês |
| LimitesCategoria | Limite de gastos por categoria em cada mês |



## Campos presentes nas quatro listas

| Nome técnico | Nome amigável | Tipo no SharePoint | Regra |
| --- | --- | --- | --- |
| UsuarioId | Usuário | Uma linha de texto | Obrigatório; preenchido pelo aplicativo com o identificador do usuário conectado |
| Periodo | Mês e ano | Número, sem casas decimais | Obrigatório; padrão: mês atual |
| ChaveUsuarioPeriodo | Chave do usuário e período | Uma linha de texto | Obrigatória; gerada pelo aplicativo, por exemplo `UsuarioId|202609` |



## Lista Receitas

| Nome técnico | Nome amigável | Tipo | Regra |
| --- | --- | --- | --- |
| `Title` | Descrição | Uma linha de texto | Obrigatório; preenchido pelo usuário |
| `Valor` | Valor recebido | Moeda (R$) | Obrigatório; maior que zero |
| `DataRecebimento` | Data de recebimento | Data, sem horário | Obrigatória; preenchida pelo usuário |
| `TipoReceita` | Tipo de receita | Escolha única | Obrigatório; opções: **Salário** e **Freelance** |
| `UsuarioId` | Identificador do usuário | Uma linha de texto | Obrigatório; preenchido pelo aplicativo com o ID da conta conectada |
| `Periodo` | Mês e ano da receita | Número, sem casas decimais | Obrigatório; calculado a partir de `DataRecebimento` no formato `AAAAMM` |
| `ChaveUsuarioPeriodo` | Chave do usuário e período | Uma linha de texto | Obrigatória; gerada pelo aplicativo a partir de `UsuarioId` e `Periodo`; **não é única** |



## Lista Despesas

| Nome técnico | Nome amigável | Tipo | Regra |
|---|---|---|---|
| Title | Descrição | Uma linha de texto | Obrigatório |
| Valor | Valor da despesa | Moeda (R$) | Obrigatório; maior que zero |
| DataDespesa | Data da despesa | Data, sem horário | Obrigatória |
| DataVencimento | Data de vencimento | Data, sem horário | Obrigatória |
| Categoria | Categoria | Escolha única | Obrigatória: Moradia, Alimentação, Transporte, Saúde, Educação, Lazer, Assinaturas ou Outros |
| TipoDespesa | Tipo de despesa | Escolha única | Obrigatório: Fixa ou Variável |
| Status | Status do pagamento | Escolha única | Obrigatório: Pendente ou Pago; padrão: Pendente |
| DataPagamento | Data do pagamento | Data, sem horário | Preenchida quando a despesa for paga |
| UsuarioId | Identificação do usuário | Uma linha de texto | Obrigatório; preenchido pelo aplicativo |
| Periodo | Mês do orçamento | Número inteiro (AAAAMM) | Obrigatório; escolhido conforme a receita que pagará a despesa |
| ChaveUsuarioPeriodo | Chave do usuário e período | Uma linha de texto | Obrigatória; preenchida pelo aplicativo no formato `UsuarioId|Periodo` |


## Lista Planejamentos

| Nome técnico | Nome amigável | Tipo | Regra |
| --- | --- | --- | --- |
| Title | Identificação | Uma linha de texto | Gerada pelo aplicativo, como `Planejamento 09/2026` |
| ReceitaPrevista | Receita esperada | Moeda (R$) | Opcional; se preenchida, maior que zero |
| MetaEconomia | Meta de economia | Moeda (R$) | Opcional; se preenchida, maior que zero |


## Lista LimitesCategoria

| Nome técnico | Nome amigável | Tipo | Regra |
| --- | --- | --- | --- |
| Title | Identificação | Uma linha de texto | Gerada pelo aplicativo, como `Alimentação 09/2026` |
| Categoria | Categoria | Escolha única | Obrigatória; mesmas opções da lista Despesas |
| ValorLimite | Limite de gastos | Moeda (R$) | Obrigatório; maior que zero |
| ChaveLimite | Chave do limite | Uma linha de texto | Obrigatória e única; combina usuário, período e categoria |



