# 🛰️ AgroVision — Inteligência Geoespacial e Sensoriamento Remoto

## 📝 Descrição do Projeto
O AgroVision é uma solução de agricultura de precisão desenvolvida para mitigar perdas agrícolas e otimizar o manejo hídrico através do monitoramento orbital agnóstico. A plataforma ingere dados multiespectrais de múltiplas constelações de satélites e transforma pixels brutos em métricas preditivas de saúde vegetal, permitindo ações preventivas antes do dano foliar visível ao olho humano.

## ❌ O Problema de Negócio
* **Desafio da Escala:** Monitoramento ineficiente e de alto custo operacional para grandes extensões de terra utilizando métodos tradicionais (inspeção visual a pé ou drones de baixa autonomia).
* **Tempo de Reação Lento:** Quando o olho humano detecta o amarelamento de uma folha em campo, o colapso celular já ocorreu dias antes. A perda de safra torna-se inevitável.
* **Desperdício Hídrico:** Irrigação baseada em intuição ou calendários fixos, gerando desperdício de água e lixiviação de nutrientes do solo.

## ⚙️ Pipeline Técnico e Arquitetura de Dados
1. **Ingestão (Data Ingestion):** Consumo automatizado de imagens multiespectrais via APIs orbitais (Copernicus/Sentinel para histórico, Planet Labs para frequência diária e Maxar para alta resolução sob demanda).
2. **Processamento Matricial (Raster Processing):** Utilização da biblioteca GDAL para leitura, recorte, projeção e tratamento de arquivos georreferenciados (`.tif` / GeoTIFF).
3. **Engenharia de Atributos (Feature Engineering):** Extração de features matemáticas pixel a pixel através do cálculo do Índice de Vegetação por Diferença Normalizada ($NDVI$), baseado na física de reflectância do Infravermelho Próximo ($NIR$) e do Canal Vermelho ($Red$).
   $$NDVI = \frac{NIR - Red}{NIR + Red}$$
4. **Visão Computacional & IA:** Aplicação de modelos de segmentação profunda (YOLO / Mask R-CNN) para isolar talhões, classificar zonas de estresse hídrico e gerar mapas de calor automatizados.
5. **Consumo do Dado (Serving):** Disponibilização de um dashboard interativo focado em usabilidade e relatórios simplificados para tomada de decisão em campo.

## 🛠️ Stack Tecnológica
* **Linguagem Principal:** Python
* **Processamento Geoespacial:** GDAL, QGIS
* **Visão Computacional & ML:** OpenCV, Scikit-Learn, YOLO / Mask R-CNN
* **Interface & Visualização:** Streamlit / Power BI

---

## 🖼️ Apresentação e Documentação do Projeto
Para acompanhar o design conceitual, telas e pitch desenvolvidos no Canva para a Global Solution, utilize os acessos abaixo:

* 📁 [Baixar Apresentação Completa em PDF](file:///C:/Users/nasci/Downloads/Agro_Vision.pptx.pdf)
* 🔗 [Visualizar Apresentação Interativa no Canva](https://www.canva.com/design/DAHLqParA4k/3UHAriAKTfDecJsaL4FY-w/edit)
