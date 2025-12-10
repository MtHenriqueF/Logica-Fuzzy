# Sistema de Inferência Fuzzy para Avaliação de Risco Cardiovascular

![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?logo=python&logoColor=white)
![Colab](https://img.shields.io/badge/Colab-F9AB00?logo=google-colab&logoColor=white)
![Scikit-Fuzzy](https://img.shields.io/badge/Library-Scikit--Fuzzy-orange)
![Status](https://img.shields.io/badge/Status-Completed-green)

Este projeto implementa um **Sistema de Inferência Fuzzy (Mamdani)** para auxiliar na estratificação do risco cardiovascular. O sistema processa três variáveis de entrada clínicas (IMC, Glicemia e Colesterol Total) para determinar uma pontuação percentual de risco, utilizando curvas gaussianas matematicamente ajustadas para garantir transições suaves e coerentes.

## 📋 Funcionalidades

* **Modelagem Matemática Precisa:** Cálculo automatizado do desvio padrão ($\sigma$) das gaussianas para garantir interseções exatas em $\mu = 0.3$ nas fronteiras das classes.
* **Tratamento de Bordas (Shoulders):** Implementação de funções sigmoidais (platôs) para limites superiores abertos (ex: Obesidade Grau III, Diabetes, Colesterol Alto).
* **Base de Regras Complexa:** Integração de 45 regras lógicas distribuídas em 3 tabelas de decisão médica.
* **Visualização Avançada:**
    * Gráficos das Funções de Pertinência.
    * Superfícies de Decisão 3D (Slicing).
    * Mapas de Calor (Heatmaps) para análise de sensibilidade.
* **Relatório Consolidado:** Geração automática de tabela de resultados para uma população de teste.

## 🧮 Variáveis do Sistema

### Entradas (Antecedentes)
1.  **IMC ($kg/m^2$):** Peso Ideal, Sobrepeso, Obesidade I, Obesidade II, Obesidade III.
2.  **Glicemia em Jejum ($mg/dL$):** Normal, Pré-Diabetes, Diabetes.
3.  **Colesterol Total ($mg/dL$):** Desejável, Limítrofe, Alto.

### Saída (Consequente)
* **Risco Cardiovascular (%):** Baixo, Médio, Alto, Muito Alto, Extremo.

## 🛠️ Instalação e Requisitos

Para executar este projeto, você precisará das seguintes bibliotecas Python:

```bash
pip install numpy scikit-fuzzy matplotlib