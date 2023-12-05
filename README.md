# Detecção de anomalias na inspeção estrutural de pontes
## Comparativo entre YOLOv8 e Detectron2

Alunos (Grupo 46):
* Nathalia Castelo Branco (nathaliaacbranco@gmail.com)
* Rafael Cabral (rafi.cabral@gmail.com)

Data da apresentação: 29/11/2023

## Resumo do trabalho

A inspeção visual desempenha um papel crucial na avaliação do estado de conservação de pontes e viadutos, sendo essencial para planos de manutenção, recuperação e reforço. A degradação inevitável das estruturas torna relevante a adoção de avaliações, transcendendo o diagnóstico e mitigando a subjetividade por meio da visão computacional. 

O banco de dados dacl10k, composto por 9.920 imagens de inspeções reais, categoriza 12 classes de danos e 6 componentes de pontes. Este estudo foca em danos comuns, resultando em 2.676 imagens de armaduras expostas e fissuras, destacando 2.000 instâncias de armaduras expostas e 3.626 de fissuras. 

A metodologia emprega redes neurais convolucionais para segmentação, utilizando modelos de estágio único (YOLOv8) e duplo (Detectron2) com transferência de aprendizagem do conjunto COCO. O subconjunto de dados é dividido em 80% para treino e 20% para validação. Técnicas de aumento, como brilho, contraste, saturação e espelhamento, são aplicadas, juntamente com hiperparâmetros específicos. 

Os resultados destacam o desempenho do YOLOv8, com 35.42% e 12.63% para mAP@50 e mAP@50:95, enquanto o Detectron2 alcança 36.64% e 13.61%. Em relação à taxa de quadros por segundo (FPS), o YOLOv8 atinge 20FPS, superando o Detectron2 com uma média de 15FPS. 

Ambos os modelos apresentam métricas semelhantes quando padronizados com os mesmos hiperparâmetros e técnicas de otimização. Entretanto, na análise qualitativa das inferências, a YoloV8 apresentou-se mais robusta. A sensibilidade dos hiperparâmetros do Detectron2 foi avaliada, sem observar melhorias significativas. Para trabalhos futuros, planeja-se uma filtragem manual do subconjunto de imagens para selecionar dados mais confiáveis dentro da perspectiva do domínio de aplicação. 

## Dataset

O dataset utilizado neste trabalho chama-se dacl10k, que significa "Damage Classification 10k images". Abaixo alguns exemplos de segmentação de danos do dataset.

![Exemplos de classificação de danos](https://github.com/phiyodr/dacl10k-toolkit/blob/master/assets/Examples.jpg?raw=true)

Este dataset pode ser encontrado no [seguinte link](https://github.com/phiyodr/dacl10k-toolkit).

## Apresentação do trabalho

Este trabalho possui um [vídeo de apresentação publicado no Youtube](https://youtu.be/GbWjok4fCmA). Assista clicando na imagem abaixo:

[![Assista ao vídeo](https://img.youtube.com/vi/GbWjok4fCmA/maxresdefault.jpg)](https://youtu.be/GbWjok4fCmA)

## Poster do trabalho

![Poster do trabalho](https://drive.google.com/file/d/1F7zizRwx27fFU6915YsWIXbVYoWqdz-s/view?usp=sharing)
