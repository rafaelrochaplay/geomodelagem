# Geomodelagem, Clima e Produção de Açaí

Repositório do trabalho da disciplina **Geomodelagem do Potencial Energético e do Microclima Urbano**, do Mestrado em Clima e Energia.

**Aluno:** Rafael Rocha Santa Rita  
**Grupo:** Rafael Rocha Santa Rita  
**Professora:** Dra. Raquel Jahara Lobosco  

## Objetivo

Desenvolver uma análise integrada da produção de açaí no Estado do Pará, combinando geoprocessamento, dados meteorológicos, modelagem espacial e visão computacional.

O trabalho foi dividido em três etapas:

1. **Mapeamento climático da região produtora de açaí**;
2. **Detecção de cachos de açaí e barbeiros com YOLO/Ultralytics**;
3. **Análise integrada entre clima, produção de açaí e presença do barbeiro**.

## Notebooks no Google Colab

Os códigos podem ser abertos diretamente no Google Colab pelos links abaixo:

- [Parte 1 — Mapeamento climático com ERA5-Land e Cartopy](https://colab.research.google.com/github/rafaelrochaplay/geomodelagem/blob/main/%28Parte%201%29mapeamento_climatico_era5land.ipynb)
- [Parte 2 — Detecção de açaí e barbeiro com YOLO/Ultralytics](https://colab.research.google.com/github/rafaelrochaplay/geomodelagem/blob/main/%28Parte%202%29uenf_acai_barbeiro_colab.ipynb)
- [Parte 3 — Análise integrada](https://colab.research.google.com/github/rafaelrochaplay/geomodelagem/blob/main/%28Parte%203%2903_analise_integrada_acai%282%29.ipynb)

## Parte 1 — Mapeamento climático

A Parte 1 utiliza dados meteorológicos do **ERA5-Land**, referentes ao ano de 2024, para produzir mapas sazonais do Estado do Pará.

Foram analisadas as seguintes variáveis:

- precipitação média às 15h;
- temperatura do ar às 15h;
- intensidade do vento às 15h;
- umidade relativa às 15h.

A região produtora de açaí foi representada a partir dos municípios de **Igarapé-Miri, Cametá e Abaetetuba**.

### Observação sobre os dados climáticos

Os arquivos NetCDF baixados do ERA5-Land não foram incluídos no repositório devido ao tamanho. Eles podem ser obtidos novamente pela execução do notebook da Parte 1.

Para executar a Parte 1, é necessário:

1. criar uma conta no Climate Data Store;
2. aceitar a licença do conjunto ERA5-Land;
3. criar no Google Colab um Secret chamado `CDS_KEY`, contendo a chave da API do Copernicus;
4. executar as células do notebook em ordem.

## Parte 2 — Visão computacional com YOLO/Ultralytics

A Parte 2 utiliza **YOLO/Ultralytics** para detectar elementos associados à produção de açaí e ao risco sanitário.

As classes trabalhadas foram:

- `acai`;
- `barbeiro`.

O treinamento foi realizado com imagens anotadas contendo cachos de açaí e o inseto barbeiro. O notebook apresenta exemplos de treinamento, validação, predição, curvas de métricas e matriz de confusão.

### Observação sobre o modelo treinado

O arquivo `best.pt`, gerado durante o treinamento, não foi incluído no repositório devido ao tamanho. O treinamento pode ser reproduzido pela execução do notebook da Parte 2.

Parte do conjunto de imagens possui caráter sintético, utilizado para fins acadêmicos e para viabilizar a construção inicial do dataset. Essa característica é discutida como limitação no relatório final.

## Parte 3 — Análise integrada

A Parte 3 utiliza a tabela climática gerada na Parte 1 para construir uma análise comparativa sazonal.

Foram integradas as seguintes informações:

- precipitação;
- temperatura do ar;
- umidade relativa;
- intensidade do vento;
- índice climático exploratório de produção.

O índice de produção é uma medida **exploratória** construída a partir da normalização das variáveis climáticas. Ele não representa produtividade agrícola real.

## Arquivos de resultados

O repositório inclui os principais arquivos gerados durante o trabalho, como:

- mapas climáticos sazonais;
- imagens de treino, validação e predição do YOLO;
- curvas de treinamento e matriz de confusão;
- tabela integrada da Parte 3;
- gráficos da análise integrada;
- relatório final em PDF.

## Limitações

A análise deve ser interpretada como uma aplicação acadêmica exploratória. Não é possível afirmar causalidade direta entre clima, produção de açaí e presença do barbeiro sem dados adicionais de campo.

Entre as principais limitações estão:

- uso de dados de reanálise em vez de medições locais;
- uso de apenas um ano de dados climáticos;
- análise climática concentrada no horário de 15h;
- dataset visual limitado;
- presença de imagens sintéticas no treinamento;
- ausência de amostragem de campo padronizada por estação.

## Relatório final

O relatório final em PDF apresenta a metodologia, os resultados, os mapas climáticos, as imagens de detecção, a análise integrada e as conclusões do trabalho.

## Repositório

https://github.com/rafaelrochaplay/geomodelagem/tree/main
