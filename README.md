# Classificação de risco de ótitos por Covid-19

Este código refere-se a uma análise de Machine Learning para o Trabalho de Conclusão de Curso (TCC) que teve como título: Uso de Machine Learning para classificação de risco de óbitos por covid-19 no estado de Mato Grosso. O TCC completo pode ser encontrado em [Biblioteca Digital da Universidade Estadual da Paraíba ](https://dspace.bc.uepb.edu.br/jspui/handle/123456789/29113).

O modelo óbtido para classificar o risco de óbito por covid-19 considerou a seguintes variáveis:

| Variável          | Categoria                         | Tipo     |
|-------------------|-----------------------------------|----------|
| Situação          | 0 - recuperado, 1 - óbito         | Numérica |
| Idade             | Variável Numérica                  | Numérica |
| Sexo              | 1 - Masculino, 0 - Feminino        | Categórica |
| ProfissionalSaude | 1 - Sim, 0 - Não                   | Categórica |
| Comorbidade       | 1 - Sim, 0 - Não                   | Categórica |
| Cardiovascular    | 1 - Sim, 0 - Não                   | Categórica |
| Diabetes          | 1 - Sim, 0 - Não                   | Categórica |
| Hipertensão       | 1 - Sim, 0 - Não                   | Categórica |
| Neoplasia         | 1 - Sim, 0 - Não                   | Categórica |
| Obesidade         | 1 - Sim, 0 - Não                   | Categórica |
| Pulmonar          | 1 - Sim, 0 - Não                   | Categórica |
| Gestante          | 1 - Sim, 0 - Não                   | Categórica |


O resultados da análise de Machine Learning foram os seguintes:

| Algoritmo            | AUC    | VP     | FP     | Acurácia |
|----------------------|--------|--------|--------|----------|
| Regressão Logística  | 0.806  | 0.798  | 0.186  | 0.813    |
| Random Forest        | 0.799  | 0.808  | 0.209  | 0.791    |
| XGBoost              | 0.803  | 0.816  | 0.211  | 0.790    |
| LightGBM             | 0.804  | 0.810  | 0.202  | 0.798    |
| CatBoost             | 0.805  | 0.807  | 0.197  | 0.802    |

Foi obtido um modelo capaz de classificar corretamente o desfecho da doença em 80% dos casos, baseando-se em informações que podem ser coletadas do paciente no momento em que o mesmo der entrada no unidade de atendimento.

**Observação:** Durante o desenvolvimento do TCC, apliquei transformação nos dados antes da divisão treino/teste, o que caracteriza um vazamento de dados. Posteriormente, identifiquei esse ponto e corrigi em projetos seguintes, utilizando Pipelines para evitar esse tipo de falha.
