# modelagem2
Esse código foi feito após o outro projeto, achei que talvez pudesse estar desorganizado ou confuso de entender, então decidi fazer esse que seria uma versão "resumida" ou mais achata que acabamos chegando em resultados parecidos. Nela também contem o teste de hipotese. 


1. Introdução e ObjetivosEste projeto foi desenvolvido como requisito para a disciplina de Estatística Aplicada, com o objetivo de demonstrar habilidades em Análise Exploratória de Dados (EDA), Modelagem Preditiva (Regressão e Classificação) e Otimização de Modelos utilizando Python.
2. Variáveis-Alvo
3. O projeto aborda dois problemas distintos usando o mesmo conjunto de dados:
4. Regressão: Previsão da pontuação média de um jogador por jogo (PTS - Points).
5. Classificação: Previsão da probabilidade de um jogador ser um High Performer (top 5% em pontuação na nossa definição de Target).
6. 2. Fonte de Dados e Licença
   3. Fonte: Dados de estatísticas de jogadores da NBA (1946 a 2020) obtidos através do Kaggle.
   4. Nome do Dataset: NBA Players Stats from 1946 to 2020
   5. URL: https://www.kaggle.com/datasets/drgilermo/nba-players-stats
   6. Licença: O conjunto de dados é geralmente distribuído sob a Licença de Banco de Dados Comunitário (CC0: Public Domain) do Kaggle, que permite o uso e compartilhamento para qualquer finalidade.
   7. Estrutura do Repositório
   8. nba-stats-project/
├── data/
│   ├── Players.csv
│   ├── player_data.csv
│   └── Seasons_Stats.csv
├── project_report.ipynb  <-- Relatório Principal e Código Completo
├── README.md             <-- Este arquivo
└── requirements.txt      <-- Dependências do projeto
7. Instruções de InstalaçãoPara replicar a análise e os modelos, siga os passos abaixo.
  4.1. 🐍 Requisitos de SoftwareVocê precisará ter o Python (3.8+) e o pip instalados no seu sistema. É altamente recomendado o uso de um ambiente virtual (ex: venv ou conda).
  4.2. 📦 Instalação de DependênciasTodas as bibliotecas necessárias estão listadas no arquivo requirements.txt. Instale-as usando o seguinte comando:
   Bashpip install -r requirements.txt
Principais Ferramentas Obrigatórias:
Biblioteca                           Propósito
pandas, numpy                  Manipulação de Dados
seaborn, matplotlib            Visualização e EDA
statsmodels                    Regressão Linear para Interpretação (p-valores, coeficientes)
sklearn                        Modelagem, Métricas e Otimização (GridSearch)
pycaret                        Comparação e Tuning Automático (Validação Cruzada)
4.3. 💾 DadosOs arquivos CSV (Players.csv, player_data.csv, Seasons_Stats.csv) devem ser colocados no subdiretório ./data/ ou baixados diretamente para o diretório raiz do projeto. O notebook project_report.ipynb espera que os dados estejam disponíveis para leitura.
   5. Instruções de ExecuçãoO projeto completo está contido no arquivo project_report.ipynb. Iniciar o Jupyter Notebook:Bashjupyter notebook
Abrir o Notebook: Abra o arquivo project_report.ipynb no seu navegador.Executar Células: Execute as células sequencialmente. O notebook está estruturado em seções claras:
Seção 1: Leitura, Junção (Merge) e EDA.
Seção 2: Modelagem de Regressão (Simples, Múltipla, Polinomial).
Seção 3: Otimização de Regressão (Pycaret).
Seção 4: Modelagem de Classificação (Naive Bayes, Regressão Logística).
Seção 5: Otimização de Classificação (Pycaret e Sklearn GridSearch).
Seção 6: Conclusões e Análise Crítica.
6. Conclusões e Próximos Passos (Resumo Executivo)
   O projeto demonstrou que:Regressão: Variáveis como MP (Minutos Jogados) e % de Arremessos são os preditores mais fortes de PTS. O modelo de Regressão Polinomial e a otimização com Pycaret resultaram em melhorias significativas no $R^2$ em comparação ao modelo Linear Múltiplo simples.
   Classificação: Devido ao desbalanceamento da classe, a métrica AUC-ROC foi crucial. O modelo de Regressão Logística otimizado via GridSearchCV apresentou um excelente poder preditivo para identificar High Performers com base nas suas estatísticas.
