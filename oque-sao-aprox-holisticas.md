# Aproximações Holísticas ( Holistic Approach)👦

****
Nome: Gustavo Costa

Curso: Ciências da Computação

Artigo Científico de Referência:  *Face Recognition Systems: A Survey; Yassin Kortli, Maher Jridi, Ayman Al Falou e Mohamed Atri*

****

Aproximações Holísticas ou Subespaciais costumam trabalhar com a face inteira, isso quer dizer que não é necessário extrair regiões da face ou pontos característicos (olhos, boca, nariz, etc). A principal função dessas aproximações é **representar
a imagem facial por meio de uma matriz de pixels e, em alguns momentos, essa matriz é convertida em vetores de características para facilitar o seu tratamento.** Logo após isso, esses vetores de características são implementados em um espaço
dimensional limitado.

É importante informar que, essas aproximações são **sensíveis à variações, por exemplo: expressões faciais diferentes, iluminação e poses.** Pelo fato de isso ocorrer nessas aproximações, elas são utilizadas largamente. Ademais, elas também são
divididas em categorias baseado no método utilizado para representar o subespaço:

### 1- Técnicas Lineares: 
  - *Eigenfaces (PCA):* Principal Component Analysis, usado para reduzir a dimensionalidade.
  - *Fisherfaces (LDA):* Linear Discriminant Analysis, foca na separação entre classes.
  - *ICA:* Independent Component Analysis, separa um conjunto de sinais misturados em componentes independentes.
  - *Gabor Filters:* Usado para análise de textura e frequência.
  - *Análise de Domínio da Frequência, DWT (Discrete Wavelet Transform), DCT (Discrete Cosine Transform):* Transformações usadas para análise de frequência e compressão de imagem.
 
### 2- Técnicas não Lineares:
  - *KPCA (Kernel PCA):* Extensão não linear do PCA.
  - *KDA (Kernel Discriminant Analysis):* Versão não linear do LDA.
  - *Gabor-KLDA:* Combinação de Gabor Filters com KDA.
  - *EWPCA, KMAMC, WT (Wavelet Transform), RT (Ridgelet Transform):* Variadas técnicas para análise de textura e padrões complexos.
  - *CNNs (Convolutional Neural Networks):* Redes neurais profundas especializadas em processamento de imagens.
  - *SVMs (Support Vector Machines), KFD (Kernel Fisher Discriminant), KPCA (Kernel PCA), LLE (Locally Linear Embedding), KDCV (Kernel Direct Covariance):* Métodos diversos para classificação, redução de dimensionalidade e aprendizado de
  características.
