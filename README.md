# INF0417 - Visão Computacional

Team 5:

INF0417 – 202105852 – KAUAN DIVINO POUSO MARIANO (leader)

INF0417 – 202004672 – FERNANDA DE CASTRO FERNANDES

INF0417 – 202105853 – LUAN GABRIEL SILVA OLIVEIRA

INF0417 – 202108784 – MATHEUS ANDRADE BRANDAO

INF0417 - 202105857 - LYAN EDUARDO SAKUNO RODRIGUES

---

# Detecção e Rastreamento de Faixas de Trânsito

Este projeto tem como objetivo desenvolver um algoritmo robusto para detectar e rastrear os limites das faixas em um vídeo utilizando técnicas tradicionais de visão computacional.

![Exemplo de Detecção de Faixas](./readme_images/example_image.jpg)  
*Figura 1: Exemplo de detecção de faixas em uma estrada.*

## Requisitos

- Python 3.x
- NumPy
- Matplotlib
- OpenCV 3.x
- Pickle
- MoviePy

## Estrutura do Projeto

- `lane_tracker.ipynb`: Notebook Jupyter com a implementação e explicação detalhada do pipeline.
- `Calibração_Camera/`: Pasta contendo imagens de tabuleiro de xadrez para calibração da câmera.
- `imagens_testes/`: Imagens de teste.
-  `video_teste`: Vídeo de teste padrão.
- `video_teste_output`: Vídeo de teste padrão com detecção de faixa.

## Como Usar

1. Execute a seção 1 do notebook `lane_tracker.ipynb` para realizar a calibração da câmera.
2. Compile todas as células do notebook para configurar o pipeline.
3. Insira o caminho do vídeo que deseja processar e execute a célula correspondente.

## Metodologia

O pipeline é composto por várias etapas, incluindo calibração da câmera, correção de distorção, transformação de perspectiva, thresholding para geração de imagem binária, detecção de faixas e visualização dos resultados.

## Resultados

O algoritmo foi testado em diversos cenários e demonstrou ser capaz de detectar e rastrear faixas com precisão, mesmo em condições variáveis de iluminação e superfície da estrada.
