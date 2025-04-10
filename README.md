--Diagnóstico com XGBoost e Interpretação com SHAP

Este projeto utiliza o algoritmo de aprendizado de máquina XGBoost para prever a presença de uma doença rara com base em dados clínicos e demográficos de pacientes. Além disso, a biblioteca SHAP é utilizada para interpretar a importância e o impacto de cada variável nas previsões do modelo.

--Estrutura do Projeto

.
├── dados/                        # Pasta com os arquivos CSV originais
│   ├── diagnostics_*.csv
│   ├── patients_*.csv
│   ├── treatments_*.csv
│   ├── hospitalizations_*.csv
│   └── comorbidities_*.csv
├── teste1.py                    # Script principal do projeto
└── README.md                    # Este arquivo

-- Requisitos

Instale os pacotes necessários com:

pip install pandas numpy matplotlib seaborn xgboost shap scikit-learn

-- Como Executar

Certifique-se de que todos os arquivos .csv estejam na pasta dados/ conforme esperado.

Altere o caminho da variável caminho no início do script teste1.py, se necessário.

Execute o script:

python teste1.py

-- O que o Script Faz

Carrega e padroniza os dados de diversas fontes (diagnósticos, pacientes, comorbidades, etc.).

Realiza a junção dos dados em um único DataFrame com base no record_id.

Seleciona variáveis clínicas e demográficas relevantes para análise.

Codifica variáveis categóricas com LabelEncoder.

Treina um modelo XGBoost para prever o status de doença rara (status_doenca_rara).

Avalia o desempenho do modelo com acurácia e relatório de classificação.

Interpreta o modelo com SHAP, gerando:

Gráfico de importância global das variáveis.

Gráficos de dependência individual por variável.

--Variável Alvo

A variável alvo é:

status_doenca_rara

Ela representa se o paciente possui ou não uma doença rara (codificada como 0 ou 1).

--Observações

O modelo pode ser ajustado para lidar com desbalanceamento de classes, hiperparâmetros, etc.

As visualizações SHAP permitem interpretar como cada variável contribuiu para a previsão em cada paciente.

Certifique-se de que os dados estejam limpos e bem estruturados para melhor performance do modelo.

--Contato

Para dúvidas, sugestões ou colaborações, entre em contato com Leandro Lima Leite
