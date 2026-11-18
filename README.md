[readme_md_desafio_citizentech.md](https://github.com/user-attachments/files/35003315/readme_md_desafio_citizentech.md)
# 🌐 Global Solution (2º Semestre) — Desafio CitizenTech

Repositório dedicado aos entregáveis da avaliação **Global Solution (2º Semestre)**, com foco na coleta, organização e análise estatística aplicada de dados públicos do Brasil para fundamentar o desenvolvimento do **Assistente Digital CitizenTech**.

---

## 👥 Integrantes do Grupo

| Nome Completo | RM |
| :--- | :--- |
| **LUCAS CARAM BUENO** | `RM570158` |
| **NICOLAS ANDRADE** | `RM572782` |

---

## 🎯 Contexto e Objetivo do Projeto

O **Desafio CitizenTech** propõe o desenvolvimento de soluções tecnológicas acessíveis que aproximem os cidadãos de informações essenciais do cotidiano — como direitos sociais, emissão de documentos civis, serviços de saúde e orientações comunitárias.

Para embasar tecnicamente a arquitetura do assistente digital, este projeto aplica métodos estatísticos em **Python** sobre indicadores oficiais do **IBGE** para as **27 Unidades da Federação (UFs)**, investigando como fatores socioeconômicos e estruturais (renda per capita, alfabetização e urbanização) influenciam a inclusão digital no país.

---

## 📂 Estrutura do Repositório

```text
├── base_dados_citizentech.csv          # Base de dados oficial consolidada do IBGE (27 UFs)
├── analise_estatistica_citizentech.py  # Script Python com análises estatísticas e protótipo lógico
├── relatorio_estatistico_citizentech.pdf # Relatório estatístico executivo completo
└── README.md                           # Documentação do repositório
```

---

## 📊 Base de Dados (`base_dados_citizentech.csv`)

Os dados empíricos foram consolidados a partir de levantamentos oficiais do **Instituto Brasileiro de Geografia e Estatística (IBGE)** (PNAD Contínua TIC, Rendimento Domiciliar per Capita, PNAD Contínua Educação e Censo Demográfico):

- **`Taxa_Acesso_Internet` (%)**: Percentual da população de 10 anos ou mais com acesso à internet.
- **`Renda_Per_Capita_RS` (R$)**: Rendimento nominal mensal domiciliar per capita.
- **`Taxa_Alfabetizacao` (%)**: Taxa de alfabetização da população de 15 anos ou mais.
- **`Taxa_Urbanizacao` (%)**: Percentual da população residente em áreas urbanas.
- **`Alta_Conectividade` (0 ou 1)**: Variável binária indicadora de estados com conectividade igual ou superior ao patamar nacional de referência (`92,5%`).

---

## 🔬 Metodologia Estatística Aplicada

O script `analise_estatistica_citizentech.py` e o relatório executivo contemplam:

1. **Análise Exploratória e Descritiva**: Medidas de tendência central e dispersão populacional/amostral para as 27 UFs.
2. **Distribuição Normal de Probabilidade**: Cálculo de probabilidades acumuladas em torno da média (`50,00%` — evento equiprovável) e acima da mediana (`37,54%` — evento menos provável).
3. **Testes de Hipóteses para a Média (Teste Z)**: Testes unilaterais à esquerda ($n = 20, \alpha = 6\%$) e à direita ($n = 25, \alpha = 9\%$).
4. **Análise Bivariada e Regressão Linear Simples**: Correlação de Pearson ($r = +0,8184$), ajuste por Mínimos Quadrados Ordinários ($R^2 = 66,97\%$, $F = 50,69$) e previsão pontual.
5. **Análise Multivariada e Regressão Linear Múltipla**: Matrizes de covariância e correlação, regressão múltipla ($R^2 = 72,71\%$, $F = 20,43$) e simulação de cenários.
6. **Regressão Logística Binária**: Classificação territorial de prontidão digital com matriz de confusão e acurácia global.
7. **Protótipo Lógico CitizenTech**: Demonstração funcional de consulta informativa verificável, sem coleta de dados pessoais sensíveis e com tratamento de entradas inválidas.

---

## ⚙️ Como Executar o Código Python

1. Certifique-se de ter o **Python 3.9+** instalado em seu ambiente (ou utilize o Google Colab / Jupyter Notebook).
2. Instale as bibliotecas necessárias:
   ```bash
   pip install numpy pandas scipy statsmodels scikit-learn matplotlib seaborn
   ```
3. Execute o script principal na mesma pasta em que se encontra o arquivo `.csv`:
   ```bash
   python analise_estatistica_citizentech.py
   ```
