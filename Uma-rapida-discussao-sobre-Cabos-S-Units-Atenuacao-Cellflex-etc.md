# Cabos, S-Units, Atenuação, Cellflex ou não Cellflex – Uma rápida discussão.

Este artigo é uma mensagem que mandei a um grande amigo explicando o racional da escolha de cabos de minha estação – Sou radioamador de apartamento, moro no 11 andar de um prédio de 15 e fiz o lançamento de dois cabos – Um para HF e outro para VHF/UHF. Foi utilizado no total 50 metros de cabos.

Abaixo segue uma racionalização da escolha de cabos que foi feita, esperando que possa ser útil a algum amigo.

* * *

# S-Units e dBs

Vamos primeiro falar de [S-Units](https://en.wikipedia.org/wiki/S_meter) e dBs.

O rádio mede a 'força' do sinal recebido em S-Units. É o bargraph/agulha que balança conforme a força do sinal recebido que vai de S0 até S9\. Em alguns rádios chega a +60 dB acima de S9.

Estritamente falando, cada S-Unit equivale a 6 dB. No entanto, fabricantes de rádios convencionaram a marcar cada S-Unit para 3 dB. Cada 3 dB também se traduz no dobro da potência transmitida/recebida.

Exemplo. Seja o véio Freire batendo um QSO com o Olivé véio lá em XAP em HF. Estou transmitindo a 100W e chego a S5 para você. Para eu subir o sinal em 1 pauzinho, virar S6, eu preciso dobrar a potência do rádio – e transmitir 200W. Para subir virar S7, já seriam nada desprezíveis 400W – E para virar S9, seriam incríveis 1600W – Mais que a potência máxima legal permitida (1500W).

No entanto, se eu cortar a potência para 50W só corta uma única S-unit, viro S4 para você. Portanto… Cada dB **importa**<span style="font-weight: normal">.</span>

# Caso de uso

Agora os requisitos de transmissão.

Vou operar em 3 bandas distintas:

HF (1.8-30 MHz)

VHF (144-148 MHz)

e UHF (430-450 MHz).

Daqui até o topo do prédio, via shaft do elevador, e mais alguns desvios, estimo em torno de 50 metros.

# Comparativos entre os cabos – Discussão

## RG-58

Agora veja o datasheet abaixo, do cabo RG-58, o coaxial normal 50 ohms que a gente utilizava em rede 10Base2:

[http://products.rfsworld.com/WebSearchECat/datasheets/pdf/?q=RG58-50JF](http://products.rfsworld.com/WebSearchECat/datasheets/pdf/?q=RG58-50JF)

Veja que na banda baixa de HF, em torno de 10 MHz, a perda é de 4.8 dB pra cada 100m. Perco um pouco mais de uma S-Unit do seu sinal chegando aqui (e transmitindo aqui também) só no cabo. Ou seja, dos 100W na saída do rádio sai algo em torno de 20W lá na entrada da antena.

Já na parte alta na banda de 10m, em 30 MHz, a gente já perde 8.5 dB em cada 100m. Calma q a coisa piora.

Em VHF, em 150 MHz esse cabo perde 19.2 dB a cada 100m e em UHF então, em 450 mega, quase sinal algum chega na ponta do cabo, com 36 dB de perda pra cada 100m. Tudo isso se dissipa ao longo do cabo na forma de calor via [efeito Joule](https://pt.wikipedia.org/wiki/Lei_de_Joule#Efeito_de_Joule).

E aí, sujou né?!

Então.... ao invés de comprar um amplificador linear, por que não usar um cabo melhor?

## RGC-213 (RG-213 rígido)

Vamos ver o cabo RG-213 rígido (RGC-213). Datasheet em [http://products.rfsworld.com/WebSearchECat/datasheets/pdf/?q=RGC213-50J](http://products.rfsworld.com/WebSearchECat/datasheets/pdf/?q=RGC213-50J)

No RGC-213, eu perco 2.3 dB a cada 100m em 30 MHz (parte alta do HF), o que já é BEM melhor, mas na banda de VHF eu perco 5.2 dB a cada 100M (quase 2 S-Units) e 9.5 dB em VHF (mais de 3 S-Units!!!)

Dá pra melhorar? Dá.

## Cellflex SCF

Na descida de HF usei esse cabo:

[http://products.rfsworld.com//websearchecat/datasheets/pdf/?q=SCF12-50J](http://products.rfsworld.com//websearchecat/datasheets/pdf/?q=SCF12-50J)

Na parte superior da banda de HF (30M), eu tenho uma perda de 1.73 dB para cada 100 metros, um pouco mais da metade de S-Unit. 50m de descida de cabo, 0.8 dB de perda. Show de bola, fechou.

Mas em UHF (450 MHz), ainda são nada desprezíveis 7 dB de perda, 2 S-units e pouco perdidas no cabo. Dá pra melhorar? Dá.

## Cellflex LCF

Usei o seguinte cabo para VHF e UHF:

[http://products.rfsworld.com/WebSearchECat/datasheets/pdf/cache/LCF12-50JFN.pdf](http://products.rfsworld.com/WebSearchECat/datasheets/pdf/cache/LCF12-50JFN.pdf)

Esse já me oferta 4.71 dB de perda a cada 100m em 450 MHz, ou seja, já é 1 S-unit a mais de vantagem em cima do cabo SCF. Para 50m de descida, 2.3 dB de perda, menos de uma S-Unit, FECHOU!

É isso aí meu compadre véio! Em RF o cabo também conta. E MUITO.

Um abração do véio Freire.
