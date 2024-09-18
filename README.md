

# Regressão Linear com Flask

Este projeto é uma aplicação web simples usando Flask para prever o preço de casas com base em seu tamanho, utilizando um modelo de regressão linear treinado com dados reais.

## Requisitos

Antes de começar, você precisará ter os seguintes pacotes Python instalados:

- `flask`
- `pandas`
- `scikit-learn`

Você pode instalar os pacotes necessários usando o seguinte comando:

```bash
pip install flask pandas scikit-learn
```

## Estrutura do Projeto

A estrutura do projeto é simples:

```
/project-root
    ├── app.py
    └── README.md
```

- `app.py`: Contém o código da aplicação Flask que treina o modelo de regressão linear e expõe as rotas para previsões.

## Como Executar

1. **Clone o repositório:**

    ```bash
    git clone <URL_DO_REPOSITORIO>
    cd <DIRETORIO_DO_PROJETO>
    ```

2. **Instale as dependências:**

    ```bash
    pip install -r requirements.txt
    ```

3. **Execute a aplicação Flask:**

    ```bash
    python app.py
    ```

4. **Acesse a aplicação:**

    Abra seu navegador e acesse `http://127.0.0.1:5000/`.

## Endpoints

A aplicação possui dois endpoints para calcular o preço da casa:

1. **Endpoint básico:**

    - **URL:** `/preco/`
    - **Método:** GET
    - **Parâmetro:** `tamanho` (o tamanho da casa em metros quadrados)
    - **Descrição:** Retorna o preço da casa com base no tamanho fornecido.

    Exemplo de uso:
    
    ```
    http://127.0.0.1:5000/preco/?tamanho=120
    ```

    Resposta:
    
    ```
    O preço da casa é: 300000.0
    ```

2. **Endpoint avançado:**

    - **URL:** `/preco-avancado/`
    - **Método:** GET
    - **Parâmetro:** `tamanho` (o tamanho da casa em metros quadrados)
    - **Descrição:** Retorna o preço da casa com base no tamanho fornecido.

    Exemplo de uso:
    
    ```
    http://127.0.0.1:5000/preco-avancado/?tamanho=120
    ```

    Resposta:
    
    ```
    O preço da casa é: 300000.0
    ```

## Descrição do Código

- **Importação de bibliotecas:** Importa Flask, pandas e scikit-learn.
- **Leitura de dados:** Carrega um conjunto de dados de casas do GitHub.
- **Preparação dos dados:** Separa os dados em recursos (tamanho) e alvo (preço) e divide em conjuntos de treino e teste.
- **Treinamento do modelo:** Cria e treina um modelo de regressão linear.
- **Endpoints Flask:** Define dois endpoints para prever o preço da casa com base no tamanho fornecido.

