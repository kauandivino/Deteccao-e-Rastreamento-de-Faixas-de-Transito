# INF0417 - Visão Computacional

Team 5:

INF0417 – 202105852 – KAUAN DIVINO POUSO MARIANO (leader)

INF0417 – 202004672 – FERNANDA DE CASTRO FERNANDES

INF0417 – 202105853 – LUAN GABRIEL SILVA OLIVEIRA

INF0417 – 202108784 – MATHEUS ANDRADE BRANDAO

INF0417 - 202105857 - LYAN EDUARDO SAKUNO RODRIGUES

---

# Detecção e Rastreamento de Faixas de Trânsito

Este projeto foi desenvolvido como parte da disciplina de Visão Computacional do curso de Bacharelado em Inteligência Artificial. Ele apresenta uma solução eficiente e de baixo custo computacional para detecção e rastreamento de faixas em vídeos utilizando técnicas tradicionais de visão computacional.

Um artigo detalhando este projeto foi publicado e pode ser acessado pelo link: [Lane Detection System for Driver Assistance in Vehicles](https://arxiv.org/abs/2410.04046).

![Exemplo de Detecção de Faixas](/imagem_exemplo.jpeg)  
*Figura 1: Exemplo de detecção de faixas em uma estrada.*

## Objetivo
O objetivo principal deste projeto é desenvolver um sistema que detecta e rastreia faixas de trânsito em tempo real, mesmo em condições adversas, como desgaste de faixas, iluminação variável e mudanças climáticas. A abordagem foca em técnicas tradicionais de visão computacional para atender a dispositivos com recursos limitados.

## Requisitos
Certifique-se de ter os seguintes pré-requisitos instalados:
- Python 3.x
- NumPy
- Matplotlib
- OpenCV 3.x
- Pickle
- MoviePy

## Instalação das Dependências
Para instalar as dependências, utilize o comando abaixo:

`pip install -r requirements.txt`

## Estrutura do Projeto

- `Calibração_Camera/`: Pasta contendo imagens de tabuleiro de xadrez para calibração da câmera.
- `imagens_testes/`: Imagens de teste.
- `Relatório Técnico/`: Relatórios Técnicos e Artigo.
-  `video_teste`: Vídeo de teste padrão.
- `video_teste_output`: Vídeo de teste padrão com detecção de faixa.
- `lane_tracker.ipynb`: Notebook Jupyter com a implementação e explicação detalhada do pipeline.

## Como Usar

1. Calibração da Câmera:

* Execute a seção 1 do notebook `lane_tracker.ipynb` para calibrar a câmera utilizando as imagens na pasta `Calibracao_Camera/`.

2. Configuração do Pipeline:

* Compile todas as células do notebook para configurar o pipeline de processamento.

3. Processamento de Vídeos:

* Insira o caminho do vídeo que deseja processar e execute a célula correspondente para gerar a saída com a detecção de faixas.


## Metodologia

O pipeline do sistema consiste nas seguintes etapas:

1. **Calibração da Câmera:** Eliminação de distorções utilizando imagens de tabuleiro de xadrez.

2. **Transformação de Perspectiva:** Conversão da vista frontal para uma vista "de cima" (bird’s-eye view).
Segmentação de Imagem: Aplicação de thresholds em diferentes canais de cor (RGB, HLS, LAB) para destacar as faixas.

3. **Detecção de Faixas:** Utilização do método de janelas deslizantes para identificar as faixas e ajustá-las a um modelo polinomial de segunda ordem.

4. **Visualização dos Resultados:** Projeção das faixas detectadas sobre a imagem original e exibição de métricas como curvatura da estrada e posição relativa do veículo.

## Resultados

### Desempenho do Algoritmo

* **Precisão:** 92% em condições de iluminação diurna e 85% em cenários noturnos ou de baixa visibilidade.
* **Taxa de Erro Médio:** Inferior a 10%.
* **Taxa de Processamento:** 24 frames por segundo em vídeos de resolução HD.

### Limitações Observadas

* Desafios em cenários com:
- Marcas de faixas muito desgastadas.
- Condições climáticas extremas (nevoeiro ou reflexos intensos).
- Curvas acentuadas.

Apesar das limitações, o sistema demonstra potencial para aplicações em sistemas avançados de assistência ao motorista (ADAS) e veículos autônomos.

## Publicação

Este projeto foi detalhado no artigo: [Lane Detection System for Driver Assistance in Vehicles](https://arxiv.org/abs/2410.04046).
