# Análise de Dados do Dark Energy Survey (DES)

## Resumo
Este mini-projeto utiliza dados públicos do Dark Energy Survey (DES) DR2 para explorar uma região específica do céu definida por restrições de Ascensão Reta (RA) e Declinação (Dec). Foram realizados uma análise exploratória dos objetos presentes, a geração de diagrama cor-magnitude e gráfico de distribuição de objetos, com foco em compreender populações de estrelas na região selecionada.

## 1 Escolha do Objeto
A escolha da região do céu para a análise foi baseada nas restrições de Ascensão Reta (RA) e Declinação (Dec) especificadas: RA entre 0° e 60° e Dec entre -30° e -60°, conforme exigido pelo programa do LIneA.  
A região foi selecionada para cobrir uma área significativa do céu observada pelo DES DR2, utilizando coordenadas de Ascensão Reta e Declinação para coletar dados dessa área.

### 1.2 Uma Observação
Acesso ao banco de dados do DES  se realiza através da infraestrutura do LIneA utilizando a biblioteca "dblinea". A biblioteca funciona apenas dentro da infraestrutura do LIneA.

## 2 Escolha da Região do Céu para Análise
Para a análise dos dados do Dark Energy Survey (DES), foi selecionada uma região específica do céu com base nas coordenadas de Ascensão Reta e Declinação.  
A área escolhida foi definida utilizando uma consulta ao banco de dados do DES, onde os objetos foram selecionados em torno de uma coordenada central específica, com um raio de 0,5°.

### 2.1 Detalhes da Região
A região do céu foi definida com as seguintes limitações:
- Ascensão Reta (RA): A região abrange objetos localizados entre 14h45m e 15h15m (±0,5° ao redor da RA central de 15h).
- Declinação (Dec): A região abrange objetos localizados entre -34.7° e -33.7° (±0,5° ao redor da Dec central de -34.2°).

Essa escolha garante uma área suficientemente grande para análise e uma quantidade significativa de dados astronômicos disponíveis.

### 2.2 Justificativa para a Escolha do Raio
O raio de 0,5 foi escolhido para capturar uma boa quantidade de objetos celestes na região sem expandir excessivamente a área analisada, mantendo os dados bem definidos.

## 3 Coleta de Dados
A coleta de dados foi realizada utilizando o banco de dados do Dark Energy Survey (DES) através da infraestrutura do LIneA (Dados obtidos.ipynb).  
Os dados coletados incluem coordenadas, magnitudes e outros parâmetros astronômicos. Os dados foram salvos no formato CSV através da biblioteca do pandas e analisados a partir de um outro notebook (Fazendo análise.ipynb).

### 3.1 Dados Utilizados
O dataset coletado inclui as seguintes colunas principais e o que cada uma representa:
- `object_id`: Identificador único do objeto.
- `ra`: Ascensão Reta (em graus).
- `dec`: Declinação (em graus).
- `mag_g`, `mag_r`, `mag_i`: Magnitudes nas bandas g, r e i.
- `err_g`, `err_r`, `err_i`: Erros associados às magnitudes.
- `gmr` : Contém a diferença entre as magnitudes nas bandas g e r de cada objeto. Essa diferença é usada para calcular o índice de cor de um objeto celeste e assim ser feito o diagrama Cor-Magnitude.

## 4 Diagrama Cor-Magnitude
O diagrama cor-magnitude foi gerado com base nas magnitudes das bandas g, r e i. A cor foi
calculada como a diferença entre as magnitudes g e r (g-r), e a magnitude absoluta foi plotada no
eixo y, como é descrito no plot.

### 4.1 Por que o Diagrama Cor-Magnitude?
Os diagramas de cor-magnitude podem ser usados para validar um diagrama teórico, assim como para aferir distâncias e estimar as idades de populações estelares distintas.

## 5 Conclusão
A análise dos dados revelou informações interessantes sobre a distribuição dos objetos na região selecionada. Observou-se uma concentracão de objetos em determinadas faixas de magnitudes, sendo no ramo principal e também houve uma densidade considerável indicando estrelas frias. O diagrama apontou diferentes populacões de estrelas ou objetos distantes. É evidente que o diagrama cor-magnitude ajudanda a classificar diferentes tipos de estrelas, por isso de tamanha importância para a Astronomia.

## 6 Créditos
Dados do Dark Energy Survey (DES) DR2. Fonte: https://des.ncsa.illinois.edu/home
