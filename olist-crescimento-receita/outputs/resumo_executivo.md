# Resumo executivo | Olist Crescimento e Receita

## Leitura do negócio
- **GMV dos produtos entregues:** R$ 13.221.498,11.
- **Pedidos entregues com itens:** 96,478.
- **Ticket médio:** R$ 137,04.
- **Categoria de maior receita:** health_beauty, com 9,3% do GMV.
- **Participação das 10 maiores categorias:** 62,4% do GMV.
- **Principal UF de consumo:** SP, com 38,3% do GMV.
- **Principal município de consumo:** Sao Paulo / SP.
- **10% de sellers com maior GMV:** concentram 67,1% das vendas dos sellers analisados.

## Recomendações orientadas por evidência
1. **Defender e desenvolver as categorias líderes.** Avaliar disponibilidade, mix e campanhas nas categorias mais representativas, acompanhando receita e conversão antes de ampliar orçamento. Categoria principal: health_beauty.
2. **Fazer testes regionais.** Priorizar análise de potencial em UFs relevantes e comparar crescimento incremental por região; SP lidera a receita observada, mas liderança não prova maior retorno marginal.
3. **Gerir concentração de sellers.** Criar plano de continuidade e diversificação da oferta se dependência dos maiores vendedores representar risco; top 10% concentram 67,1% do GMV.
4. **Acelerar produtos vencedores com proteção de margem.** Testar melhor posicionamento dos top produtos e medir conversão, recompra e margem antes de escalar.
5. **Instituir governança mensal.** Monitorar pedidos, GMV, ticket e composição por categoria e UF; validar meses parciais e alinhar métricas ao financeiro.

## Limitações
- O GMV aqui é soma do preço dos itens de pedidos entregues por data de compra; exclui frete, cancelados e não entregues.
- Base histórica Olist, sem leitura da performance atual e sem apuração de lucro, margem, comissão, taxa de devolução ou CAC.
- Períodos de fronteira do dataset podem ser incompletos; não extrapolar como previsão.

## Contexto externo | Ebit/Nielsen e IBGE
- **GMV Olist (jan–ago/2018 contra jan–ago/2017):** +141.1%.
- **Pedidos Olist (jan–ago/2018 contra jan–ago/2017):** +139.9%.
- **Faturamento do e-commerce brasileiro (2018 contra 2017, anos completos):** +12.2% (Webshoppers/Ebit-Nielsen).
- **Índice regional de presença relativa (2018):** maior valor em SP, 1.85; índice = share do GMV da amostra / share populacional do IBGE.

### Implicações de decisão
1. Validar capacidade de manter crescimento de pedidos sem deterioração de margem e serviço.
2. Executar pilotos de aquisição e logística em UFs de menor presença relativa, considerando tamanho econômico e custo de atendimento.
3. Priorizar categorias e sellers com retorno comprovado, mitigando concentração e monitorando custos.

### Cuidados metodológicos adicionais
- **Não** interpretar a diferença entre taxas da Olist e do mercado como ganho de market share: métrica e janelas diferentes (8 meses versus 12 meses), amostra limitada.
- A população é do ano-base 2018 e o GMV regional usa apenas compras de janeiro a agosto de 2018.
- Índice de presença não é demanda potencial, participação de mercado ou previsão de retorno.
- Referências: https://ftp.ibge.gov.br/Estimativas_de_Populacao/Estimativas_2018/POP2018_20220905.pdf ; https://www.terra.com.br/byte/receita-do-e-commerce-no-brasil-foi-de-r-532-bi-em-2018-diz-estudo,586591935998801e529b01f0566a08fdt0ugp598.html

## Alavancas de crescimento e decisões condicionais
- **Jan–ago/2017:** 21,998 pedidos, R$ 2.993.456,13 de GMV e R$ 136,08 de ticket.
- **Jan–ago/2018:** 52,783 pedidos, R$ 7.218.125,12 de GMV e R$ 136,75 de ticket.
- **Ponte do GMV:** efeito volume R$ 4.189.178,42; efeito ticket R$ 14.791,15; interação R$ 20.699,41.

### Cenários hipotéticos em uma janela equivalente de 8 meses (NÃO previsões)
- **Conservador:** pedidos +5%, ticket +0% ⇒ R$ 7.579.031,38 de GMV hipotético (+5.0% vs. jan–ago/2018).
- **Base:** pedidos +10%, ticket +3% ⇒ R$ 8.178.135,76 de GMV hipotético (+13.3% vs. jan–ago/2018).
- **Otimista:** pedidos +15%, ticket +5% ⇒ R$ 8.715.886,08 de GMV hipotético (+20.8% vs. jan–ago/2018).

### Priorização regional (triagem ilustrativa)
- **UFs elegíveis:** BA, CE, PE, GO. Critérios: população ≥ 3,000,000, pedidos ≥ 500, índice de presença < 0.85. Ranking por diferença de participação da população e do GMV em pontos percentuais.
- **Não representa demanda não atendida, market share, ROI, causalidade ou retorno previsto.** Os resultados mudam conforme os limites configurados; ver planilha `Robustez`.

### Recomendação ao comitê
Executar testes controlados e escalonar investimentos **somente** após comprovar margem de contribuição incremental positiva, custos de aquisição aceitáveis e qualidade do serviço, dados indisponíveis na amostra. Reavaliar em 30, 60 e 90 dias.

### Rastreabilidade dos resultados
- Abas: Decomposicao, Cenarios, Sensibilidade, Priorizacao_UF, Robustez, Plano_90d.
- Fonte interna: Olist (pedidos entregues, itens); fontes externas: IBGE (população UF 2018) e Ebit/Nielsen (faturamento do e-commerce brasileiro em 2017 e 2018).
- Cenários = sensibilidade sobre o GMV jan–ago/2018; **não há previsão estatística** nem dados de margem/CAC.
