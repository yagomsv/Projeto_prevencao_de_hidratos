![Sem título](https://user-images.githubusercontent.com/101029639/216844549-a90c1127-98b5-4709-9515-2c9b678eb2d1.png)

## Projeto: Prevenção de formação de hidratos em poços de petróleo utilizando modelos de Aprendizagem de Máquina

Na indústria do petróleo, assim como em outras atividades industriais tem crescido a demanda por encontrar formas de se realizar essas operações de forma segura, produtiva, com qualidade e com eficiência energética. Para isso o controle desses processos se faz necessário, a fim de se evitar a ocorrência de eventos indesejados, como falhas ou mau funcionamentos. Falhas são caracterizadas por desvios ou anomalias na operação normal de um processo, que podem ser identificadas por sinais de vibração de uma máquina, sensores de temperatura e pressão de um processo e etc.

Na indústria do petróleo falhas em poços de petróleo podem causar grandes perdas de produção. A Petrobras S.A (Brasil) estima que durante o ano de 2016 cerca de 1,5 milhões de barris de petróleo foram deixados de ser produzidos devido a falhas em seus poços, o que correspondia na época a uma **perda de arrecadação de USD 75,7 milhões**, levando em consideração que o **preço médio do barril de petróleo na época era de USD 50,0.**

Existem diversas falhas que podem acontecer em poços de petróleo e suas linhas de produção, mas nesta aplicação focaremos na detecção da falha de "formação de hidratos". Em particular, essa falha pode ocorrer em poços *off- shore* e causar grandes problemas operacionais, pois na sua ocorrência o poço pode parar completamente de produzir devido a grande obstrução causado pela formação de hidratos nas linhas de escoamento do óleo do leito marinho até as plataformas de produção. Segundo dados da própria Petrobras Unidade Operaciona do Rio de Janeiro, entre os anos de 2014 e 2017 essa foi a falha que causou maior perda cumulativa de produção de óleo.

Hidratos são compostos cristalinos, de aparência semelhantes ao gelo, formados pela reação do gás natural com a água. Para que o hidrato se forme, é necessário que se tenha água e gás na presença de alta pressão e baixas temperaturas. Condições essas encontradas no escoamento da mistura produzida em reservatórios localizados em elevadas lâminas d'água, como é o caso dos reservatórios do Pré-Sal.

Nesse estudo foram utilizados dados reais e simulados de um processo de produção de petróleo com a medição de variáveis e a detecção de formação de hidratos nas linhas de produção dos poços. Os dados foram coletados e produzidos durante os anos de 2017 e 2018 e conta com 81 instâncias simuladas e 3 instâncias reais.

O objetivo desta aplicação foi realizar uma análise exploratória dos dados para entender melhor o comportamento das variáveis ao longo do processo, além de identificar variáveis congeladas e faltantes. Posteriormente foi realizado a criação de modelos de *Machine Learning* para classificação binária da condição dos poços (normal ou em falha). Para a criação dos modelos foi optado por utilizar uma metodologia que sugere a criação de modelos mais simples até modelos mais robustos, avaliando-os e escolhendo aquele que melhor se encaixar a situação problema.

### Descrição das variáveis do processo:
- P- PDG: Pressão na PDG (Pa);
- P- TPT: Pressão no Transdutor de pressão e Temperatura do poço (Pa);
- T- TPT: Temperatura no Transdutor de pressão e Temperatura do poço (°C);
- P-MON-CKP: Pressão a montante na PCK (Válvula choke de produção) (Pa);
- T-JUS-CKP: Temperatura a jusante na PCK (°C);
- P-JUS-CKGL: Pressão a jusante na GLCK (Gás lift) (Pa);
- T-JUS-CKGL: Temperatura a jusante na GLCK (Gás lift) (°C);
- **QGL:** Vazão do Gás lift (m³/s).

### Ferramentas e dados utilizados:
- Manipulação, limpeza e análise exploratória dos dados: Pandas, Numpy, missingno;
- Visualização dos dados: Matplotlib;
- Machine Learning: Scikit- Learn (Modelos de classificação Regressão Logística e Árvores de Decisão)
- Fonte dos dados: https://www.sciencedirect.com/science/article/pii/S0920410519306357?via%3Dihub
