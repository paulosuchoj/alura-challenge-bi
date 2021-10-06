# Semanas 03 e 04 - Alura Store

<p align="center">
  <img src="https://i.postimg.cc/gJppBcWt/alura-store-branco.png">
</p>

## Dashboard

O dashboard criado para a Alura Store pode ser acessado na web, através do seguinte link:

**[Dashboard Alura Store - Alura Challenge BI - Semanas 03 e 04](https://app.powerbi.com/view?r=eyJrIjoiMWUyOTBlYmMtNmUzMS00MWNlLTkxMDItMWM5MTE3ZDUxOGYwIiwidCI6IjJjNzUwYmUyLTVkYzAtNDRjNy04MzNjLTA5NGY4ZGE5NzljMyJ9&pageName=ReportSection8b2dd9e1c7f74bb92054)**

## Caso

A **Alura Store**, precisa entender como anda a sua área **financeira**, pensando em **hipóteses**.

Para esse fim, desenvolveremos um dashboard tático da área financeira de uma empresa, no qual vamos criar duas páginas, sendo uma delas exibindo um overview de toda a área financeira e a outra página  realizando uma análise de cenários.

## Conceitos

Alguns dos conceitos usados para as métricas desse dashboard são específicos da área financeira, então segue uma explicação breve de cada um deles

#### Lucro

O lucro é calculado como o valor recebido **proveniente da venda** de um produto ou serviço após **subtrair os gastos** com sua aquisição, ou fabricação. No caso da Alura Store, esse cálculo foi feito subtraindo-se da receita os valores de custo de produção, impostos e frete.

#### Receita

A receita é toda a entrada de dinheiro na empresa, **proveniente de suas atividades**, isso é, de todas as vendas de seus serviços, produtos, bens. Esse valor é considerado sem qualquer tipo de desconto, antes de fazer todos os cálculos de despesas, pagamentos de fornecedores e custos, impostos e afins.


## Páginas

O dashboard foi estruturado em um relatório com três páginas, Overview Financeiro, Simulação e Rankings. 

**Obs.:** Os dados acerca de cada elemento das páginas estará disposto da seguinte maneira abaixo:

- Propriedade: [Tabela de Origem] Dado (Cálculo)

### Página de Rosto

<p align="center">
    <img src="https://i.postimg.cc/4yJdPZY9/firefox-Tote-Zi-AXZf.jpg"/>
</p>

Serve apenas como uma capa do relatório e uma mensagem de boas-vindas. Possui um botão **Start** que leva à pagina de Overview.

### Overview

<p align="center">
  <img src="https://i.postimg.cc/3Nnwb6Gb/firefox-76c-Asw-Abdg.png">
</p>


Essa página é a visão geral da parte financeira da Alura Store, à partir da qual o cliente já pode observar a situação do departamento. Nela é possível observar as seguintes informações:

**Bloco de Indicadores Monetários**

<p align="center">
  <img src="https://i.postimg.cc/jj7LdMVL/firefox-Ebt-WL3o7-Mi.png">
</p>

Esse item é um conjunto com os indicadores monetários de Receita, Custos, Despesas, Lucro e Frete. Cada item é um **cartão** e eles contêm os seguintes dados:

- Receita
  - Campos: [_Medidas] Receita

- Custos
  - Campos: [_Medidas] Custos
- Despesas
  - Campos: [_Medidas] Despesas
- Lucro
  - Campos: [_Medidas] Lucro
- Frete
  - Campos: [_Medidas] Frete

**Despesas, Custos e Impostos por Mês**

<p align="center">
  <img src="https://i.postimg.cc/5N4Yq5zR/firefox-NO991mkh-XQ.png">
</p>

Esse item mostra a variação ao longo dos meses de despesas, custos e impostos da Alura Store. Ele é um **gráfico de linhas** com os seguintes dados:

- Eixo: [Pedido] Data da Compra (Mês)
- Valores: [\_Medidas] Despesas, [\_Medidas] Custos, [\_Medidas] Impostos

**Lucro por Mês**

<p align="center">
  <img src="https://i.postimg.cc/0yrzh8cG/firefox-YO3a-KYDGHR.png">
</p>

Essa visualização mostra a composição dos lucros da Alura Store distribuídos por mês, permitindo saber em quais meses a empresa mais gera lucro no ano.

Ele é um **gráfico de cascata** com os seguintes dados:

- Categoria: [Pedidos] Data da Compra
- Valores: [\_Medidas] Lucro
- Dica de Ferramentas: Tooltip

**Filtro de Ano**

<p align="center">
    <img src="https://i.postimg.cc/7ZGKwJVm/image.png" />
</p>

Esse item é uma **segmentação de dados** que permite filtrar toda a página do relatório por ano de operação da Alura Store. Ele contém os seguintes dados:

- Campo: [Pedidos] Data da Compra (Ano)

**Filtro de Vendedor**

<p align="center">
    <img src="https://i.postimg.cc/T1NBHMdw/image.png" />
</p>

Esse item é uma **segmentação de dados** que permite filtrar toda a página do relatório pelo vendedor que gerou os resultados de operação da Alura Store. Ele contém os seguintes dados:

- Campo: [Vendedores] Nome do Vendedor

### Simulação

<p align="center">
  <img src="https://i.postimg.cc/NMF9Fxyw/firefox-31-QRAi-Gv5-N.png">
</p>

Essa página é um dos principais pedidos do cliente Alura Store. Através dela é possível criar predições e cenários financeiros da empresa com a mudança das variáveis de demanda, despesas, preço dos produtos e custos de produção destes.

Os filtros variam de -1 a 1 (que traduzem-se de redução de 100% a aumento de 100%), variando meio ponto percentual a cada passo.

**Indicadores Financeiros Simulados**

<p align="center">
  <img src="https://i.postimg.cc/RVg3P3QV/firefox-x-Cu-E9-IYwg-D.png">
</p>

Esse item é um conjunto com os indicadores monetários simulados de Receita, Despesas, Custos e Lucro. Cada item é um **cartão** e eles contêm os seguintes dados:

- Receita Simulada
  - Campos: [_Cenários] Receita

- Custos Simulados
  - Campos: [_Cenários] Custos
- Despesas Simuladas
  - Campos: [_Cenários] Despesas
- Lucro Simulado
  - Campos: [_Cenários] Lucro

**Filtros de Simulação**

<p align="center">
  <img src="https://i.postimg.cc/Sx5nhwvB/firefox-6m-DDr-Oav-S9.png">
</p>

Esse item é um conjunto de quatro **segmentações de dados**, que são a chave para o funcionamento desse relatório de simulação. Através dos sliders é possível configurar a variação de cada um dos indicadores, conforme a descrição, e verificar a alteração em todos os demais itens do cenário:

- Variação de Demanda
  - Campos: [Cenário Demanda] Cenário Demanda
- Variação Despesas
  - Campos: [Cenário Despesas] Cenário Despesas
- Variação Preço Produto
  - Campos: [Cenário Preço Produto] Cenário Preço Produto
- Variação Custos
  - Campos: [Cenário Custos] Cenário Custos

**Lucro Simulado por Mês**

<p align="center">
  <img src="https://i.postimg.cc/ydCWJ0Bn/firefox-GEBc-XQGWy-Q.png">
</p>

Possui função análoga à do gráfico de lucro incluso na página de Overview, mas leva em consideração os valores simulados para plotar as colunas.

Ele é um **gráfico de cascata** com os seguintes dados:

- Categoria: [Pedidos] Data da Compra
- Valores: [\_Cenários] Lucro Cenário
- Dica de Ferramentas: Tooltip

**Botão de Reset**

<p align="center">
  <img src="https://i.postimg.cc/qvgKZQCg/firefox-7tot-F1-PXlj.png">
</p>

O botão de reset é uma **imagem** que permite retornar todos os indicadores simulados e os sliders de variação ao seu estado original. O indicador utilizado nela para essa ação deve primeiro ser definido na aba Exibição > Indicadores, e então basta adicionar um novo à lista e nomeá-lo de Sem Filtro.

Ela está configurada da seguinte maneira:

- Ação 
  - Tipo: Indicador
  - Indicador: Sem Filtro

### Rankings

<p align="center">
  <img src="https://i.postimg.cc/13BNBpNt/firefox-Cyg-QK6si-Vj.png">
</p>

A última visualização do dashboard, essa página mostra indicadores relacionados aos vendedores e aos produtos da Alura Store. Ela agrega a receita e quantidade de pedidos de cada vendedor, as top 5 categorias de produtos mais vendidos e que geram mais renda, bem como a quantidade de pedidos feitos por mês.

**Top 5 Categorias de Produtos Mais Vendidos**

<p align="center">
  <img src="https://i.postimg.cc/wjJjtwfs/firefox-q3-KGdgrjim.png">
</p>

Visualização que mostra as top 5 categorias de produtos que mais são vendidos na Alura Store. É interessante notar como não são exatamente as mesmas top 5 que mais geram receita, que podem ser visualizadas no gráfico na parte inferior do relatório.

Esse item é um gráfico de **colunas empilhadas** com os seguintes dados:

- Eixo: [Produtos] Categoria do Produto
- Valores: [Pedidos] Quantidade
- Filtros: [Produtos] Categoria do Produto é N Superior = 5 por valor [Pedidos] Quantidade

**Quantidade de Pedidos por Mês**

<p align="center">
  <img src="https://i.postimg.cc/tTrq0wT8/firefox-l8o-OTWh-HSS.png">
</p>

Esse item é um **gráfico de linha** que permite ver a distribuição de quantidade de pedidos por mês ao longo do ano. Ele possui os seguintes dados:

- Eixo: [Pedidos] Data da Compra
- Valores: [Pedidos] Quantidade

**Top 5 Categorias que Geram Mais Receita**

<p align="center">
  <img src="https://i.postimg.cc/6qy9Bc4q/firefox-pdl-JDn-Gkb-V.png">
</p>

Assim como o outro **gráfico de colunas empilhadas**, essa visualização é um top 5, mas que mostra as categorias de produtos que mais geram receita para a Alura Store. Ele está configurado com os seguintes dados:

- Eixo: [Produtos] Categoria do Produto
- Valores: [\_Medidas] Receita
- Filtros: [Produtos] Categoria do Produto é N Superior = 5 por valor [\_Medidas] Receita

**Receita por Vendedor**

<p align="center">
  <img src="https://i.postimg.cc/Prgm70Cv/firefox-RRa-Zmg-G4v-P.png">
</p>

**Gráfico de pizza** que permite visualizar a receita gerada por cada um dos vendedores da equipe da Alura Store. Ele possui a seguinte configuração:

- Legenda: [Vendedores] Nome do Vendedor
- Valores: [\_Medidas] Receita

**Quantidade de Pedidos por Vendedor**

<p align="center">
  <img src="https://i.postimg.cc/MGDVvTd1/firefox-o-JC2-URL0-HL.png">
</p>

**Gráfico de rosca** com a visualização de quantidade de pedidos fechados por cada vendedor da Alura Store. Contém os seguintes dados:

- Legenda: [Vendedores] Nome do Vendedor
- Valores: [\_Medidas] Receita

**Filtro de Ano**

<p align="center">
  <img src="https://i.postimg.cc/nhpDqdrg/firefox-U8f-UGo-FN2c.png">
</p>

**Segmentação de dados** utilizada para filtrar o relatório como um todo e refletir a situação do ano selecionado, permitindo ver a evolução dos vendedores e dos rankings da loja. Está configurado da seguinte maneira:

- Campo: [Pedidos] Data da Compra (Ano)

## Medidas e Fórmulas

### Tabela de Medidas

| Medida                              |                           Fórmula                           |
| ----------------------------------- | :---------------------------------------------------------: |
| Custos                              |                    SUM(Produtos[Custos])                    |
| Despesas                            | SUM('Notas Fiscais'[Imposto]) + SUM('Notas Fiscais'[Frete]) |
| Frete                               |                 SUM('Notas Fiscais'[Frete])                 |
| Impostos                            |                SUM('Notas Fiscais'[Imposto])                |
| Receita                             |            SUM('Notas Fiscais'[Valor da Venda])             |
| Lucro                               |              [Receita] - [Custos] - [Despesas]              |
| Total de Compras                    |               SUM('Idade e Genero'[Compras])                |
| Valor Total de Conversão de Compras |    SUM('Idade e Genero'[Valor de conversão de compras])     |
| Valor Total Investido               |         SUM('Idade e Genero'[Quantia gasta (BRL)])          |

### Tabela de Cenários

| Medida           |                           Fórmula                            |
| ---------------- | :----------------------------------------------------------: |
| Custos Cenário   | SUMX(Pedidos, Pedidos[Quantidade] * Pedidos[Produtos.Custos]) * (1 + 'Cenário Custos'[Cenário Custos Valor]) |
| Despesas Cenário | SUM('Notas Fiscais'[Frete]) + SUM('Notas Fiscais'[Imposto]) + (1 + 'Cenário Despesas'[Cenário Despesas Valor]) + (1 + 'Cenário Preço Produto'[Cenário Preço Produto Valor]) |
| Lucro Cenário    |  [Receita Cenário] - [Custos Cenário] - [Despesas Cenário]   |
| Receita Cenário  | SUMX(Pedidos, Pedidos[Quantidade] * (1 + 'Cenário Demanda'[Cenário Demanda Valor]) * RELATED(Produtos[Preço]) * (1 + 'Cenário Preço Produto'[Cenário Preço Produto Valor])) |

## ETL

- As tabelas foram todas renomeadas da seguinte maneira:
  - financeiros notas_fiscais > Notas Fiscais
  - financeiro pedidos > Pedidos
  - financeiro produtos > Produtos
  - financeiro vendedores > Vendedores

**Notas Fiscais**

- Criação da coluna `Frete Corrigido` com a fórmula `Table.AddColumn(#"Colunas Renomeadas", "Frete Corrigido", each [frete_old] * 0.01)`
- Exclusão da coluna `frete`
- Exclusão da coluna `valor_venda`
- Criação da coluna `Valor da Venda` com a fórmula `Table.AddColumn(#"Colunas Removidas", "Valor da Venda", each [Frete Corrigido] * 10)`
- renomeação das colunas `id_nota`, `numero_nota`, `id_pedido`, `id_vendedor`, `valor_venda` para `ID da Nota Fiscal`, `Numero da Nota Fiscal`, `ID do Pedido`, `ID do Vendedor`, `Valor da Venda`
- Ajuste dos tipos das colunas de acordo com seus dados
- substituição de todos os valores 6 por 5 na coluna `ID do Vendedor`, uma vez que o mesmo vendedor estava duplicado na tabela de vendedores e possuía os IDs 3 e 6

**Pedidos**

- Ajuste dos tipos das colunas de acordo com seus dados
- Criação de uma consulta mesclada a fim de incluir na tabela de Pedidos o Custo vindo da tabela Produtos, para auxiliar no cálculo final de custo de produção da Alura Store

**Produtos**

- renomeação da coluna `id_produto` para `ID do Produto`
- Ajuste dos tipos das colunas de acordo com seus dados
- Normalização das categorias de produtos (cada letra em maiúscula, remoção de `_`, remoção de duplicatas e correção de nomes)
- Renomeação da coluna `categoria_produto` para `Categoria do Produto`
- substituição de `_` por `" "` na coluna categoria produto

**Vendedores**

- Renomeação de `id_vendedor` e `nome_vendedor` para `ID do Vendedor` e `Nome do Vendedor`
- Normalização dos nomes dos vendedores (cada letra em maiúscula, remoção de `_`, remoção de duplicatas e correção de nomes)
- Transformação de todas as colunas de id para texto

### Diagrama Relacional

<p align="center">
  <img src="https://i.postimg.cc/wTdPYfXf/Xp-T7-Hz-HOEZ.png">
</p>



## Melhorias e Aprendizados

### O Que Aprendi

- Utilização de parâmetros (What If?)
- Criação de página de simulação de cenários financeiros com o uso dos parâmetros
- Criação de tooltips (dica de ferramenta) para exibir informações granulares em gráficos

### O Que Preciso Melhorar e Aprender

- Aprofundar mais o conhecimento de SQL
- Entender melhor sobre os parâmetros dentro do Power BI, como eles funcionam e suas interações com os componentes de visualização de dados

## Referências

[Como calcular o lucro de uma empresa? Descubra!](https://www.contabilizei.com.br/contabilidade-online/como-calcular-o-lucro-de-uma-empresa-descubra/)

[O que é receita de empresa? ](https://www.capitalresearch.com.br/blog/investimentos/receita-de-empresa/)



<div>Os ícones foram  providenciados por <a href="https://www.flaticon.com/authors/smashicons" title="Smashicons">Smashicons</a> do site <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div>

