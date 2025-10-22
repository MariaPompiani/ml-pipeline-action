# Projeto de Pipeline de Machine Learning com GitHub Actions

Este repositório contém um workflow automatizado que treina um modelo de Machine Learning e gera um relatório de classificação.

## Workflow: `ml.yml`

O fluxo de trabalho (`.github/workflows/ml.yml`) é acionado a cada `push` e realiza as seguintes tarefas:

1.  **Checkout**: Baixa o código-fonte e os dados.
2.  **Setup Python**: Prepara o ambiente Python.
3.  **Cache**: Utiliza o cache de dependências para acelerar a instalação de bibliotecas como `pandas` e `scikit-learn`.
4.  **Install Dependencies**: Instala as bibliotecas necessárias.
5.  **Run Training**: Executa o script `train.py`, que treina um modelo de regressão logística.
6.  **Upload Artifact**: Salva o `report.txt` gerado como um artefato no GitHub, permitindo que a performance do modelo seja auditada a qualquer momento.
