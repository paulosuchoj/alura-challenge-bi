# Semana 01 - Alura Log

[alura-log.png](https://postimg.cc/4YJSv847)

## Dashboard

O dashboard criado para a Alura Log pode ser acessado na web, através do seguinte link:

**[Dashboard Alura Log - Alura Challenge BI - Semana 01](https://app.powerbi.com/view?r=eyJrIjoiMmZmYWQ1NzItMTA5MS00ODJjLWI3ZjQtNjJmNTA4Y2YwYjMyIiwidCI6IjJjNzUwYmUyLTVkYzAtNDRjNy04MzNjLTA5NGY4ZGE5NzljMyJ9&pageName=ReportSection)**

## Caso

A pessoa que gerencia a área de logística da Alura Log, está enfrentando algumas mudanças em sua área por conta do aumento da demanda dos serviços de logística no período da pandemia. Ela quer manter a qualidade de seu serviço, mas para isso precisa acompanhar constantemente as métricas do seu departamento para tomar as melhores decisões. Quando nos contou isso, analisamos que para auxiliar nesse desafio precisaremos fazer um dashboard para logística. Para isso, vamos visualizar algumas métricas muito importantes para a área.

## Páginas
O dashboard foi estruturado em três relatórios ou páginas diferentes: Geral, Frota e Financeiro. Cada uma delas se foca em diferentes aspectos e insights possíveis de depreender a partir da massa de dados e das relações entre eles.

**Obs.: **Os dados acerca de cada elemento das páginas estará disposto da seguinte maneira abaixo:

- Propriedade: [Tabela de Origem] Dado (Cálculo)

### Geral

[PBIDesktop-du-KMXbeeq-F.png](https://postimg.cc/yJb436nf)

Essa página é uma visão geral da Alura Log, desenvolvida como uma tela de boas-vindas à partir da qual o cliente já pode observar a situação atual da empresa, um "snapshot". Nela é possível observar as seguintes informações:

**Volume de Estoque**

[PBIDesktop-6wryb0-IOpr.png](https://postimg.cc/r0z7N6zf)

Mostra a quantidade de itens no estoque por ano, bem como a média de itens acumulados.

É um **_gráfico de colunas empilhadas e linha_**, com os seguintes dados:

- Eixo compartilhado: [Estoque] Data da Atualização - Ano
- Valores da coluna: [Estoque] Quantidade
- Valores de linha: [Estoque] Quantidade (Média)

**Mapa de Entregas**

[PBIDesktop-Rwyn9-Dakc-G.png](https://postimg.cc/bdDKGj7J)

Visualização com círculos de diferentes tamanhos sobre um mapa do Brasil. O tamanho dos círculos indica o volume de entregas realizadas naquela região, baseando-se em dados de latitude e longitude.

É um **_mapa_**, com os seguintes dados:

- Localização: [Pedidos] País, [Pedidos] UF da Entrega, [Pedidos] Latitude, [Pedidos] Longitude
- Tamanho: [Pedidos] Quantidade

**S2D - Ship to Door**

[PBIDesktop-k-JAl6-HMShd.png](https://postimg.cc/gLZ51vVR)

Essa visualização é muito interessante, e mostra a quantidade média de dias que um pedido demora para sair do centro de distribuição após a compra e chegar até a casa do comprador. A classificação das médias é feita por mês.

É um **_gráfico de linhas_**, com os seguintes dados:

- Eixo: [Pedidos] Data da Compra - Mês
- Valores: [Pedidos] S2D (Média)

**Volume e Status de Pedidos**

[PBIDesktop-FWIIzvq3v-D.png](https://postimg.cc/gX5QMMZm)

Bloco que contém as informações de quantos pedidos já foram atendidos pela Alura Log, divididos em: quantos foram entregues no prazo estipulado, quantos estão em trânsito e quantos já estão estão ou foram entregues atrasados.

É um conjunto de **_cartões_**, **_imagens_** e **_caixas de texto_**. Os cartões contém os seguintes dados:

- *Total de Pedidos*

  - Campos: [Pedidos] ID do Pedido (Contagem)

    

- *Entregues no Prazo*

  - Campos: [Medidas] Pedidos Entregues no Prazo

    

- *Em Trânsito*

  - Campos: [Medidas] Pedidos em Trânsito

    

- *Em Atraso*

  - Campos: [Medidas] Pedidos Entregues em Atraso

### Frota

[PBIDesktop-IIy-MM6-LVUu.png](https://postimg.cc/wtvYBR5y)

A segunda página dá um resumo acerca da frota da Alura Log, que é composta por 50 veículos de tipos diferentes. Há também alguns dados da logística geral. A tela contém uma segmentação de dados por ano, na forma de botões. 

Nela estão as seguintes informações:

**Disponibilidade de Veículos**

[PBIDesktop-s-Rnrt-Kq995.png](https://postimg.cc/GHN4Gfxz)

Mostra a proporção de veículos disponíveis e ocupados da frota.

É um **_gráfico_** de rosca com os seguintes dados:

- Valores: [Medidas] Veículos Disponíveis, [Medidas] Veículos Ocupados

**Disponibilidade de Cada Tipo de Veículo**

Faz a separação da disponibilidade dos veículos da frota por cada tipo de veículo (caminhonetes, carros e motos).

É um conjunto de **_cartões_**, **_imagens_** e **_caixas de texto_**. Os cartões contém os seguintes dados:

- *Caminhonetes*
  - Disponíveis
    - Campos: [Veículos] Tipo (Contagem)
    - Filtros: [Veículos] Status é Disponível, [Veículos] Tipo é Caminhonete
  - Total na Frota
    - Campos: [Veículos] Tipo (Contagem)
    - Filtros: [Veículos] Tipo é Caminhonete
- *Carros*
  - Disponíveis
    - Campos: [Veículos] Tipo (Contagem)
    - Filtros: [Veículos] Status é Disponível, [Veículos] Tipo é Carro
  - Total na Frota
    - Campos: [Veículos] Tipo (Contagem)
    - Filtros: [Veículos] Tipo é Carro
- *Motos*
  - Disponíveis
    - Campos: [Medidas] Motos Disponíveis*****
  - Total na Frota
    - Campos: [Veículos] Tipo (Contagem)
    - Filtros: [Veículos] Tipo é Moto

*****Foi necessário utilizar uma medida específica para as motos disponíveis, para que o cartão não mostre "Em Branco", uma vez que a quantidade de motos disponíveis é 0 (zero).

**Distribuição de Status de Pedidos por Ano**

[PBIDesktop-0hvq2-F5d-Sd.png](https://postimg.cc/PCwP4M6H)

Esse gráfico mostra a quantidade de pedidos por cada mês no ano e seus status de entrega.

Ele é um **_gráfico de colunas empilhadas_**, com os seguintes dados:

- Eixo: [Pedidos] Data da Compra - Ano, Mês
- Valores: [Medidas] Pedidos em Atraso, [Medidas] Pedidos em Trânsito, [Medidas] Pedidos Entregues no Prazo

**Quantidade de Pedidos por Estado**

[PBIDesktop-g-L8185-Qe-LQ.png](https://postimg.cc/zV3LLNKV)

Visualização que mostra o total de pedidos feitos por compradores de cada estado. É notável a discrepância entre SP e RJ (com volume de pedidos de 36 e 30 mil, respectivamente) comparados aos demais estados do Brasil, cujos volumes flutuam sempre ao redor de 3 mil.

Ele é um **_gráfico de colunas empilhadas_**, com os seguintes dados:

- Eixo: [Pedidos] UF da Entrega
- Valores: [Pedidos] Quantidade (Contagem)

### Financeiro

Página que contém algumas visualizações da parte financeira da Alura Log. É focada em faturamento sob diversos ângulos, e possui componentes de segmentação de dados por ano e mês.

Nela estão as seguintes informações:

**Valor do Estoque Atual e Faturamento Total**

[PBIDesktop-hw-X4yx-YCF0.png](https://postimg.cc/k2W7DMMN)

Mostra o valor em R$ (reais) do estoque atual acumulado na última atualização, e o faturamento total da Alura Log.

São dois **_cartões_** com os seguintes dados:

- *Valor do Estoque Atual*
  - Campos: [Medidas] Valor do Estoque Atual
- *Faturamento Total*
  - Campos: [Medidas] Faturamento Total

**Estados com Maior Faturamento**

[PBIDesktop-D5gal-Ucwh-P.png](https://postimg.cc/HVqpp8ms)

Mostra, de maneira sintética e visual, o faturamento da Alura Log em cada estado. Mais uma vez fica visível a discrepância de SP e RJ com os demais estados. É necessário juntar o faturamento de ao menos 6 estados para se ter uma área quase do tamanho da do RJ no gráfico, por exemplo.

Esse componente é um **_treemap_** com os seguintes dados:

- Grupo: [Pedidos] UF da Entrega
- Valores: [Pedidos] Faturamento
- Filtros: [Pedidos] UF da Entrega é N Superior = 8 por valor [Pedidos] Faturamento

**Faturamento Total por Semestre**

[PBIDesktop-Zc-USt-VOTLS.png](https://postimg.cc/6y2WJLDm)

Exibe o faturamento semestral da Alura Log.

É um **_gráfico de área_** com os seguintes dados:

- Eixo: [Pedidos] Data da Compra - Ano, Mês
- Valores: [Pedidos] Faturamento

**Faturamento Total por Categoria**

[PBIDesktop-42-Gg-OFOO1-G.png](https://postimg.cc/HJHdMGjq)

Exibe a classificação das categorias de produtos entregues pela Alura Log, e quais são os que geram mais receita.

É um **_gráfico de barras clusterizado** com os seguintes dados:

- Eixo: [Produtos] Categoria do Produto
- Valores: [Pedidos] Faturamento
- Filtros: [Pedidos] Faturamento é N Superior = 10 por valor [Pedidos] Faturamento

## Medidas e Fórmulas
### Tabela de Medidas



```markdown
| Medida            | Fórmula |
|-------------------|---------|
| Faturamento       | SUM(Pedidos[Quantidade]) * SUM(Produtos[Preço]) |
| Faturamento Total | SUM(Pedidos[Faturamento]) + 0 |
| Motos Disponíveis | CALCULATE(COUNTROWS('Veículos'), Filter('Veículos', 'Veículos'[Tipo] = "Moto" && 'Veículos'[Status] = "Disponível")) + 0 |
| Pedidos em Atraso | CALCULATE(COUNTROWS(Pedidos), FILTER(Pedidos, Pedidos[Data de Entrega] > Pedidos[Data da Previsão de Entrega])) |
| Pedidos em Trânsito| CALCULATE(COUNTROWS(Pedidos), FILTER(Pedidos, Pedidos[Status do Pedido] = "Em Trânsito")) |
| Pedidos Entregues no Prazo | CALCULATE(COUNTROWS(Pedidos), FILTER(Pedidos, Pedidos[Data de Entrega] <= Pedidos[Data da Previsão de Entrega])) |
| Valor do Estoque Atual | SUMX(Estoque, Estoque[Quantidade] * RELATED(Produtos[Preço])) |
| Veículos Disponíveis | CALCULATE(COUNTROWS('Veículos'), FILTER('Veículos', 'Veículos'[Status] = "Disponível")) + 0 |
| Veículos Ocupados | COUNTROWS(FILTER('Veículos', 'Veículos'[Status] = "Ocupado")) |
```

## ETL
O processo de ETL foi todo feito através do Power BI, a partir dos 4 arquivos CSV originais (Tabela - Estoque, Tabela - Pedidos, Tabela - Veículos e Tabela - Produtos) fornecidos para a elaboração dos relatórios.

O tratamento de dados consistiu em:

- Pedidos
  - Ajustar tipos de dados e região de todas as colunas necessárias
  - Fazer a separação das colunas de data da compra, data da entrega e data da previsão para deixar a data em uma coluna e a hora em outra
  - Acertar os valores de latitude e longitude para não perder as casas decimais e corrigir sua região para que o Power BI reconhecesse a vírgula
  - Fazer uma consulta mesclada com a tabela de Produtos para adicionar à de Pedidos a coluna de Preço (feito após a criação de relacionamentos entre as tabelas)
  - Criar uma coluna customizada com a multiplicação de Quantidade por Preço, a fim de obter o faturamento de cada linha
  - Essa tabela possuía milhares de registros com células em branco na coluna de data da entrega, por conta dos pedidos em que ainda estão em trânsito. Os erros causados por esses valores em branco foram substituídos pelo valor null, para evitar críticas e desvios

- Estoque
  - A coluna de data da atualização originalmente estava preenchida com o formato dd-mmm.aaaa (01-jan.-2019, por exemplo. Ela foi ajustada para substituir o separador "-" por "/", e substituir todos os nomes abreviados dos meses por seus respectivos números
  - Essa mesma coluna, em sequência, foi quebrada em três para separar o dia, mês e ano
- Veículos
  - Foi feito apenas normalização dos dados (corte, limpeza) e renomeação das colunas para integridade entre as chaves primárias das relações (colunas de ID)
- Produtos
  - A coluna de categoria do produto estava preenchida, originalmente, com o formato 00-categoria_do_produto (1-agro_industria_e_comercio, por exemplo). Foi feita a substituição do separador "_" por " ", e a quebra da coluna pelo separador "-" para obter uma coluna de IDs.

### Diagrama Relacional

[PBIDesktop-Nn9-XEEw944.png](https://postimg.cc/mz3KYh1R)

## Melhorias e Aprendizados
### O Que Aprendi

Aprendi a usar componentes que ainda não tinha utilizado nos cursos e treinamentos da Alura. Também aprendi sobre conceitos como S2D.

Uma das descobertas mais interessantes foi a da mescla de consultas, utilizada para juntar as tabelas de Pedidos e Produtos através do ID do Produto, a fim de obter o Preço. Esse recurso é muito poderoso.

Também aprendi como fazer a navegação entre as páginas através de botões, imagens e elementos gráficos.

### O Que Reforcei

Criação de medidas, conceitos de ETL e normalização de dados e manipulação geral de dados através do PowerQuery e DAX.

### O Que Preciso Melhorar e Aprender

Layout geral do dashboard, como criação de temas, distribuição das informações e exibição coerente. É possível melhorar muito a qualidade e valor dos dashboards com técnicas de storytelling de dados.

Preciso aprender mais sobre as funções do DAX como SUM, COUNTROWS etc., há muitas delas que podem ser usadas para encurtar ou fazer medidas de maneira mais eficiente.

Explorar mais o Power BI "por baixo do capô" e aprender sobre M e mescla de consultas.

