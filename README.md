<h1 align="center">
<img src="https://img.shields.io/static/v1?label=REDES%20NEURAIS%20ARTIFICIAIS%20POR&message=MAYCON%20BATESTIN&color=7159c1&style=flat-square&logo=ghost"/>

<h3> <p align="center">CODE THE FUTURE - Reconhecimento de Doenças em Folhas de Tomate </p> </h3>
<h3> <p align="center"> ================= </p> </h3>


# Descritivo

#### Neste repositório você vai encontrar 4 pastas.

1. Dataset: Diretorio que contém os arquivos para teste e treino das folhas de tomate.
2. Material: Diretório onde encontram-se o arquivo de apresentação da aula.
3. Notebook: Diretório onde irá encontrar notebook usado no google colab.
4. Modelos: Diretório onde irá encontrar arquivos do modelo exportado da plataforma Teachnable Machine (contém também a instrução de como usar)

---
# Objetivos 

---
1. O objetivo deste notebook é Redes Neurais Convolucionais.
2. Os dados para usar serão clonados do nosso próprio github, pela pasta dataset.
3. Vamos treinar nosso modelo para que ele aprenda a detectar doença em plantações de tomate.
---

### Dicionário


Class	                                                  | Type  	  |    Description                              | Link para mais informações |
----------------------------------------------------------|:---------:|:-------------------------------------------:|:---------------------------:|
virus_mosaico_do_tomate_Y  	  										  	  |Class     | O agente causal da risca-do-tomateiro (PVY) ocorre de forma restrita em lavoruas de tomate no Brasil. São poucas as plantas hospedeiras do vírus. A transmissão é feita por pulgões, que adquirem o vírus em uma planta doente.	                    | [Link](https://www.embrapa.br/agencia-de-informacao-tecnologica/cultivos/tomate/producao/doencas-e-pragas/doencas/virus/mosaico-do-virus-y) |
mancha_alvo														  |Class    | A mancha-alvo, causada pelo fungo Corynespora cassiicola, é uma das principais doenças da soja e uma grande ameaça à agricultura brasileira, uma vez que sua incidência vem aumentando nas últimas safras.                         | [Link](https://agriculture.basf.com/br/pt/conteudos/cultivos-e-sementes/soja/mancha-alvo-principais-sintomas.html) |
mancha_bacteriana		     										  |Class     | A mancha-bacteriana é uma bacteriose de importância econômica secundária para a cultura da berinjela, jiló, pimenta e tomate, porém causa grandes perdas na cultura do pimentão. Danos: A bactéria pode ocorrer em todos os estágios de desenvolvimento da planta.	                | [Link](https://www.agrolink.com.br/problemas/mancha-bacteriana_1666.html) |
virus_folha_amarela  | Class | A doença da folha amarela, uma das principais pragas da cana-de-açúcar no Brasil, é causada por um vírus resistente ao tratamento térmico transmitido pelo pulgão Melanaphis sacchari | [Link](https://www.agrolink.com.br/noticias/estudo-busca-resistencia-a-doenca-da-folha-amarela_457815.html) |
requeima  | Class | A requeima causa manchas encharcadas, grandes e escuras nas folhas e nas brotações jovens, evoluindo para uma "queima" ou "mela" geral da planta (Figura 1). Na face inferior da lesão observa-se um mofo pulverulento esbranquiçado, que é a esporulação do fungo. Nos frutos, a prodidão é dura, de coloração marrom-escura. | [Link](https://www.embrapa.br/agencia-de-informacao-tecnologica/cultivos/tomate/producao/doencas-e-pragas/doencas/fungo/requeima) |
enrolamento_de_folha | Class | O sintoma do enrolamento da folha pode ocorrer em plantas jovens produzidas sob cobertura e plantadas no campo durante os períodos úmidos. Geralmente é observado mais tarde, em plantas com pelo menos 3 buquês e no período de verão. | [Link](http://ephytia.inra.fr/pt/C/5334/Tomate-Enrolamento-Fisiologico-das-Folhas) |
pinta_preta | Class | A pinta preta, causada por Alteranaria solani, é uma das doenças mais importantes na cultura do tomate. Manejá-la exige a integração de medidas que incluem o uso de fungicidas aplicados preventivamente ou assim que aparecerem os primeiros sintomas. | [Link](https://revistacultivar.com.br/artigos/como-controlar-pinta-preta-no-tomateiro) |
acaros | Class | Costuma se alojar na face inferior de folíolos – onde deposita seus ovos – e brotos, na região apical da planta. Infesta qualquer estádio de desenvolvimento do tomateiro. Adultos e ninfas perfuram e sugam as células da epiderme vegetal. | [Link](https://agriculture.basf.com/br/pt/conteudos/cultivos-e-sementes/tomate/tipos-acaro.html) |
folhas_saudaveis   | Class | Saúde dos Tomates
mancha_septoria   | Class | A septoriose ou mancha-de-septoria é uma doença importante do tomateiro nas épocas de chuva, ocorrendo em quase todas as regiões produtoras do Brasil e do mundo (Jones et al., 1991; Kurozawa & Pavan, 1997; Zambolim et al., 2000). | [Link](https://ainfo.cnptia.embrapa.br/digital/bitstream/item/103062/1/cot-37.pdf)|

---


--- 
# MACHINE LEARNING

### LOCAL - Clone/FORK

1. Clone o repositório para seu ambiente com o comando `git clone https://github.com/batestin1/coding_the_future_reconhecimento_de_pragas_com_redes_neurais.git`.
2. Abra a pasta Machine Learning e o notebook `cnn_para_doencas_de_folhas.ipynb` via juptyer notebook ou a IDE de sua preferência.

### COLAB

1. Clique no [Link](https://colab.research.google.com/drive/101JSh0JY97aWCij2iwIF1_8UrcuebG_z?usp=sharing)

----
