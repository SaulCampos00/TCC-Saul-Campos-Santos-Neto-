A utilização de religadores automáticos para proteção, automação e melhoria da rede elétrica.

Saul de Campos Santos Neto (FHO)
Prof. Dr. Daniel Augusto Pagi Ferreira (FHO)

Resumo
A energia elétrica é indispensável em vários setores da sociedade, como nas residências, no comércio, na indústria e nas áreas rurais. Para garantir um fornecimento contínuo e seguro, os dispositivos de proteção instalados na rede elétrica precisam ser eficientes e adaptáveis, permitindo que a empresa responsável pelo abastecimento de energia cumpra integralmente as normas estabelecidas pelos órgãos reguladores e reduza ao máximo as interrupções inesperadas. Seguindo os parâmetros normativos o self-healing já estava implantado porem obtense uma expansão de rede e o acréscimo de equipamentos para melhorar a automação aumentando eficiência no restabelecimento aumentam a confiabilidade e a qualidade da energia elétrica. Como a maior parte dos defeitos em redes de distribuição é de natureza transitória, é fundamental empregar dispositivos de proteção com religação automática. Caso o defeito persista, apenas o primeiro dispositivo a montante deverá ser desligado. Este artigo aborda as técnicas mais comuns de coordenação de proteção em redes de distribuição, ressaltando a importância de compreender o funcionamento dos dispositivos para melhorar sua coordenação.
Palavras-Chaves: distribuição, relé de proteção, sistema self-healing.

Introdução
O sistema elétrico de potência é um conjunto de dispositivos e infraestruturas que colaboram para gerar, transmitir e distribuir energia elétrica aos consumidores, conforme padrões de qualidade, segurança e custos estabelecidos. A confiabilidade é essencial, indicando o período em que os componentes, partes ou sistemas operam sem apresentar falhas, junto com a disponibilidade. Estes dois fatores são fundamentais para avaliar a eficiência do sistema (BITTENCOURT, 2016).
A ANEEL (2022) regula o setor elétrico no Brasil, incluindo o automatismo da rede de distribuição para garantir segurança e eficiência. Isso envolve estabelecer diretrizes para que as concessionárias utilizem tecnologias que melhorem a resposta a falhas e variações na demanda, visando um serviço de qualidade para aos consumidores.
Ferreira (2011) e Luiz (2012) apresentaram sobre quais aspectos de proteção de redes de distribuição de energia elétrica sofrem alterações procedimentais e normativas quando há geradores distribuídos conectados na rede.
A automação da rede elétrica possibilita a detecção ágil e precisa de falhas e interrupções, superando em velocidade e precisão o monitoramento manual. Essa agilidade permite respostas imediatas das equipes de manutenção, encurtando o tempo de inatividade para os usuários finais. Em comparação com métodos manuais de detecção, que dependem de relatos de clientes ou verificações periódicas, a automação garante uma identificação rápida das falhas, muitas vezes antes mesmo de serem perceptíveis pelos usuários finais.
Automação é descrita como uma fusão de subsistemas que permite a uma empresa concessionária monitorarem, coordenar e operar parcial ou totalmente os componentes do sistema elétrico em tempo real. Ela implica o uso de tecnologia para facilitar os procedimentos operacionais executados por dispositivos mecânicos ou eletrônicos. Esta definição é ampla e incluem diversos subsistemas frequentemente considerados de forma independente, tais como supervisão e controle de subestações, monitoramento e controle da rede elétrica, gestão de carga, medição remota, atendimento às reclamações dos consumidores, engenharia, entre outros (CRISPINO, 2000).
Segundo MAMEDE FILHO, (2024) uma subestação desempenha um papel crucial no sistema elétrico ao reduzir ou elevar o nível de tensão associado à potência que chega aos terminais primários (subestação abaixadora) ou aos terminais secundários (subestação elevadora) dos transformadores, que são seus elementos mais importantes. Essa função permite a transmissão eficiente e segura da energia elétrica ao longo da rede.
 BATISTA, (2008) em situações de contingência, é crucial controlar em tempo real os fluxos de potência dos equipamentos envolvidos para garantir a estabilidade e segurança do sistema elétrico.
A avaliação e regulação da excelência do serviço elétrico são conduzidas por diretrizes estabelecidas pela serie de documentos Regras e Procedimentos de Distribuição (PRODIST) da Agencia Nacional de Energia Elétrica (ANEEL). Os procedimentos relativos aos indicadores de continuidade, tempo de resposta e monitoramento automatizado da qualidade da energia fornecida, através do cálculo de indicadores individuais e agregado. São estabelecidos métodos para a divulgação desses indicadores e o gerenciamento de interrupções no fornecimento de energia.
Self-healing é a habilidade da rede de detectar, isolar o problema, reduzir o impacto nos clientes afetados e restaurar o serviço o mais rápido possível, com intervenção humana mínima. Isso implica que o sistema seja inteligente o suficiente para tomar e programar decisões. Essa capacidade da rede segue a sequência de análise, isolamento e restauração, usando configurações automáticas (ANDRADE, 2022).
O objetivo deste trabalho é estudar um caso real de melhoria e expansão da rede de distribuição elétrica, destacando a importância crucial da proteção e automação. Será abordado como automatização da rede poderá desempenhar um papel fundamental na redução do número de usuários afetados por falhas acidentais.
A rede estudada é uma subestação de 34,5 kV com um único alimentador que atende um bairro isolado de uma cidade no interior do Estado de São Paulo, com cerca de 1600 unidades consumidoras urbanas e rurais. Quando ocorre alguma falha na há contingencia nesta rede ou um desligamento acidental todos os clientes são afetados, prejudicando os indicadores de qualidade de energia elétrica para esta região.

Revisão Bibliográfica
Indicadores de qualidade da energia elétrica
DEC: (Duração Equivalente de Interrupção por Unidade Consumidora) representa o desligamento médio em horas de um conjunto de clientes. 
DEC=i=1nCai*t(i)Cs
Ca- clientes interrompidos;
t- tempo em horas;
Cs- clientes totais do conjunto (localidade);
n- total de desligamentos.
FEC: (Frequência Equivalente de Interrupção por Unidade Consumidora) representa a quantidade media de vezes na qual os clientes de um conjunto ficam sem energia.
DEC=i=1nCaiCs
Ca- clientes interrompidos;
Cs- clientes totais do conjunto (localidade);
n- total de desligamentos.
DIC: (Duração de Interrupção Individual por Unidade Consumidora) representado para consumidores individuais.
DIC=i=1nti
t- tempo em horas;
n- total de desligamentos.
FIC: (Frequência de Interrupção Individual por Unidade Consumidora) representa a quantidade media de vezes na qual o cliente ficou sem energia.
FIC=n
n- total de desligamentos
Aspectos de proteção do sistema de distribuição elétrica 
Seletividade
A seletividade é essencial para a eficiência e a confiabilidade dos sistemas de proteção elétrica. Ela garante que, ao detectar correntes anormais, como as causadas por uma falha, apenas os dispositivos de proteção que estão mais próximos do ponto de falha atuem. Desta forma, o sistema desenergiza exclusivamente a parte afetada do circuito, preservando o restante da rede em funcionamento (MAMEDE FILHO, 2013).
Para programar essa seletividade, os dispositivos de proteção, como religadores e religadores automáticos, são configurados com tempos de atuação e configurações de corrente específicas. Esses ajustes permitem que a resposta à falha sejam rápidas e localizadas reduzindo o impacto para os consumidores e mantendo a rede elétrica mais confiável.
Serão destacados dois tipos de seletividade a cronométrica e a amperimétrica.
Seletividade cronométrica 
A seletividade cronométrica é uma técnica de coordenação de dispositivos de proteção elétrica que utiliza o tempo como base para garantir que apenas o dispositivo mais próximo do ponto de falha no primeiro momento. Ela consiste em definir diferentes tempos de operação para os dispositivos de proteção ao longo da rede elétrica, criando uma posição de atuação com base na localização (MAMEDE FILHO, 2013).
A Figura 1a mostra a característica de tempo definido e a Figura 1b mostra a curva de tempo inverso.




Figura 1 – a) Curva de tempo definido genérica e b) Curva de tempo inverso genérica
a)
b)



Fonte: adaptado de Mamede Filho (2013)
Seletividade Amperimétrica.
Na prática, isso significa que os dispositivos de proteção mais próximos da carga são configurados para atuar em correntes de falha mais baixas, enquanto os dispositivos mais próximos da fonte de energia possuem configurações para correntes de falha mais elevadas (MAMEDE FILHO, 2013).
Ip2>Ics>Ip1
Sendo:
Ics = Corrente de defeito no ponto;
Ip1 = Ajuste de corrente de proteção numero 1;
Ip2 = Ajuste de corrente de proteção numero 2.
Coordenação
A coordenação em sistemas elétricos é definida pela disposição de dois ou mais dispositivos de proteção em série, configurados para operar em uma sequência específica e predefinida. O objetivo dessa sequência é garantir que, em caso de falhas ou sobrecorrentes, apenas o dispositivo mais próximo ao ponto de falha no primeiro dia, enquanto os demais aguardam, conforme seus tempos de retardo e ajuste.
A figura 3 2 ilustra a coordenação entre os múltiplos reles de proteção da concessionária, onde as curvas de proteção para garantir a coordenação os reles mais longe da fonte devem estar a esquerda dos mais próximos da fonte.
Figura 3- Coordenograma genérico de proteção

Fonte: Neoenergia Elektro (2022)
Self-healing
Self- healing pela tradução literal é auto-cura. No caso das redes elétricas isso se traduz na capacidade que a própria rede elétrica tem de isolar o problema, o mais rapidamente possível sem intervenção humana.
O Self healing descentralizado é constituído por algumas lógicas. A seguir serão apresentadas algumas definições pertinentes sobre este assunto.
Ilhas de self- healing: são conjuntos de equipamentos onde podem conter 2 ou mais equipamentos onde que possuem lógicas de recomposição automática.
Tempo de atuação: é predefinido para abertura ou fechamento após sensibilizar falta de tensão e corrente.
Bloqueio: tempo definido ao equipamento para que não repita o ciclo de proteção
Feeder: lógica predefinida para equipamento fazer sua abertura com tempo definido após a sensibilização de falta de tensão a montante do mesmo. Em fluxo normal equipamento estará sempre normalmente fechado e habilitado a recomposição automática sendo ele Religador ou Seccionalizador
Tie: lógico predefinido para equipamento fazer seu fechamento com tempo definido respeitando o tempo do Feeder, a sensibilização de falta de tensão a montante e ajusante do TIE sempre normalmente aberto, com proteção para single-shot.
Single- shot: (Disparo único) é a proteção envolvendo o Tie após o ciclo do feeder. Tie da um single-shot para tentativa de reenergização do sistema. 
A Figura 4 3 apresenta todas as questões anteriores. Tomando um destaques nas ilhas de Self-Healing são pintadas de cinza,  e o Feeder feeder esta está representado pelo quadrado pintado em vermelho e o Tie representado em amarelo nas ilhas de self-healing.
Figura 4 – Ilhas de self-healing 

Fonte: Neoenergia Elektro (2022).
Religador de proteção automático e suas funções.
Religador automático Figura 5 é um modulo compacto com circuito capaz de detectar sobrecorrentes, sobtensões, subtensões, correntes de fuga entre outras proteções. 
Figura 5 – Religador automático 

Funções do religador em um só equipamento
As seguintes funções e equipamentos para religação são encontradas em redes de distribuição de energia elétrica.
RL: Religador automático com proteção para fase, terra, rele de alta impedância (Raí), atuando independente da sua retaguarda, esta ilustrado na Figura 6.
Figura 6 – Ciclo de atuação do RL com curto-circuito

Fonte: Neoenergia Elektro (2022)
SL: O seccionalizador é um religador automático, utilizado sempre em conjunto com outros equipamentos de proteção, normalmente um religador e um disjuntor na sua retaguarda. Este modo de operação não permite abrir por curto circuito somente na ausência de corrente gerado pela sua retaguarda. A cada abertura de sua retaguarda ele abre contagem para dar seletividade, no caso se a sua retaguarda tiver três aberturas o seccionalizador terá duas aberturas, esta ilustrado na Figura 7.
Figura 7 – ciclo de abertura do SL acompanhando a falta de tensão e corrente da retaguarda.

Fonte: Neoenergia Elektro (2022).
IF - é um religador automático com a funcionalidade de o seccionalizador pôr não faz abertura dependendo da retaguarda. Ele é somente usado para monitorar corrente de curto e comando remoto pelo centro de operação para isolar rede ou manobras. 
CZ - é um religador automático com a funcionalidade de chave faca, em sua lógica não tem proteção é apenas para comando remoto ou manual. Caso esteja com a função de TIE ele pode ter proteção de fase, terra e Raí porem com o single- shot. 
Há ainda dispositivos de seccionamento nas redes de distribuição de energia elétrica, principalmente as chaves faca e fusível.
As chaves faca e fusível também são muito utilizadas em sistemas de distribuição de energia elétrica para seccionamento e proteção, respectivamente.  A chave seccionadora unipolar tipo faca é utilizada em redes de distribuição de energia para manobra do sistema, provida de gancho para utilização de ferramenta de abertura em carga (COCEL, 2020);
Já na chave porta fusível quando ocorre um curto circuito pode ser substituído o fusível. Em transformadores é utilizado para dar proteção aos clientes da rede elétrica secundaria. São utilizadas também em linha rurais, e em outros tipos de proteções como cabine primarias de clientes (). 
Objetivo 
O objetivo deste trabalho é estudar um caso real de melhoria e expansão da rede de distribuição elétrica, destacando a importância crucial da proteção e automação. Será abordado como automatização da rede poderá desempenhar um papel fundamental na redução do número de usuários afetados por falhas acidentais.
A rede estudada é uma subestação de 34,5 kV com um único alimentador que atende um bairro isolado de uma cidade no interior do Estado de São Paulo, com cerca de 1600 unidades consumidoras urbanas e rurais. Quando ocorre alguma falha na há contingencia nesta rede ou um desligamento acidental todos os clientes são afetados, prejudicando os indicadores de qualidade de energia elétrica para esta região.
Metodologia
A rede elétrica representado na figura 8 deste estudo de caso tem constantes desligamentos acidentais, há pontos de contingencias pôr não são muito eficazes. Esta rede tem como fonte o interruptor BAL 52-1 e se estende até o religador automático ITN001666, atendendo um total de 1.636 clientes. Essa rede conta com um sistema automatizado que integra os religadores automáticos ITN00428, ITN001666 e ITN00485..

Figura 8 – Diagrama unifilar da rede atual

A rede elétrica representado na figura 8 deste estudo de caso tem constantes desligamentos acidentais, há pontos de contingencias pôr não são muito eficazes. Esta rede tem como fonte o interruptor BAL 52-1 e se estende até o religador automático ITN001666, atendendo um total de 1.636 clientes. Essa rede conta com um sistema automatizado que integra os religadores automáticos ITN00428, ITN001666 e ITN00485.
A rede atual é constituída por:
Subestação de 34,5 kV rebaixadora para 13,8kV;
Alimentador 13,8 kV (Al 24);
Religador automático com função IF NF (ITN00428);
Religador automático na função SL NF (ITN01669);
Religador automático na função de CZ NA (ITN01666);
Dois ramais com chave fusível (ITN00257) e (ITN00917);
Chave faca (ITN01547) interligação entre o disjuntor (IT02-Al 24) e o alimentador (52-01). 
Na primeira forma do automatismo, quando ocorre um desligamento da rede a montante do ITN00428, ocorre a temporização de dois equipamentos, com intervalos de 70 e 80 segundos. Após esse período, os equipamentos Feeder ITN00428 e Tie ITN01666 mudam seu status, consecutivamente, para normalmente aberto e normalmente fechado. Essa mudança permite que a energia seja reestabelecida, alimentando todos os clientes que foram afetados pelo desligamento.
Outra parte da automação da rede diz respeito à seletividade entre os picos do disjuntor BAL 52-1 e o equipamento ITN01669. O religador automático possui quatro possibilidades de aberturas, proteção para fase, neutra, relé de alta impedância (RAI) e por automatismo, enquanto o ITN01669 atua como seccionalizador (SL). Para que haja seletividade com o religador automático, suas proteções devem ser ajustadas para níveis um pouco mais baixos. No entanto, devido à distância do equipamento ate o disjuntor não há seletividade por proteção.
Assim, cada vez que o ITN01669 alertar sobre a falta de tensão no montante, será iniciada a contagem até três aberturas. Caso o defeito esteja à jusante do ITN01669, na penúltima abertura do disjuntor, o ITN01669 irá isolar o defeito, permitindo que o disjuntor BAL 52-1 ligue a rede novamente. Com o SL ITN01669 realizando a abertura em conformidade com a seletividade do interruptor BAL 52-1, o equipamento Tie ITN001666 tentará religar a rede elétrica. Contudo, por motivos de proteção, esse trecho permanecerá desligado até que a situação seja regularizada, esta ilustrada na Figura 8.
A rede com esse automatismo é eficiente porem todos os desligamentos involuntários por defeitos permanente podem ser demorados os restabelecimentos por falta de manobras e outras fontes de alimentação.
Segundo ANEEL (2021) são permitidos piques com ate 180 segundos, que não serão contabilizados como desligamento afetando os indicadores.
A figura 9 apresenta um fluxograma que contem as possibilidade de operação dos dispositivos de seccionamento e proteção da rede de distribuição de energia elétrica estudada.
Figura 9 – fluxograma da atuação do self-healing

A figura 10 apresenta a rede elétrica unifilar vista pelo Google Earth, onde se encontra maior acumulo de sua carga.
Figura 10 – vista de satélite da rede elétrica estudada e destacada na cor vermelha

Fonte:  Google Earth.

Resultados 
A proposta inclui as seguintes inserções:
Religador automático na função CZ com automatismo (self-healing TIE) substituindo a chave fusível (ITN00257);
Religador automático na função RL NF com automatismo (self-healing FEEDER) substituindo a chave faca (ITN01547);
Acrescentar a extensão de rede entre os ramais (ITN00257)  ate (ITN00917);
Religador automático na função SL no equipamento (ITN01608);
Manter aberto a chave faca (ITN01607)

Figura 11 - Esquema unifilar atualizado

Execução do automatismo 
Após um desligamento da subestação BAL 52-10 e BAL 52-1, os equipamentos Feeder ITN00428 e o Tie ITN00257 iniciam temporizações simultâneas de 70 e 80 segundos, respectivamente. Quando esse tempo se esgota, o Feeder realiza a abertura do circuito, enquanto o Tie executa o fechamento. Esse processo permite o isolamento do trecho afetado e, ao mesmo tempo, tenta religar a rede por uma fonte alternativa, garantindo a continuidade do fornecimento de energia para as áreas que não foram diretamente impactadas pelo desligamento.
Após uma atuação do BAL 52-1 por proteção, ele fará três aberturas com intervalos realizados de 1/2, 20 e 60 segundos. A cada abertura, o equipamento SL ITN01608 contará duas ausências de corrente e automaticamente seccionará a rede. O IF ITN00428, ao detectar falta de tensão, irá temporizar por 70 segundos e, em seguida, fará o seccionamento da rede.
O Tie ITN00257, também ao perceber a ausência de tensão, iniciará uma temporização de 80 segundos. Após esse período, ele tentará religar a rede utilizando outra fonte de alimentação. Caso não haja detecção de curto-circuito, o Tie permanecerá ligado, energizando a rede até o SL ITN01608 e isolando o trecho entre o ITN00428 e o ITN01608, garantindo a segurança e continuidade no fornecimento de