# Semana 02 - Alura Shop

<p align="center">
  <img src="https://i.postimg.cc/fL1VLTrS/alura-shop-branco.png">
</p>




## Dashboard

O dashboard criado para a Alura Shop pode ser acessado na web, através do seguinte link:

**[Dashboard Alura Shop - Alura Challenge BI - Semana 02](https://app.powerbi.com/view?r=eyJrIjoiNDMzNDRjYWItNzk3Yi00MjhjLWJhYWUtYWZjNDBiOGExYWM0IiwidCI6IjJjNzUwYmUyLTVkYzAtNDRjNy04MzNjLTA5NGY4ZGE5NzljMyJ9&pageName=ReportSection)**

## Caso

Agora a Alura Shop **investiu** em publicidade para se destacar no mercado, e a gerência da empresa tem dúvidas se o retorno dessa propaganda **surtiu efeito**.

A nossa missão é apoiar a gerência em suas **tomadas de decisão**, e elucidar as dúvidas. Para isso desenvolveremos um dashboard estratégico de marketing com o objetivo de monitorar uma campanha de publicidade paga durante o mês de julho de 2021. Apresentaremos **indicadores relevantes** para a validação estratégica do negócio.

## Conceitos

Alguns dos conceitos usados para as métricas desse dashboard são bem específicos da área de marketing digital, então segue uma explicação breve de cada um deles

#### ROAS

A sigla vem do inglês _Return on Advertising Spend_, ou _Retorno Sobre o Investimento Publicitário_ em tradução livre. Essa métrica mede as receitas e custos envolvidos em uma campanha publicitária. É possível fazer um paralaleo dela com o ROI (_Return on Investment_, ou _Retorno Sobre Investimentos_), mas o ROAS é usado única e exclusivamente para acompanhar os anúncios pagos e demais gastos relacionados à publicidade da empresa ou negócio.

O cálculo do ROAS gera um número inteiro, e a recomendação dos analistas de marketing é que ele esteja sempre acima de 2, no mínimo.

#### Ticket Médio

Métrica que representa o valor médio gasto pelos clientes nos pedidos. Quanto maior o valor, mais os clientes estão gastando na loja, e assim o ticket médio pode mostrar o comportamento dos clientes em relação à marca e a satisfação com a empresa.

Recomenda-se que o valor do ticket médio seja analisado sempre dentro de um contexto histórico, a fim de verificar se ele está em ascenção, declínio ou estabilizado. Deve-se levar em conta também aspectos sazonais que possam afetar o negócio (aumento de vendas de sorvetes no verão em uma sorveteria, aumento de vendas de eletrônicos e roupas na época do natal, etc.)

#### Taxa de Conversão

Também conhecida em inglês como CVR (_Conversion Rate_), essa métrica é obtida com a divisão entre o número de visitantes em um site pela quantidade de conversões (que podem ser vendas, leads, clicks ou outro objetivo do negócio). No caso da Alura Shop, utilizou-se a quantidade de compras dividido pelo número de visualizações da página.

Essa métrica mostra o quão atrativos são seus produtos, experiência do cliente e preço, e qual a proporção de usuários engajados na campanha e transformados em clientes;



<p align="center">
  <img src="https://i.postimg.cc/Qx57SCTb/hgz8-PTpg2l.gif">
</p>

## Páginas

O dashboard foi estruturado em um único relatório conciso chamado Campanha. Esse relatório mostra, em uma única visão, todos os dados importantes requisitados pelo cliente em sua campanha de marketing digital.

**Obs.:** Os dados acerca de cada elemento das páginas estará disposto da seguinte maneira abaixo:

- Propriedade: [Tabela de Origem] Dado (Cálculo)

### Campanha

<p align="center">
  <img src="https://i.postimg.cc/pLZjyQHN/PBIDesktop-UVJK7vfs1-P.png">
</p>

Essa página é a visão geral da Alura Shop, à partir da qual o cliente já pode observar a situação atual da campanha de marketing digital, num "snapshot". Nela é possível observar as seguintes informações:

**Última Atualização**

<p align="center">
  <img src="https://i.postimg.cc/ZY1NYjGs/firefox-Otwz-Bx-YLqy.png">
</p>

Esse item mostra a data e hora da última atualização do dashboard, feita de maneira agendada por um gateway de dados. Ele é composto de um **_cartão_**, com os seguintes dados:

- Campos: [_Medidas] Atualização

**Compras Efetuadas, Valor Investido, Conversão de Compras, Custo por Click e Taxa de Conversão**

<p align="center">
  <img src="https://i.postimg.cc/pdXhcSjr/firefox-l-B0-XYOztvi.png">
</p>


Esse bloco é um conjunto de medidas mais simples que podem ser exibidas em números únicos e compreendidas rapidamente.

Ele é composto de cinco **_cartões_**, com os seguintes dados:

- _Compras Efetuadas_
  - Campos: [_Medidas] Total de Compras
- _Valor Investido_
  - Campos: [_Medidas] Valor Total Investido
- _Conversão de Compras_
  - Campos: [_Medidas] Valor Total de Conversão de Compras
- _Custo por Click_
  - Campos: [_Medidas] Custo por Clique
- _Taxa de Conversão_
  - Campos: [_Medidas] Taxa de Conversão

**Compras por Gênero**

<p align="center">
  <img src="https://i.postimg.cc/JzhxQhvt/PBIDesktop-5gtbr-VJ29i.png">
</p>


Visualização da distribuição de volume de compras na loja por gênero do usuário.

É um **_gráfico de pizza_**, com os seguintes dados:

- Detalhes: [Idade e Gênero] Gênero
- Valores: [Idade e Gênero] Compras (Soma)

**ROAS**

<p align="center">
  <img src="https://i.postimg.cc/tR1PH8MV/firefox-CUs-E9-F2-CKD.png">
</p>


O ROAS foi mostrado nesse dashboard em um componente customizado chamado Tornado Chart, obtido gratuitamente através da loja do Power BI. Os dados nele estão organizados pela idade de forma crescente, e mostram qual gênero e idade deu o maior retorno para a loja comparado ao valor investido na campanha.

É um **_tornado chart_**, com os seguintes dados:

- Grupo: [Idade e Gênero] Gênero
- Legenda: [Idade e Gênero] Idade
- Valores: [_Medidas] ROAS

**Distribuição de Plataformas**

<p align="center">
  <img src="https://i.postimg.cc/43LKD1v5/firefox-lky-RDHwb2-U.png">
</p>


Esse item mostra o alcance da campanha distribuído nas diferentes plataformas em que os anúncios foram vinculados. É interessante observar como o Facebook sozinho possui muito mais da metade dos acessos, o que pode indicar para a loja que ela deve investir ainda mais nele na próxima campanha, pois o público alvo dela se engaja mais por essa rede.

É um conjunto de **_gráfico de rosca_**. Os dados são:

- Legenda: [Dispositivos] Plataforma
- Valores: [Dispositivos] Plataforma (Contagem)

**Jornada de Compra**

<p align="center">
  <img src="https://i.postimg.cc/TYgDKgGd/firefox-bov-HTW8-Mjn.png">
</p>

A jornada de compra mostra o caminho feito pelos clientes até chegarem de fato à compra, e quantos clientes desistem em cada etapa do caminho. Isso pode ajudar a equipe de marketing a ter insights de onde melhorar, e onde aplicar técnicas melhores de engajamento e retenção a fim de garantir mais compras e aumentar a taxa de conversão.

Ele é um **_funil_** com os seguintes dados:

- Valores: [Idade e Gênero] Visualizações por página (Soma), [Idade e Gênero] Adicionados ao carrinho (Soma), [Idade e Gênero] Checkouts iniciados (Soma), [Idade e Gênero] Compras (Soma)

**Ticket Médio por Plataforma**

<p align="center">
  <img src="https://i.postimg.cc/T1WTHVQp/firefox-NWlbh-MFlm-B.png">
</p>

O ticket médio permite visualizar qual plataforma onde os anúncios foram vinculados está gerando o maior retorno por cliente.

Essa visualização é um **_gráfico de barras empilhadas_**, e contém os seguintes dados:

-  Eixos: [Dispositivos] Plataforma do Dispositivo, [Dispositivos] Plataforma
- Valores: [_Medidas] Ticket Médio

**Conversão de Compras por Dia da Campanha**

<p align="center">
  <img src="https://i.postimg.cc/nh19kxCN/firefox-Ccr-Vw-Unj-XV.png">
</p>

<p align="center">
  <img src="https://i.postimg.cc/65Qn5kfn/PBIDesktop-IVCtsv-Xwa8.png">
</p>

Esse gráfico mostra um fato importante, qual foi o período de pico da campanha. Através de um drill-down também é possível ver que as sextas e sábados (representados pelos números 6 e 7, respectivamente) são o dia de maior volume de compras durante a campanha. Com esse dado seria possível a equipe de marketing direcionar a quantidade e frequência de seus anúnicos às sextas e sábados, por exemplo.

Esse é um **_gráfico de área_** com os dados:

- Eixo: [Calendário] Data, [Calendário] Dia da Semana
- Valores: [_Medidas] Valor Total de Conversão de Compras

## Medidas e Fórmulas

### Tabela de Medidas

| Medida                              |                           Fórmula                            |
| ----------------------------------- | :----------------------------------------------------------: |
| Atualização                         |          SELECTEDVALUE('Atualização'[Data e Hora])           |
| Custo por Clique                    | SUM('Idade e Genero'[Quantia gasta (BRL)]) / SUM('Idade e Genero'[Cliques no link]) |
| Maior Ticket Médio                  | VAR maiorValor = MAXX(ALLSELECTED(Dispositivos[Plataforma do dispositivo]), [Ticket Médio]) RETURN SWITCH(TRUE(), [Ticket Médio] = maiorValor, "#E66C37", "#008080") |
| ROAS                                | SUM('Idade e Genero'[Valor de conversão de compras]) / SUM('Idade e Genero'[Quantia gasta (BRL)]) |
| Taxa de Conversão                   | SUM('Idade e Genero'[Compras]) / (SUM('Idade e Genero'[Visualizações por página])) |
| Ticket Médio                        | DIVIDE(SUM(Dispositivos[Quantia gasta (BRL)]), SUM(Dispositivos[Compras])) |
| Total de Compras                    |                SUM('Idade e Genero'[Compras])                |
| Valor Total de Conversão de Compras |     SUM('Idade e Genero'[Valor de conversão de compras])     |
| Valor Total Investido               |          SUM('Idade e Genero'[Quantia gasta (BRL)])          |

## ETL

O processo de ETL foi todo feito através do Power BI, a partir dos 2 arquivos JSON originais (Tabela_dispositivos, Tabela_idade_e_genero) fornecidos para a elaboração dos relatórios.

Foram inclusas duas tabelas, Atualização e Calendario.

O tratamento de dados consistiu em:

- **Dispositivos**

  - Remoção do termo "mobile_" da coluna Plataforma do dispositivo
  - Substituição de todos os valores null por 0
  - Tipo das colunas Alcance, Impressões, Cliques em links, Visualizações por página, Compras no website, Adicionados ao carrinho, Checkouts iniciados e Compras ajustado para Número Inteiro
  - Tipo das colunas Quantia gasta (BRL), Valor de conversão adicionado ao carrinho e Valor de conversão de compras ajustado para Moeda
  - Todas as colunas foram Limpas, Cortadas e tiveram cada palavra colocada em maiúscula

- **Calendario**

  - Foram adicionadas as seguintes colunas à tabela Calendario, com as fórmulas:

    | Coluna        | Fórmula                                                      |
    | ------------- | ------------------------------------------------------------ |
    | Data          | CALENDAR(DATE(2021, 1, 1), DATE(2021, 12, 31))               |
    | Ano           | YEAR(Calendario[Data])                                       |
    | Mês           | MONTH(Calendario[Data])                                      |
    | Dia           | DAY(Calendario[Data])                                        |
    | Semana        | WEEKNUM(Calendario[Data], 1)                                 |
    | Trimestre     | QUARTER(Calendario[Data])                                    |
    | Dia da Semana | WEEKDAY(Calendario[Data])                                    |
    | Nome do Dia   | SWITCH(Calendario[Dia da Semana], 1, "Domingo", 2, "Segunda", 3, "Terça", 4, "Quarta", 5, "Quinta", 6, "Sexta", 7, "Sábado") |

- **Idade e Gênero**

  - Remoção da coluna vazia FIELD4
  - Substiuição dos valores null por 0
  - Tipo das colunas Quantia gasta (BRL), Valor de conversão adicionado ao carrinho e Valor de conversão de compras ajustado para Moeda
  - Todas as colunas foram Limpas, Cortadas e tiveram cada palavra colocada em maiúscula

- **Atualização**

  - Tabela inclusa para mostrar a data de atualização automática do dashboard. Ela contém apenas uma coluna, com a fórmula DAX `DateTimeZone.SwitchZone(DateTimeZone.LocalNow(), -3)`

### Diagrama Relacional

<p align="center">
  <img src="https://i.postimg.cc/cLDgPy19/PBIDesktop-Jn-IG1z-Y7v-K.png">
</p>


## Melhorias e Aprendizados

### O Que Aprendi

- Criação e utilização da tabela Calendario para controlar o uso de datas associadas no dashboard
- Atualização automática agendada através de gateway de dados
- Conceitos de marketing digital e métricas utilizadas na área, e como elas podem ser usadas pelas equipes para direcionar esforços e investimentos

### O Que Preciso Melhorar e Aprender

- Utilização de cores no dashboard
- Novas ferramentas de ETL como Google Colab

## Referências

[O Que é, Como Calcular e a Diferença do ROI](https://neilpatel.com/br/blog/roas-o-que-e/)

[Taxa de conversão: o que é e como calcular?](https://resultadosdigitais.com.br/blog/o-que-taxa-de-conversao/)

[Ticket médio: por que esse indicador é tão importante para sua empresa?](https://www.organicadigital.com/blog/ticket-medio-por-que-esse-indicador-e-tao-importante/)

<div>Ícones feitos por <a href="https://www.freepik.com" title="Freepik">Freepik</a> e obtidos de <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div>

