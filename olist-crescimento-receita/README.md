# Olist | Crescimento e Receita

Análise exploratória do **Brazilian E-Commerce Public Dataset by Olist** com foco em desempenho comercial e decisões de investimento.

**Pergunta central:** De onde vem o crescimento comercial, quais categorias e regiões concentram as vendas e quais oportunidades devem ser investigadas?

## Entregas

- `notebooks/01_crescimento_receita.ipynb` — notebook reproduzível, análise descritiva, contexto externo, decomposição de crescimento, cenários hipotéticos e priorização regional.
- `outputs/tabelas_analiticas.xlsx` — tabelas analíticas e seis abas de avaliação de oportunidades: `Decomposicao`, `Cenarios`, `Sensibilidade`, `Priorizacao_UF`, `Robustez` e `Plano_90d`.
- `outputs/resumo_executivo.md` — síntese dos indicadores e recomendações.
- `outputs/cenarios_crescimento.csv` e `outputs/priorizacao_uf.csv` — tabelas complementares.
- `outputs/figures/` — gráficos gerados pelo notebook (o pacote apresenta os gráficos de decomposição, cenários, sensibilidade e triagem regional; os demais são reproduzidos na execução).
- `reports/relatorio_executivo_olist.pdf` e `.docx` — relatório executivo para investidores.
- `apresentacao/apresentacao_executiva_olist.pptx` — apresentação de storytelling executivo.

## Dados necessários

Copie para `data/raw/` estes **seis CSVs originais** do conjunto público Olist (não incluídos no pacote):

1. `olist_orders_dataset.csv`
2. `olist_order_items_dataset.csv`
3. `olist_products_dataset.csv`
4. `olist_product_category_name_translation.csv`
5. `olist_sellers_dataset.csv`
6. `olist_customers_dataset.csv`

As fontes externas estão em `data/external/`:

- `webshoppers_ebit_mercado_2017_2018.csv` — faturamento nacional do e-commerce em 2017 e 2018, baseado em Ebit/Nielsen.
- `ibge_populacao_uf_2018.csv` — população estimada das UFs pelo IBGE, ano-base 2018.

Os arquivos externos são locais e incluem informações de origem. Não é necessário acessar a internet para executar o notebook.

## Como executar

No terminal do VS Code, a partir da pasta do projeto (PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
jupyter lab
```

Abra `notebooks/01_crescimento_receita.ipynb`, escolha o kernel do ambiente `.venv` e execute todas as células (`Run All`). Pode usar seu ambiente já configurado, caso tenha as dependências instaladas.

A execução atualiza as figuras, a planilha e os CSVs dentro de `outputs/`, com **nomes neutros e consistentes**.

## Metodologia e definições

- **Pedidos**: `order_id` distintos de pedidos entregues com itens; referência temporal pela data da compra.
- **GMV**: soma de `order_items.price` de pedidos entregues; não inclui frete, cancelados ou não entregues. Não representa a receita contábil da Olist nem o lucro.
- **Ticket médio**: GMV dividido pelo número de pedidos entregues com itens.
- **Categoria, UF e município**: associação dos itens/produtos com clientes e sellers, utilizando suas chaves.
- **Comparação de crescimento**: janeiro–agosto de 2017 versus janeiro–agosto de 2018 para manter uma janela de oito meses.
- **Contexto de mercado**: faturamento anual do comércio eletrônico nacional (2017 e 2018), mostrado apenas como referência; janelas e métricas distintas impedem inferir ganho de market share.
- **Presença regional**: participação da UF no GMV da amostra dividida pela participação da UF na população de 2018; não mede demanda reprimida nem ROI.
- **Cenários**: análise hipotética de sensibilidade sobre o GMV janeiro–agosto de 2018, não previsão estatística, orçamento ou lucro.
- **Recomendações**: pilotos condicionados à mensuração de margem incremental, CAC, conversão, frete e qualidade de serviço, métricas não disponíveis no dataset.

## Reprodutibilidade

A pasta `data/raw/` fica fora do controle de versão para evitar publicação de CSVs transacionais volumosos. O `.gitignore` também exclui `.venv/`. O notebook exporta tabelas que permitem auditoria dos cálculos.

Leia `docs/GUIA_PUBLICACAO_GITHUB.md` antes de publicar o repositório e revise se as saídas são consistentes com o relatório e os slides.
