# Eigenface e Principal Component Analysis (PCA)

****
Nome: Gustavo Costa

Curso: Ciências da Computação

Artigo Científico de Referência: Face Recognition Systems: A Survey; Yassin Kortli, Maher Jridi, Ayman Al Falou e Mohamed Atri

****

Eigenfaces é um dos mais populares métodos de aproximações holísticas usadas para extrair pontos característicos da imagem facial. Essa aproximação é baseada na técnica estatística de Análise de Componentes Principais (PCA), que consiste em
transformar o número de possíveis variáveis correlatas em um número pequeno de variáveis incorretas chamadas de *componentes principais*.

## Funcionamento 🔢

Há algumas informações primordiais que sempre precisam estar na memória, principalmente para o entendimento facilitado do Eigenface:

- Toda imagem consiste em uma matriz NxM, cujo cada posição (i,j), i sendo linhas e j sendo colunas, corresponde à um *pixel*.

- Toda imagem, nem sempre carrega 100% de informações úteis para o reconhecimento facial e dado isso, muitas vezes pode ser *custoso* trabalhar com informações desnecessárias em grandes sistemas.

- Considere um conjunto de imagens do set de treinamento **{X1, X2, X3, ..., Xn}**.

- A média facial do set é definido pela seguinte fórmula:

  <img src="https://i.ibb.co/K5F3QS4/Captura-de-tela-2024-01-12-201659.png">

  * **μ** representa a média facial.
  * **n** representa a quantidade de imagens do set.

- Para estimar a matriz de covariância que representa o grau de dispersão de todos os vetores de características em relação ao vetor médio. A matriz de covariância Q é definida
da seguinte maneira:

  <img src="https://i.ibb.co/9NkRMcq/Captura-de-tela-2024-01-12-203339.png">

  * **Q** representa a matriz de covariância.
  * **μ** representa a média facial.
  * **(Xi−μ)** é o vetor da diferença entre a observação Xi e a média μ.
  * **(Xi−μ)^T** é o transposto deste vetor de diferença.

