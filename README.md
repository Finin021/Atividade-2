# Sistemas Evolutivos e Aplicados à Robótica — DeepFace

## Sobre o Projeto

Este projeto apresenta um estudo utilizando a biblioteca **DeepFace**, com foco em tarefas de **análise facial** utilizando técnicas de **Visão Computacional** e **Inteligência Artificial**.

O objetivo principal é analisar a capacidade do modelo em identificar automaticamente diferentes características faciais presentes em uma imagem, considerando os seguintes fatores:

* Identificação de emoções
* Estimativa de idade
* Classificação de gênero
* Detecção facial
* Extração de características faciais

---

## Tecnologias Utilizadas

As seguintes tecnologias foram utilizadas durante o desenvolvimento do projeto:

* Python
* DeepFace
* OpenCV
* NumPy
* Google Colab
* Visão Computacional
* Inteligência Artificial

---

## Recursos Utilizados

Os seguintes recursos disponibilizados pela biblioteca DeepFace foram utilizados durante os experimentos:

| Recurso          | Função                         |
| ---------------- | ------------------------------ |
| Emotion          | Identificação de emoções       |
| Age              | Estimativa de idade            |
| Gender           | Classificação de gênero        |
| Face Detection   | Detecção facial                |
| Region Detection | Localização do rosto na imagem |

---

## Metodologia

Os experimentos foram realizados seguindo as seguintes etapas:

1. Instalação automática da biblioteca DeepFace;
2. Carregamento da imagem de teste;
3. Detecção facial automática;
4. Extração das características faciais;
5. Análise dos resultados obtidos.

Foi utilizada uma imagem contendo um rosto humano para realização dos testes, permitindo ao modelo identificar diferentes características presentes na imagem.

---

## Características Detectadas

Durante a análise, foram identificadas as seguintes informações:

* Emoções
* Idade estimada
* Gênero
* Região facial
* Classificações faciais adicionais

---

## Resultados Obtidos

### Emoções detectadas

| Emoção   |  Resultado |
| -------- | ---------: |
| Zangado  |  0.000089% |
| Nojo     | 0.0000006% |
| Medo     |    0.0060% |
| Feliz    |  91.01343% |
| Triste   |   0.00762% |
| Surpreso |   0.03711% |
| Neutro   |    8.9357% |

**Emoção dominante:** Feliz

---

### Região Facial Detectada

| Propriedade      | Valor |
| ---------------- | ----: |
| x                |   610 |
| y                |   890 |
| largura          |   657 |
| altura           |   657 |
| Confiança Facial |  0.95 |

---

### Idade e Gênero

| Característica | Resultado |
| -------------- | --------: |
| Idade estimada |   23 anos |
| Mulher         |   0.0267% |
| Homem          | 99.97329% |

**Gênero dominante:** Homem

---

### Características Classificadas pelo Modelo

| Classificação    | Resultado |
| ---------------- | --------: |
| Asiático         |  0.59814% |
| Indiano          | 14.55353% |
| Negro            |  0.17101% |
| Branco           | 10.34127% |
| Oriente Médio    | 44.51679% |
| Latino/Hispânico | 29.81923% |

**Classificação predominante:** Oriente Médio

---

## Conclusão

Os resultados obtidos demonstram que a biblioteca **DeepFace** apresentou capacidade para identificar automaticamente diferentes características faciais utilizando apenas uma imagem como entrada. O sistema foi capaz de realizar múltiplas análises simultaneamente, incluindo identificação de emoções, estimativa de idade, classificação de gênero e extração de características faciais.

Os experimentos também demonstraram a aplicação prática de técnicas de visão computacional e inteligência artificial em tarefas relacionadas à análise facial automatizada.

---

## Código disponível em:

```bash
!pip install deepface

from google.colab import files

uploaded = files.upload()

import cv2
from deepface import DeepFace
from google.colab.patches import cv2_imshow

filename = list(uploaded.keys())[0]

img = cv2.imread(filename)

result = DeepFace.analyze(
    img,
    enforce_detection=False
)

print(result)

cv2_imshow(img)
```

---

## Referências

* DeepFace Documentation
* OpenCV Documentation
* Python Documentation
