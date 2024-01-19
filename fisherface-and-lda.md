# Fisherface & Linear Discriminant Analysis (LDA) 🐟

****
Nome: Gustavo Costa

Curso: Ciências da Computação

Artigo Científico de Referência: Face Recognition Systems: A Survey; Yassin Kortli, Maher Jridi, Ayman Al Falou e Mohamed Atri

****

O método Fisherface é baseado no mesmo princípio de similaridade em relação ao método Eigenface. O objetivo desse método é reduzir a alta dimensionalidade da imagem por meio do uso da técnica LDA ao invés de utilizar PCA (Principal Component 
Analysis). A técnica LDA é comumente usado para redução de dimensionalidade e reconhecimento facial, a técnica PCA é **não é supervisionada** enquanto a técnica LDA **é uma técnica de aprendizagem e é supervisionada**, além disso, ela também
utiliza as informações contidas nos dados.

O Fisherface tem como objetivo **separar classes e maximizar essa diferença entre elas**, para o nosso contexto: reconhecimentos faciais, considere como classe um indivíduo. Logo, o objetivo é maximizar a diferença entre indivíduos e, também
**minimizar a diferença dentro de cada classe**. Então resumindo: a ideia por trás dessa técnica é: **distanciar o máximo possível uma pessoa da outra e, ao mesmo tempo, aproximar/igualar fotos/imagens da mesma pessoa**. Essas maximizações e
minimizações são feitas por meio da análise das matrizes de dispersão (scatter matrices) entres as classes e dentro das classes, denominadas como: 
  
  - **Sb** é a matriz de dispersão entre classes
  - **Sw** é a matriz de dispersão dentro da classe

## Matriz de Dispersão Dentro da Classe (Sw)
A matriz de dispersão dentro da classe, Sw, representa a dispersão das amostras em torno da média de sua própria classe. Sua fórmula é:

  <img src="https://i.ibb.co/SQfHj1y/Captura-de-tela-2024-01-18-221823.png">

  Onde:
    
  - **c** é o número de classes (no nosso contexto, mais uma vez, pense como diferentes pessoas)
  - **Xi** é o conjunto de amostras na i-ésima classe.
  - **x** é uma amostra individual.
  - **μi** é a média das amostras na i-ésima classe.
  - **(x - μi)** é o vetor de diferença entre a amostra x e a média da classe μi.

## Matriz de Dispersão Entre Classes (Sb)
A matriz de dispersão entre classes Sb representa a dispersão das médias de cada classe em torno da média geral de todas as classes. Sua fórmula é:

  <img src="https://i.ibb.co/fd2cxhZ/Captura-de-tela-2024-01-18-222323.png">

  Onde:

  - **Ni** é o número de amostras na i-ésima classe.
  - **μi** é a média das amostras na i-ésima classe.
  - **μ** é a média geral de todas as amostras.
  - **(μi - μ)** é o vetor de diferença entre a média da classe μi e a média geral μ.

## Objetivo do Fisherface 🎯
O objetivo é encontrar um conjunto de vetores que maximizem a razão do determinante de Sb para o determinante de Sw. Matematicamente, isso envolve encontrar os *vetores* que maximizam a seguinte função:

<img src="https://i.ibb.co/LN6xbDC/Captura-de-tela-2024-01-18-223439.png">

Onde **W** é a matriz dos vetores discriminantes.

## Aplicações utilizando Fisherface no contexto de Reconhecimento Facial

- **Maximização da Separabilidade:** Ao maximizar a separabilidade entre diferentes classes (diferentes faces) e minimizar a variação dentro de cada classe, o Fisherface se torna eficaz em reconhecer faces mesmo sob variações de
iluminação e expressão facial.

- **Redução de Dimensionalidade:** Assim como o PCA, o LDA também serve para reduzir a dimensionalidade dos dados, mas com um foco mais direcionado à maximização da separabilidade entre as classes.

****


<img src="https://i.ibb.co/BB0xqGv/fisherface.png">

*fonte da imagem: https://blog.csdn.net/kuweicai/article/details/79330524*
