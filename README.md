# 📊 Análise de Vendas de E-commerce

Projeto de portfólio em **Análise de Dados** utilizando Python. O objetivo é
simular o dia a dia de um analista de dados: limpar uma base "suja", explorar
os dados, gerar visualizações e extrair insights de negócio.

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.x-yellow)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)

## 🎯 Objetivo

Uma empresa fictícia de e-commerce registrou seus pedidos de 2024, mas a base
possui problemas comuns do mundo real: duplicatas, valores nulos, textos
inconsistentes e erros de digitação. O projeto responde perguntas como:

- Quais categorias de produto geram mais receita?
- Como a receita evolui ao longo do ano (sazonalidade)?
- Quais regiões e canais de venda performam melhor?
- Qual o ticket médio por segmento de cliente?
- Como está a satisfação dos clientes (avaliações)?

## 🗂️ Estrutura do repositório

```
projeto-analise-vendas/
├── data/
│   └── vendas_ecommerce.csv       # dataset (sintético, gerado programaticamente)
├── notebooks/
│   └── analise_vendas.ipynb       # notebook completo: limpeza + EDA + gráficos
├── images/                        # gráficos exportados em PNG
├── src/
│   ├── gerar_dados.py             # script que gera o dataset sintético
│   └── build_notebook.py          # script que monta o notebook
├── requirements.txt
└── README.md
```

## 🧹 Etapas do projeto

1. **Geração/ingestão dos dados** — dataset simulado com 6.000+ pedidos
   (categoria, preço, quantidade, desconto, região, segmento de cliente,
   canal de venda, avaliação).
2. **Limpeza de dados**
   - Remoção de linhas duplicadas
   - Padronização de texto (categorias com maiúsculas/espaços)
   - Tratamento de valores nulos (preço preenchido pela mediana da categoria,
     região marcada como "Não Informado")
   - Correção de valores inconsistentes (quantidades negativas)
   - Criação de colunas derivadas (receita, mês, dia da semana)
3. **Análise exploratória (EDA)** com `pandas`
4. **Visualização de dados** com `matplotlib` e `seaborn`
5. **Insights de negócio** documentados ao final do notebook

## 📈 Principais gráficos gerados

| Receita por categoria | Evolução mensal da receita |
|---|---|
| ![categoria](images/receita_por_categoria.png) | ![mensal](images/receita_mensal.png) |

| Receita por região | Ticket médio (segmento x canal) |
|---|---|
| ![regiao](images/receita_por_regiao.png) | ![heatmap](images/ticket_medio_heatmap.png) |

## 🛠️ Tecnologias utilizadas

- **Python 3**
- **Pandas** e **NumPy** — manipulação e limpeza de dados
- **Matplotlib** e **Seaborn** — visualização de dados
- **Jupyter Notebook** — desenvolvimento e storytelling

## ▶️ Como executar o projeto

```bash
# 1. Clonar o repositório
git clone https://github.com/SEU-USUARIO/projeto-analise-vendas.git
cd projeto-analise-vendas

# 2. Criar ambiente virtual (opcional, mas recomendado)
python3 -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

# 3. Instalar dependências
pip install -r requirements.txt

# 4. (Opcional) Gerar novamente o dataset sintético
python3 src/gerar_dados.py

# 5. Abrir o notebook
jupyter notebook notebooks/analise_vendas.ipynb
```

## 💡 Próximos passos (ideias de evolução)

- Adicionar um dashboard interativo (Streamlit ou Power BI)
- Criar consultas SQL para as mesmas análises
- Testar modelos preditivos de receita (ex.: regressão)
- Automatizar a atualização dos dados com um pipeline

## 👤 Autor

Sinta-se à vontade para adaptar este projeto com seu nome, LinkedIn e demais
links de contato.

---
*Projeto criado para fins de estudo e portfólio em Análise de Dados.*
