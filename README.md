# Predição de Eventos Extremos

> Modelo de Machine Learning (rede neural LSTM) para previsão de eventos extremos do clima espacial — tempestades geomagnéticas medidas pelo índice Dst.

![Python](https://img.shields.io/badge/Python-3.x-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange)
![License](https://img.shields.io/badge/License-MIT-green)

**Equipe CDI:** Andrei Ferreira Inomata, Caio Henrique Lima de Andrade, Guilherme Magalhães Lima, Sofia Souza Costa e Vitor Manoel Emidio Machado.

## Sobre o projeto

Este projeto desenvolve um modelo de *Machine Learning* para prever a ocorrência de
eventos extremos do clima espacial, com foco em tempestades geomagnéticas. A partir de
dados de vento solar, posição de satélites e manchas solares, uma rede neural do tipo
**LSTM (Long Short-Term Memory)** é treinada para prever o índice **Dst**.

Desenvolvido para o **VII Desafio em Ciência de Dados**, parte do **X Congresso de
Ciência, Tecnologia e Inovação da PUC Goiás**.

## Funcionalidades

- Coleta e pré-processamento de dados históricos de clima espacial.
- Treinamento de modelo LSTM para previsão de eventos extremos.
- Avaliação de desempenho e ajuste de hiperparâmetros.
- Visualização dos resultados da previsão.

## Estrutura do projeto

```
Predicao-Eventos-Extremos/
├── data/                  # Conjuntos de dados (CSV)
│   ├── labels.csv
│   ├── satellite_pos.csv
│   └── sunspots.csv
├── models/                # Modelo treinado e configuração
│   ├── model.keras
│   ├── config.json
│   └── scaler.pck
├── notebooks/             # Notebooks de análise e modelagem
│   └── PredicaoDST.ipynb
├── docs/                  # Relatório e documentação
│   └── Relatorio_Equipe_CDI.pdf
├── references/            # Artigos científicos de referência
├── requirements.txt       # Dependências Python
├── LICENSE
└── README.md
```

## Dados

Provenientes de fontes públicas de clima espacial:

- **NASA** — National Aeronautics and Space Administration
- **NOAA** — National Oceanic and Atmospheric Administration

> Observação: o arquivo `solar_wind.csv` referenciado no notebook não é versionado por
> conta do tamanho. Baixe-o da fonte original e coloque-o em `data/` antes de executar.

## Modelo

- Rede neural **LSTM (Long Short-Term Memory)**.
- Métrica de avaliação: **RMSE** (Raiz Quadrada do Erro Médio).

## Como executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/CaioHenri99/Predicao-Eventos-Extremos.git
   cd Predicao-Eventos-Extremos
   ```
2. (Opcional) Crie um ambiente virtual:
   ```bash
   python -m venv .venv
   source .venv/bin/activate   # Windows: .venv\Scripts\activate
   ```
3. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
4. Abra o notebook:
   ```bash
   jupyter notebook notebooks/BaseDadosLabelsV1_8.ipynb
   ```

> Se for rodar no Google Colab, ajuste os caminhos de leitura dos dados para a pasta `data/`.

## Links úteis

- MagNet: https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2023SW003514
- NOAA: https://www.noaa.gov/
- Machine Learning para previsão de eventos climáticos: https://www.youtube.com/watch?v=uyYT6c0rUss

## Comissão organizadora

- Profª. Maria José Pereira Dantas
- Prof. José Elmo de Menezes

## Contato

| Participante | E-mail |
|---|---|
| Caio Henrique Lima de Andrade | infinit.dev7@gmail.com |
| Andrei Ferreira Inomata | andreiinomata36@gmail.com |
| Sofia Souza Costa | sofiacosta@discente.ufg.br |
| Guilherme Magalhães Lima | guimaglima-2004@hotmail.com |
| Vitor Manoel Emidio Machado | vitoremidiomachado@gmail.com |

## Licença

Distribuído sob a licença MIT. Veja [LICENSE](LICENSE) para mais informações.

---

> Este projeto tem fins de pesquisa e não deve ser utilizado para tomar decisões
> críticas sem a devida análise de especialistas.
