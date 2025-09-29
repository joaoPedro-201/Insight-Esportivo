# Projeto Insight Esportivo ⚽️

Um analisador de estatísticas esportivas automatizado, focado em encontrar valor em apostas recreativas através de modelos matemáticos. Este projeto nasceu da paixão por esportes e tecnologia, com o objetivo de transformar intuição em decisões baseadas em dados.

## 📖 Sobre o Projeto

O objetivo principal do **Insight Esportivo** é coletar, processar e analisar dados de partidas de futebol (e futuramente outros esportes) para gerar probabilidades estatísticas para resultados de jogos. Em vez de depender de "achismos", este programa utiliza dados históricos, forma recente das equipes e modelos como a Distribuição de Poisson para prever os resultados mais prováveis.

Este é um projeto de portfólio para demonstrar habilidades em:
* Coleta de dados via APIs (API Consumption)
* Armazenamento e modelagem de dados (SQL com SQLite)
* Análise de dados e modelagem estatística (Python, Pandas)
* Automação de tarefas
* Desenvolvimento de software em geral

---

## ✨ Funcionalidades Principais

* **Coleta Automatizada:** Busca dados de jogos, times e ligas de uma API de esportes.
* **Armazenamento Persistente:** Salva todos os dados coletados em um banco de dados SQLite para análises futuras.
* **Análise Estatística:** Calcula métricas essenciais como:
    * Média de gols marcados/sofridos (em casa e fora)
    * Análise de confrontos diretos (Head-to-Head)
    * Forma recente das equipes (últimos 5 jogos)
* **Modelo Preditivo:** Utiliza a Distribuição de Poisson para calcular a probabilidade de resultados exatos (ex: 1x0, 2x1) e de resultados gerais (Vitória Time A, Empate, Vitória Time B).
* **Interface Simples:** Exibe as análises de forma clara através de uma interface de linha de comando (CLI).

---

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python 3
* **Análise de Dados:**
    * Pandas
    * NumPy
* **Comunicação com API:**
    * Requests
* **Banco de Dados:**
    * SQLite
    * SQLAlchemy
* **Gerenciamento de Dependências:**
    * Pip

---

## 🚀 Como Começar

Para executar este projeto localmente, siga os passos abaixo.

### Pré-requisitos

* Python 3.8 ou superior
* Git
* Uma chave de API de um provedor de dados esportivos (ex: [API-FOOTBALL](https://www.api-football.com/))

### Instalação

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/](https://github.com/)[SEU_USUARIO_GITHUB]/insight-esportivo.git
    cd insight-esportivo
    ```

2.  **Crie e ative um ambiente virtual:**
    ```bash
    # Para Windows
    python -m venv venv
    .\venv\Scripts\activate

    # Para macOS/Linux
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Instale as dependências:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Configure suas variáveis de ambiente:**
    * Renomeie o arquivo `.env.example` para `.env`.
    * Abra o arquivo `.env` e insira sua chave da API:
        ```ini
        API_KEY="SUA_CHAVE_SECRETA_DA_API_AQUI"
        ```

---

## 💻 Como Usar

O projeto é dividido em dois scripts principais:

1.  **Coletor de Dados (`collector.py`):**
    * Execute este script para buscar novos dados da API e salvá-los no banco de dados local.
    ```bash
    python collector.py --liga "Brasileirão Série A"
    ```

2.  **Analisador (`analyzer.py`):**
    * Execute este script para analisar uma partida usando os dados já armazenados localmente.
    ```bash
    python analyzer.py --timeA "Flamengo" --timeB "Palmeiras"
    ```
    A saída esperada será algo como:

    ```
    =============================================
      Análise de Jogo: Flamengo vs. Palmeiras
    =============================================

    Probabilidades Calculadas:
    --------------------------
    Vitória do Flamengo:  48.5%
    Empate:               25.3%
    Vitória do Palmeiras: 26.2%

    Sugestão de Valor:
    --------------------------
    Com base nas probabilidades calculadas, o resultado mais provável é a vitória do Flamengo.
    ```

---

## 🗺️ Roadmap do Projeto

-   [ ] Desenvolver uma interface web simples com Flask ou FastAPI para visualizar as análises.
-   [ ] Expandir para outros esportes, como Basquete (NBA).
-   [ ] Criar um bot para Telegram ou Discord que envie notificações de jogos com alto potencial de valor.
-   [ ] Aprimorar o modelo estatístico, incluindo mais variáveis (escalações, lesões, etc.).
-   [ ] Implementar um sistema de agendamento (scheduler) para executar a coleta de dados diariamente de forma automática.

---

## 📜 Licença

Distribuído sob a licença MIT. Veja `LICENSE` para mais informações.
