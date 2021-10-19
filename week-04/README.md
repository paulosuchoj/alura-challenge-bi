# Semana 04 - Curriculum

## Dashboard

O dashboard criado como curriculum pode ser acessado na web, através do seguinte link:

**[Dashboard Curriculum - Alura Challenge BI - Semana 04](https://app.powerbi.com/view?r=eyJrIjoiM2M4NjEwOTMtM2EyMC00ZjQ4LTk3N2ItZGI3OWZlMzkyZTNiIiwidCI6IjJjNzUwYmUyLTVkYzAtNDRjNy04MzNjLTA5NGY4ZGE5NzljMyJ9&pageName=ReportSection)**

## Caso

Essa era a última tarefa do Challenge BI da Alura, a criação de um curriculum e portfólio, contendo os trabalhos que foram feitos durante as 4 semanas de desafio e nossos canais de contato. A criação do dashboard era livre, de acordo com o gosto e imaginação de cada desenvolvedor.


## Páginas

Esse dashboard possui apenas uma página principal, denominada Curriculum.

**Obs.:** Os dados acerca de cada elemento das páginas estará disposto da seguinte maneira abaixo:

- Propriedade: [Tabela de Origem] Dado (Cálculo)

### Curriculum

<p align="center">
    <img src="https://i.postimg.cc/YqB2JxTv/msedge-GTy-Ov-Hg1gj.png"/>
</p>

Concentra todas as informações relevantes sobre mim, meus conhecimentos, experiência e trabalhos feitos. Consiste de um cabeçalho, botões de navegação e componentes flutuantes de árvore de habilidades, linha temporal de experiências, portfólio, idiomas e cartão de contato.

**Cabeçalho**

<p align="center">
  <img src="https://i.postimg.cc/CLsKq24x/firefox-g-KKdr-Viojb.png">
</p>

Conjunto de uma **imagem** com foto de perfil, uma **caixa de texto** com mensagem de boas-vindas e apresentação, e uma **imagem** com link para envio de e-mails.

**Botões de Navegação**

<p align="center">
  <img src="https://i.postimg.cc/ryrFnHZ6/msedge-t-Gkio-Cwsa-N.png">
</p>

Conjunto de 5 **botões** para navegação entre os itens do curriculum. Cada um deles exibe seu respectivo item e esconde o que estava aberto, através do uso de Seleções e Indicadores.

**Habilidades**

<p align="center">
  <img src="https://i.postimg.cc/Jz2bVSJh/firefox-ONUV6-QSvod.png">
</p>

Essa item exibe minhas habilidades, classificadas em Básico, Intermediário e Avançado. Ele é uma **árvore hierárquica** e contém os seguintes dados:

- Analisar: [Habilidades] Nível
- Explicar por: [Habilidades] Nível, [Habilidades] Habilidade

**Experiências**

<p align="center">
  <img src="https://i.postimg.cc/sD3PpYs3/firefox-d-Pc-U9iq-Mye.png">
</p>


Esse item mostra minha carreira em termos de empresas, cargos e atividades numa linha temporal. Ele é um **gráfico de Gantt** (obtido da loja do Power BI, com o nome de Gantt Chart By MAQ Software), com as seguintes configurações:

- Category: [Experiencia] Empresa
- Start: [Experiencia] Data Inicio
- End: [Experiencia] Data Fim
- Tooltip: [Experiencia] Cargo, [Experiencia] Atividades

**Portfólio**

<p align="center">
  <img src="https://i.postimg.cc/ydqcW9L4/firefox-Bn2-S6-Hv-TJH.png">
</p>


Galeria com os projetos finalizados durante o Challenge BI. É um conjunto de **imagens** e **caixas de texto** com os links necessários das screenshots e o título de cada uma, e a Ação de cada um é levar para o respectivo dashboard publicado na web.

**Idiomas**

<p align="center">
  <img src="https://i.postimg.cc/MGf1Wtbm/firefox-YH1sw5-NBM1.png">
</p>

**Tabela** simples com uma listagem de idiomas e nível. Possui as seguintes configurações:

- Valores: [Idiomas] Link Bandeira, [Idiomas] Idioma, [Idiomas] Nível, [Idiomas] Nível Numérico

**Contato**

<p align="center">
    <img src="https://i.postimg.cc/9QMGkcDS/firefox-MBXmx-B6lu0.png" />
</p>


Outro item simples, é apenas uma **caixa de texto** com mensagem, e duas **imagens** que levam, respectivamente, ao meu LinkedIn e GitHub.

- Campo: [Pedidos] Data da Compra (Ano)

## ETL

Os dados desse dashboard foram carregados à partir da Web, pois estão armazenados em uma planilha no Google Sheets.

O processo de tratamento para todas as três tabelas foi o mesmo:

- Remover a coluna de índice
- Remover linhas em branco
- Promover a primeira linha para cabeçalhos

### Diagrama Relacional

<p align="center">
  <img src="https://i.postimg.cc/J4Lnt8ZF/PBIDesktop-p-Uf-YESy-Uu-H.png">
</p>

## Referências

<div>Os ícones foram providenciados por <a href="https://www.flaticon.com/authors/pixel-perfect" title="Pixel perfect">Pixel perfect</a> do site <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div>

