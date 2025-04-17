# 📊 ETL de Notebooks/Smartphone do Mercado Livre

Este projeto realiza uma pipeline ETL completa com dados de notebooks do Mercado Livre usando Scrapy e Pandas.

---

## 🔄 Etapas

### 1. Extração
- Feita com o framework [Scrapy](https://scrapy.org/).
- Coleta informações de até 10 páginas com notebooks, incluindo:
  - Marca
  - Nome
  - Preço antigo e novo
  - Avaliação
  - Quantidade de avaliações
  - Vendedor

### 2. Transformação
- Limpeza dos dados: remoção de parênteses, espaços e conversão de colunas numéricas.
- Renomeação de colunas para português.
- Agrupamento por marca e tipo para gerar métricas agregadas.

### 3. Carga
- Exportação dos dados limpos para `.csv` e `.xlsx`.
- Análises podem ser visualizadas no notebook `etl_pipeline.ipynb`.
- Salvando os dados em um banco SQLite
--Após realizar a coleta e tratamento dos dados, você pode armazená-los em um banco de dados SQLite utilizando o pandas com SQLAlchemy. Isso facilita análises futuras, integrações e consultas SQL.

---

## 🧰 Tecnologias

- Python 3.13+
- Scrapy
- Pandas
- Jupyter Notebook

---

## 🚀 Como executar

### 1. Clone o projeto
```bash
git clone https://github.com/seu-usuario/notebook-etl-mercado-livre.git
cd notebook-etl-mercado-livre
```

### 2. Instale os pacotes
```bash
pip install -r requirements.txt
```

### 3. Rode o spider
```bash
cd scrapy_project
scrapy crawl notebook -o ../data/raw/notebooks_raw.json
```

### 4. Transforme os dados
Abra o notebook `notebooks/etl_pipeline.ipynb` e execute as células.

---

## ✍️ Autor
André Rodrigues – [linkedin.com/in/andrehrsilva](https://linkedin.com/in/andrehrsilva)
