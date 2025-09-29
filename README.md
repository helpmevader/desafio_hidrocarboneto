# 🧭 Desafio Técnico: Mapa Interativo de Poluentes

## 1. Objetivo

Este projeto foi desenvolvido como solução para o Desafio Técnico IHC – Especialista em Python e Geoprocessamento (GIS). O objetivo principal é gerar um **mapa interativo e offline (`mapa.html`)** a partir de um conjunto de dados ambientais, visualizando a concentração de dois poluentes distintos.

## 2. Funcionalidades Implementadas

#### Funcionalidades Essenciais:
- **Camada de Barras de Concentração**: Cada estação de monitoramento é representada por ícones de barras verticais, cuja altura é proporcional à concentração do poluente.
- **Tooltips Informativos**: Ao passar o mouse sobre as barras, são exibidas informações detalhadas da estação, incluindo nome, data da coleta e valor da medição.
- **Camada de Mapa de Calor (Heatmap)**: Visualização da distribuição geográfica da concentração dos poluentes.

#### Funcionalidades Bônus:
- ✨ **Interface com Barra Lateral**: Uma barra lateral à direita, que pode ser expandida ou minimizada, concentra todas as interações do usuário.
- ✨ **Controle de Camadas Granular**: Dentro da barra lateral, o usuário pode ligar ou desligar individualmente as camadas de **Barras (Poluente A e B)** e **Mapa de Calor (Poluente A e B)**.
- ✨ **Múltiplos Mapas Base**: É possível alternar entre uma visualização "Clean" (para foco nos dados) e "Imagem de Satélite" (para contexto geográfico).
- ✨ **Legenda Fixa**: Uma legenda sempre visível no canto inferior direito explica as cores das barras e a escala do heatmap.
- ✨ **Barra de Escala**: Uma escala cartográfica foi adicionada ao canto inferior esquerdo.
- ✨ **Exportação em GeoJSON**: Um botão na barra lateral permite o download dos dados das estações em formato `.geojson`, cumprindo um dos requisitos bônus.

## 3. Como Executar o Projeto

**Pré-requisitos:**
- Python 3.8+

**Instruções:**
1.  Clone ou faça o download deste repositório.
2.  Navegue até a pasta raiz do projeto pelo terminal.
3.  Instale as dependências necessárias:
    ```bash
    pip install -r requirements.txt
    ```
4.  Execute o script principal:
    ```bash
    python src/map.py
    ```
5.  Após a execução, o arquivo final estará disponível em `maps/mapa.html`. Abra este arquivo em qualquer navegador web.

## 4. Estrutura de Arquivos

O projeto segue a estrutura de pastas solicitada:
```
.
├── data/
│   └── dados_exemplo_poluentes_no_acentos.csv
├── maps/
│   └── mapa.html
├── src/
│   └── map.py
├── requirements.txt
└── README.md
```

## 5. Tecnologias Utilizadas
- **Python**: Linguagem principal para o processamento dos dados.
- **Pandas**: Para manipulação e limpeza dos dados tabulares.
- **GeoPandas**: Para a estruturação dos dados geográficos e exportação em GeoJSON.
- **Folium**: Biblioteca principal para a criação dos mapas interativos.
- **HTML/CSS/JavaScript**: Injetados via Folium para criar a interface customizada.