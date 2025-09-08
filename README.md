# Análise Exploratória de Dados - PProductions

by Matheus Medrado Massena

Este projeto consiste em uma análise exploratória de dados (EDA) de um conjunto de filmes, com o objetivo de responder a perguntas específicas sobre bilheteria, notas no IMDb, gêneros e outros fatores que podem influenciar o desempenho de um filme.

## Objetivos

- Explorar e visualizar os principais fatores relacionados ao sucesso de um filme.
- Responder às seguintes questões:
  1. Qual filme recomendar para uma pessoa que você não conhece?
  2. Quais fatores estão relacionados com alta expectativa de faturamento?
  3. É possível inferir informações sobre o gênero de um filme a partir da coluna `Overview`?

### Instalação

Clone este repositório e acesse:

```bash
git clone https://github.com/MedradoM/LH_CD_MATHEUS_MEDRADO_MASSENA.git
cd LH_CD_Desafio_PProductions
```

### Criação do ambiente virtual e instalação das dependências

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

### Instalação das dependências:

```bash
pip install -r requirements.txt
```

### Como Executar:

```bash
cd notebooks/
jupyter notebook 01_EDA_PProductions.ipynb
```

Todos os gráficos e análises estarão disponíveis diretamente no notebook.

### Como Carregar o Modelo .pkl

Caso você queira testar o modelo salvo, basta rodar:

```python
import joblib

loaded_model = joblib.load("../models/imdb_rating_model.pkl")

exemplo = {
    'Released_Year': [1999],
    'Runtime': [199],
    'Meta_score': [80.0],
    'No_of_Votes': [1234567],
    'Gross_Revenue': [987654321],
    'Genre': ['Drama'],
    ...
}

exemplo_df = pd.DataFrame(exemplo)
exemplo_df_formatted = format_data(exemplo_df)

pred = loaded_model.predict(exemplo_df_formatted)

print("Previsão do modelo:", pred)
```

### Tecnologias Utilizadas

- Python 3.10.16

- Pandas

- Numpy

- Matplotlib

- Seaborn

- Scikit-learn

- Jupyter Notebook

### Licença

Este projeto é de uso acadêmico/educacional e não possui fins comerciais.
