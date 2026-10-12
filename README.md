# 📊 Laboratório: Transformando Dados em Decisões — Análise de Vendas

![Status](https://img.shields.io/badge/Status-Concluído-success)
![Ferramentas](https://img.shields.io/badge/Ferramentas-Power_BI_|_Python_|_Pandas-blue)

## 📌 Sobre o Projeto
Este projeto foi desenvolvido como parte de um laboratório prático de Análise de Dados. O objetivo principal foi atuar como um Analista de Dados para explorar uma base de vendas (`base_vendas_voluntarios.csv`), tratar inconsistências, extrair métricas de negócio (KPIs) e desenvolver um dashboard interativo para facilitar a tomada de decisão.

Embora o desafio original propusesse o uso do Excel, o projeto foi elevado para um nível profissional utilizando **Python (Jupyter Notebook)** para a Análise Exploratória de Dados (EDA) avançada e **Power BI** para a construção do Dashboard Executivo final.

---

## 🎯 Objetivos (Missões do Laboratório)

- **Missão 1: Preparação de Dados:** Explorar a base, tratar dados e criar a coluna `Valor Total` (somando `Preço` + `Frete`) para refletir o faturamento real.
- **Missão 2: Análise e Respostas:** Descobrir os melhores estados, produtos mais vendidos, categorias com maior receita e piores avaliações.
- **Missão 3: Dashboard Executivo:** Consolidar as análises em um painel visual escuro (Dark Theme) com alto contraste e interatividade.

---

## 🛠️ Tecnologias e Ferramentas Utilizadas

*   **Power BI:** Construção do dashboard, modelagem de dados (Power Query) e criação de métricas (DAX).
*   **Python (Jupyter Notebook):** Limpeza inicial e análises estatísticas.
*   **Bibliotecas Python:** `pandas` (manipulação de dados), `matplotlib` e `seaborn` (visualização de dados e boxplots).

---

## 📈 O Dashboard Final
O painel foi construído no Power BI com foco em UI/UX para facilitar a leitura por gestores. 

**KPIs Monitorados:**
*   **Faturamento Total:** R$ 739,96 Mil
*   **Total de Vendas:** 2 Mil pedidos
*   **Ticket Médio:** R$ 313,68
*   **Avaliação Média:** 3,98 / 5,00

**Visualizações:**
1.  Faturamento por Categoria (Barras horizontais)
2.  Total de Vendas por Local/Estado (Gráfico de colunas)
3.  Total de Vendas por Tipo de Pagamento (Gráfico de rosca)
4.  Total de Vendas por Mês (Análise de sazonalidade)

---

## 💡 Principais Insights e Decisões Técnicas

Durante o desenvolvimento, algumas decisões analíticas foram cruciais para garantir a veracidade das informações:

1.  **Correção do Faturamento:** O dataset separava o "Preço" do "Frete". Foi realizada uma engenharia de atributos (Feature Engineering) para somar ambos no `Valor Total`, corrigindo subnotificações nas métricas da empresa.
2.  **Escala de Dados Ajustada:** Problemas de importação de CSV (pontos vs. vírgulas) geraram métricas irreais na casa dos Bilhões/Trilhões. O problema foi tratado na raiz via Power Query e cálculos DAX.
3.  **Tratamento de Viés Temporal:** O gráfico de linhas anual exibia uma "queda falsa" em 2023, pois o ano continha apenas dados até março. O eixo temporal foi ajustado para **Meses**, revelando a verdadeira sazonalidade de vendas (com picos claros em Março e Setembro).

### 🚀 Desafio Extra: O Frete afeta a avaliação?
Através de uma análise bivariada utilizando gráficos de *Boxplot* em Python, testou-se a hipótese de que o valor alto do frete gerava insatisfação (notas 1 e 2). 
**A descoberta:** Não há correlação. Clientes que pagaram fretes altíssimos (acima de R$ 150) também deram nota máxima (5). Isso indica à empresa que as avaliações ruins derivam de outros fatores (como qualidade do produto ou atraso logístico), e não do preço do transporte.

---

## ⚙️ Como executar o projeto

1.  Faça o clone deste repositório: `git clone https://github.com/seu-usuario/seu-repositorio.git`
2.  Para ver a análise em código: Abra o arquivo `.ipynb` utilizando o Jupyter Notebook, VS Code ou Google Colab.
3.  Para ver o painel interativo: Abra o arquivo `.pbix` utilizando o Microsoft Power BI Desktop.
