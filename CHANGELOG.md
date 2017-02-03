# Change Log
Todas as principais alterações deste projeto serão documentadas neste arquivo.

Este formato é baseado no [Keep a Changelog](http://keepachangelog.com/)
e este projeto adere ao [Semantic Versioning](http://semver.org/).


## [0.1.0] - 2016-05-12
### Added
- Método para o cálculo do percentual submerso (caso de elemento parcialmente 
submerso).
- Método para cálculo da força de fluido interno para análise de riser e
mangote. Adicionalmente, foram realizadas melhorias no cálculo dos 
coeficientes do polinômio de Hermite.
- Criação de classes para calcular os esforços provenientes do efeito de onda
sobre a linha.
- Consideração da aproximação de Wheeler para avaliar a velocidade de 
correnteza acima do nível médio da água do mar.

### Changed
- Modificação do método de cálculo da cinemática da onda para considerar uma
aproximação para o caso de águas profundas (manter compatibilidade com a
formulação presente no TPN).


## [1.3.2] - 2013-11-26
### Fixed
- Correção de problema. Estava ocorrendo um acesso indevido a uma posição do
aceleração na classe IntAlg. Esse acesso indevido estava sendo realizado em
teste condicional para saber se o valor da aceleração é NAN ou INF. 
Portanto, caso a simulação transcorresse até o final o resultado não seria 
afetado.


## [1.3.1] - 2013-04-16
### Added
- Inclusão de mais uma função de interpolação denomida Hermite. Trata-se de 
um polinômio do terceiro grau que utiliza, além do valor da função o valor
da sua derivada.


## [1.3.0] - 2013-03-06
### Added
- Inclusão do algoritmo de integração temporal adaptativo.

### Changed
- Ajuste do cálculo do engastamento perfeito para incluir as parcelas 
inercias devida a massa da estrutura e a massa adicional (formulação
de Morison).
- Alteração no método que faz a integração no tempo para retornar um valor
informando se o cálculo foi bem sucecido ou não.
- Ajustes na geração da malha feita pela classe Line, de forma a permitir que
a geração de malhas curtas (distância entre as extremidades maior que o 
comprimento da linha).

### Fixed
- Correções no método de cálculo da força de atrito para deixar compatível
com a formulação presente no OrcaFlex.
