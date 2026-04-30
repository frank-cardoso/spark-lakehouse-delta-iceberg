# Trabalho: Apache Spark com Delta Lake e Apache Iceberg

**Disciplina:** Arquitetura de Dados - UniSatc  
**Professor:** Jorge Silva  

## Grupo
- Frank Cardoso
- Gustavo Nunes

## Descrição
Projeto desenvolvido para demonstração do Apache Spark Local (PySpark) executando operações transacionais (ACID) em tabelas nos formatos **Delta Lake** e **Apache Iceberg** de forma local.

👉 **Documentação Oficial (Evidências):** [Acessar o site do projeto](https://frank-cardoso.github.io/spark-lakehouse-delta-iceberg/)

## Setup e Ambiente
Para este laboratório foi utilizado o **Windows 11**, mas o projeto é totalmente compatível com ambientes **Linux/WSL**. O projeto Python foi inicializado com o **Poetry** para isolamento de dependências e configuração do ambiente, garantindo a compatibilidade do PySpark 3.5.0 com o Python 3.11.

Comandos utilizados para setup do ambiente:
```powershell
python -m pip install --user poetry
python -m poetry install
```

Os exemplos de código PySpark para instanciar o motor e manipular as tabelas (INSERT, UPDATE e DELETE) estão nos arquivos:
* `notebooks/delta_lab.ipynb`
* `notebooks/iceberg_lab.ipynb`

**Nota 1:** Antes de executar os arquivos citados acima, não esqueça de selecionar o seu ambiente virtual criado pelo Poetry como Kernel do seu Jupyter Notebook.

**Nota 2:** Os arquivos `.ipynb` foram executados dentro do VS Code. Diferente do Linux/WSL, a execução no Windows exige o `winutils`, que já foi tratado via script direto nas primeiras células dos nossos notebooks.

## Referências
* [Delta Lake Quickstart](https://docs.delta.io/latest/quick-start.html)
* [Apache Iceberg Spark Quickstart](https://iceberg.apache.org/spark-quickstart/)
* [MkDocs Material](https://squidfunk.github.io/mkdocs-material/)