Aqui está uma proposta de texto para o arquivo `README.md` do seu projeto, estruturada de forma profissional e baseada no conteúdo do seu notebook.

---

# AP2 - Análise de Produção de Combustível

Este projeto foi desenvolvido como parte da avaliação AP2 para a disciplina de **Laboratório de Ciência de Dados** (CK0441). O objetivo principal é realizar uma análise exploratória, limpeza e visualização de dados sobre a produção de combustível (Etanol Hidratado e Anidro) no Brasil entre 2019 e 2023.

## 📋 Informações do Aluno

* **Nome:** Cícero Rogério dos Santos Alves Filho
* **Matrícula:** 578748
* **Curso:** Ciência de Dados
* **Data:** 14 a 15/12/2025

## 🎯 Objetivos

O notebook investiga o dataset fornecido para cumprir três etapas principais de um pipeline de Ciência de Dados:

1. **Identificação:** Detecção de problemas de qualidade de dados (valores ausentes, duplicatas, *outliers* e inconsistências de formatação).
2. **Tratamento:** Limpeza e padronização dos dados para garantir a integridade da análise.
3. **Visualização e Análise:** Geração de *insights* sobre a evolução da produção e o desempenho dos estados brasileiros.

## 🗂️ Sobre os Dados

* **Fonte:** [ap2-combustivel-producao.csv](https://raw.githubusercontent.com/ccalmendra/ciencia-dados/refs/heads/main/dados/ap2-combustivel-producao.csv)
* **Período Analisado:** 2019 a 2023 (parcial)
* **Variáveis Principais:**
* `Mês/Ano`: Data da produção.
* `Região` e `Estado`: Localização geográfica.
* `Produção Etanol Hidratado (m³/d)`: Combustível utilizado diretamente em veículos.
* `Produção Etanol Anidro (m³/d)`: Combustível utilizado como aditivo na gasolina.



## 🛠️ Metodologia Aplicada

### 1. Identificação e Diagnóstico

Foram detectados diversos problemas na base original:

* **Inconsistência Temporal:** Múltiplos formatos de data (ex: `MM/AAAA`, `AAAA-MM`, `MM/AA` e erros de digitação).
* **Inconsistência Categórica:** Variações na grafia dos estados (ex: `GO` vs `Goiás`, falta de acentuação).
* **Outliers:** Identificação de *outliers* naturais (grande escala de produção em SP) e *outliers* de erro (um registro impossível de ~10 milhões de  em MG).
* **Valores Nulos:** Lacunas na produção e na definição de regiões.

### 2. Tratamento de Dados

As seguintes correções foram implementadas:

* **Padronização de Datas:** Criação de função personalizada para unificar todas as datas no formato `datetime`.
* **Correção de Estados e Regiões:** Unificação de nomes (siglas  nomes completos) e preenchimento de regiões faltantes via mapeamento.
* **Correção de Outlier Crítico:** Substituição do valor errôneo de Minas Gerais pela mediana do estado.
* **Limpeza:** Remoção de duplicatas exatas e lógicas.

### 3. Principais Resultados

* **Liderança Absoluta:** O estado de **São Paulo** manteve-se como o maior produtor nacional de ambos os tipos de etanol durante todo o período analisado.
* **Consistência:** Não houve alternância na liderança do ranking nacional, evidenciando a infraestrutura superior do complexo sucroalcooleiro paulista.
* **Análise de Crise:** Identificação de estados que zeraram a produção ou operaram abaixo do desvio padrão em momentos específicos (fenômeno regionalizado).

## 🚀 Como Executar

### Pré-requisitos

Certifique-se de ter as seguintes bibliotecas Python instaladas:

```python
pandas
numpy
matplotlib
seaborn

```

### Instalação

Você pode instalar as dependências via pip:

```bash
pip install pandas numpy matplotlib seaborn

```

### Execução

1. Clone este repositório ou baixe o arquivo `Projeto_combustiveis.ipynb`.
2. Abra o arquivo utilizando o Jupyter Notebook, Jupyter Lab ou Google Colab.
3. Execute todas as células sequencialmente para reproduzir a análise e os gráficos.

---

*Projeto acadêmico desenvolvido para fins avaliativos.*
