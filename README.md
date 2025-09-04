## Visão Geral do Projeto

Este projeto é uma jornada pessoal no mundo da **visão computacional**, com o objetivo de consolidar meus estudos e aplicar conceitos em uma área que gosto. O projeto `Contador de repetições` foi desenvolvido para atuar como um contador de repetições de exercícios, como o **bíceps curl (rosca direta)**, usando a webcam e o poder das bibliotecas **MediaPipe** e **OpenCV**.

O principal objetivo é demonstrar a capacidade de rastrear e analisar movimentos do corpo humano em tempo real, calculando ângulos de articulações e, com base neles, criar uma lógica para contar as repetições de forma precisa.

## Tecnologias Utilizadas

* **Python**: Linguagem de programação principal.
* **MediaPipe**: Uma solução de machine learning do Google que detecta pontos-chave (landmarks) do corpo humano, como ombros, cotovelos e pulsos.
* **OpenCV**: Biblioteca de visão computacional usada para capturar e processar o vídeo da webcam.
* **Numpy**: Essencial para realizar operações matemáticas eficientes, como o cálculo do ângulo entre os vetores das articulações.

## Funcionalidades

O script principal realiza as seguintes etapas:

1.  **Captura de Vídeo**: Inicia a captura de vídeo da sua webcam.
2.  **Detecção de Pose**: Utiliza o modelo **`mp_pose`** do MediaPipe para detectar os `landmarks` do corpo em cada quadro do vídeo.
3.  **Processamento de Imagem**: Converte o formato de cor da imagem de BGR para RGB para que o MediaPipe possa processá-la e depois a reverte de RGB para BGR para exibição com o OpenCV.
4.  **Extração de Coordenadas**: Extrai as coordenadas `(x, y, z)` de cada `landmark` detectado, permitindo o cálculo do ângulo entre as articulações.
