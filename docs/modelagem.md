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
| Title | Descrição | Uma linha de texto | Obrigatório |
| Valor | Valor recebido | Moeda (R$) | Obrigatório; maior que zero |
| DataRecebimento | Data de recebimento | Data, sem horário | Obrigatória |
| TipoReceita | Tipo de receita | Escolha única | Obrigatório |



## Lista Despesas

| Nome técnico | Nome amigável | Tipo | Regra |
| --- | --- | --- | --- |
| Title | Descrição | Uma linha de texto | Obrigatório |
| Valor | Valor da despesa | Moeda (R$) | Obrigatório; maior que zero |
| DataDespesa | Data da despesa | Data, sem horário | Obrigatória |
| DataVencimento | Vencimento | Data, sem horário | Obrigatória; inicialmente igual à data da despesa |
| Categoria | Categoria | Escolha única | Obrigatória |
| TipoDespesa | Tipo de despesa | Escolha única | `Fixa` ou `Variável` |
| Status | Situação | Escolha única | `Pendente` ou `Pago`; padrão: `Pendente` |
| DataPagamento | Data do pagamento | Data, sem horário | Opcional; preenchida ao marcar como pago |



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



