# Analise de Dados - AgroTech Solutions

## 1.Visão geral

Este projeto foi desenvolvido para a empresa fictícia AgroTech Solutions, com o objetivo de analisar os dados de vendas e estoque, identificar inconsistências na base de dados e transformar informações em indicadores que auxiliem a tomada de decisões gerenciais.

O trabalho foi desenvolvido utilizando MySQL, com a criação e manipulação da tabela tb_vendas_agro, aplicação de tratamentos nos registros e elaboração de consultas SQL para gerar relatórios e indicadores de desempenho (KPIs).

## 2. Como executar

Para executar o projeto, é necessário ter o MySQL instalado.

- Parte 1: Limpeza e correção dos dados.

- Parte 2: Análise dos dados tratados.

- Parte 3: Criação e análise de 10 indicadores (KPIs).

O código cria o banco de dados agropecuaria_db, cria a tabela tb_vendas_agro, insere os dados e realiza as etapas de tratamento e análise.

## 3.Dicionario de dados

### Colunas da tabela

- **`id`**: identificador único do registro, do tipo `INT`.
- **`produto`**: nome do produto, do tipo `VARCHAR(100)`.
- **`categoria`**: categoria à qual o produto pertence, do tipo `VARCHAR(50)`.
- **`fornecedor`**: nome do fornecedor do produto, do tipo `VARCHAR(100)`.
- **`estado`**: estado relacionado ao registro, do tipo `VARCHAR(50)`.
- **`quantidade`**: quantidade registrada do produto, do tipo `INT`.
- **`valor_unitario`**: valor de uma unidade do produto, do tipo `DECIMAL(10,2)`.
- **`data_venda`**: data registrada da venda, do tipo `DATE`.
- **`estoque`**: indica se o produto está disponível em estoque, do tipo `BOOLEAN`.

### Observações sobre os campos

- **Quantidade:** representa o número de unidades registradas do produto.
- **Estoque:** informa se o produto está disponível (`TRUE`) ou indisponível (`FALSE`).
- **Data da venda:** registra a data associada à venda.

## 4.Resultados do tratamento e do relatório gerencial

Na primeira etapa, foram identificados e corrigidos problemas nos dados, como nomes de produtos escritos incorretamente, diferenças na identificação de fornecedores, estados e categorias, além de valores e quantidades que precisavam de ajustes.

Também foram removidos registros duplicados, dados de teste e registros com datas inválidas.

Após o tratamento, a base passou de 75 para 68 registros. Foram mantidos 48 produtos disponíveis e 20 indisponíveis. A análise também identificou 6 fornecedores, 6 categorias e 8 estados.

Os resultados permitiram organizar melhor as informações e preparar a base para a criação dos indicadores.

## 5.Catálogo e resultados dos 10 KPIs

### KPI 01 — Percentual de produtos disponíveis

Tem como objetivo identificar a proporção de produtos disponíveis em relação ao total de registros. O cálculo considera os 48 produtos disponíveis divididos pelos 68 registros finais. O resultado foi de 70,59%.



### KPI 02 — Percentual do valor parado

Tem como objetivo identificar quanto do valor potencial do estoque está associado a produtos indisponíveis. O cálculo considera o valor potencial dos produtos indisponíveis em relação ao valor potencial total. O resultado foi de 29,79%, equivalente a R$ 326.690,50.

### KPI 03 — Produtos indisponíveis por categoria

Tem como objetivo identificar quais categorias concentram mais produtos indisponíveis. A categoria Defensivos apresentou 7 registros indisponíveis, seguida por Sementes, com 4; Grãos e Fertilizantes, com 3 cada; Rações, com 2; e Minerais, com 1.

### KPI 04 — Quantidade média por produto disponível

Tem como objetivo calcular a média de unidades registradas nos produtos disponíveis. Foram consideradas 5.681 unidades distribuídas entre 48 produtos disponíveis. O resultado foi de 118,35 unidades por produto.

### KPI 05 — Quantidade disponível por estado

Tem como objetivo identificar a distribuição da quantidade disponível entre os estados. O Paraná apresentou 1.777 unidades, seguido por Mato Grosso, com 1.510, e Mato Grosso do Sul, com 768. Esses três estados concentram uma parte significativa da quantidade disponível.

### KPI 06 — Valor potencial do estoque disponível

Tem como objetivo calcular o valor potencial do estoque disponível. O cálculo é realizado multiplicando a quantidade pelo valor unitário de cada produto disponível. O resultado total foi de R$ 769.784,00.

### KPI 07 — Valor potencial do estoque por fornecedor

Tem como objetivo identificar quais fornecedores representam os maiores valores potenciais no estoque disponível. O fornecedor Campo Verde apresentou R$ 334.995,00, seguido por Solo Forte, com R$ 140.840,00, e NutriCampo, com R$ 98.492,20.

### KPI 08 — Participação dos fornecedores nos registros

Tem como objetivo analisar a participação de cada fornecedor no total de registros. O fornecedor Campo Verde apresentou a maior participação, com 16 registros, equivalentes a 23,53% do total.

### KPI 09 — Valor médio por categoria

Tem como objetivo comparar o valor unitário médio dos produtos de cada categoria. Defensivos apresentou a maior média, com R$ 739,91, seguido por Fertilizantes, com R$ 296,74, e Grãos, com R$ 136,02.

### KPI 10 — Produtos com valor unitário acima de R$ 500

Tem como objetivo identificar a proporção de produtos com valor unitário igual ou superior a R$ 500. Foram identificados 11 produtos nessa condição, representando 16,18% dos 68 registros.

## Conclusão gerencial

A análise dos dados permitiu identificar pontos importantes para a gestão da AgroTech Solutions.

O primeiro destaque é que 29,79% do valor potencial do estoque está relacionado a produtos indisponíveis. Esse resultado indica a importância de acompanhar a disponibilidade dos produtos.

Outro ponto é a categoria Defensivos, que apresentou a maior quantidade de produtos indisponíveis e também o maior valor médio por categoria.

Além disso, o fornecedor Campo Verde apresentou o maior valor potencial no estoque disponível, demonstrando uma concentração relevante nesse fornecedor.

Com essas informações, a empresa pode melhorar o controle do estoque, acompanhar as categorias com maior indisponibilidade e analisar a distribuição dos produtos entre os fornecedores. O acompanhamento periódico dos KPIs pode auxiliar na identificação de problemas e na tomada de decisões.
