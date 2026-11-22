# Esquema dos ficheiros (edição n.º 1)

Separador: vírgula. Decimais: ponto. Codificação: UTF-8. Valores em euros, sem IVA.

## `custo-por-nicho.csv`

| Coluna | Significado |
|---|---|
| `grupo` | `obras` (pintura, remodelação, fachadas e isolamento, trabalhos verticais), `eletricistas` (inclui carregadores para carros elétricos), `limpezas`, `obras_e_eletricistas`, `todas` |
| `contas` | Número de contas de Google Ads no grupo |
| `investimento_eur` | Soma do custo no período |
| `cliques` | Soma dos cliques nos anúncios |
| `pedidos` | Soma dos contactos medidos (ver o README) |
| `custo_por_pedido_eur` | `investimento_eur ÷ pedidos` |
| `custo_por_clique_eur` | `investimento_eur ÷ cliques` |
| `cliques_com_pedido_pct` | `pedidos ÷ cliques × 100` |
| `mediana_por_conta_eur` | Mediana do custo por pedido de cada conta; com 2 contas é a média das duas |

## `canais-de-contacto.csv`

| Coluna | Significado |
|---|---|
| `canal` | Ação de conversão principal que registou o pedido |
| `pedidos` | Pedidos registados por esse canal (8 contas) |
| `pct` | Percentagem do total de 135 |

O formulário só era medido em 2 das 8 contas.

## `evolucao-mensal-2026.csv`

As 8 contas juntas, por mês. Outubro vai de 1 a 21. Julho (24–31) fica fora: só havia uma conta ativa.

## `margens-estatisticas.csv`

| Coluna | Significado |
|---|---|
| `ic95_inferior_pct`, `ic95_superior_pct` | Intervalo de confiança de 95 % (Wilson) da taxa de cliques com pedido |
| `custo_por_pedido_margem_inferior_eur`, `custo_por_pedido_margem_superior_eur` | Custo por clique ÷ limites da taxa; mede só a incerteza da taxa |
