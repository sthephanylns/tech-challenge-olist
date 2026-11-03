# Olist: Onde investir para continuar crescendo

**Tech Challenge – Fase 1 · POSTECH Data Analytics (FIAP)**
**Autora:** Sthephany Nascimento · RM 377624

Análise dos dados do e-commerce Olist para um relatório voltado a investidores, com foco em vendas, entrega e satisfação do cliente.

**Pergunta norteadora:** O crescimento da Olist vai continuar? E onde vale mais a pena investir para isso acontecer?

## Principais resultados

| Tema | O que encontrei |
|---|---|
| Crescimento | A receita de jan–ago/2018 foi **138% maior** que no mesmo período de 2017 (o mercado cresceu 12%). Mas desde jan/2018 as vendas pararam de subir |
| Entrega | O pedido leva em média **12,6 dias** para chegar, e a Olist promete cerca de 24. **6,8%** dos pedidos atrasam, chegando a 19% nos meses de pico |
| Satisfação | Nota média **4,3** quando chega no prazo e **2,3** quando atrasa |
| Regiões | Em SP o pedido chega em 9 dias; no Norte, de 20 a 29. No Norte, o frete chega a 36% do preço do produto |
| Oportunidade | Norte e Nordeste têm 36% da população, mas fazem só 11% dos pedidos |
| Recompra | Só **3%** dos clientes compraram mais de uma vez |
| Previsão | Cerca de **R$ 4,3 milhões** de set a dez/2018, com uns 10 mil pedidos na Black Friday |

**Recomendação central:** investir em entregas mais rápidas, principalmente fora do Sudeste e nas datas de pico, e criar ações para o cliente voltar a comprar.

## O que tem neste repositório

├── techchallengeolistfase1.ipynb                       # notebook com toda a análise
├── Olist onde investir para continuar crescendo.pptx   # apresentação executiva
├── figuras/                                            # gráficos gerados pelo notebook
├── requirements.txt                                    # bibliotecas usadas
└── README.md

## Como rodar

1. Baixe os dados no Kaggle: [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) (arquivo `archive.zip`).
2. Abra o notebook no [Google Colab](https://colab.research.google.com) (*Arquivo → Fazer upload de notebook*).
3. Clique em *Ambiente de execução → Executar tudo* e envie o `archive.zip` quando o notebook pedir.

Os dados não estão no repositório porque são grandes (cerca de 120 MB). Eles podem ser baixados direto no Kaggle.

## Como fiz

- **Metodologia:** CRISP-DM (entender o negócio, entender e preparar os dados, analisar e propor recomendações).
- **Tabelas usadas:** pedidos, itens, clientes, produtos, vendedores, pagamentos e avaliações, ligadas pelo `order_id` e pelo `customer_id`.
- **Receita:** valor dos produtos vendidos, sem frete, só de pedidos não cancelados.
- **Período das análises por mês:** jan/2017 a ago/2018. Os meses das pontas têm poucos pedidos.
- **Atraso:** pedido entregue depois da data prometida na compra.
- **Outliers:** identificados pelo método IQR e mantidos, porque são vendas reais.
- **Previsão:** média de mar–ago/2018 com o efeito da Black Friday e do Natal de 2017. É uma estimativa simples, porque há menos de 2 anos de dados.

## Dados externos

- Webshoppers (Ebit/Nielsen): o e-commerce brasileiro faturou R$ 53,2 bilhões em 2018, alta de 12%. [Fonte](https://www.tribunapr.com.br/noticias/economia/faturamento-do-e-commerce-soma-r-532-bilhoes-em-2018-alta-de-12/amp/)
- IBGE: estimativa da população por estado (2016), usada para calcular os pedidos por 100 mil habitantes. [Fonte](https://anda.ibge.gov.br/media/com_mediaibge/arquivos/03120a50001a6b5087c98b7a62f31665.pdf)

## Ferramentas

Python · pandas · NumPy · Matplotlib · Google Colab
