# Trabalho: Apache Spark com Delta Lake e Apache Iceberg

**Disciplina:** Arquitetura de Dados - UniSatc  
**Professor:** Jorge Silva  

## Grupo
- Frank Cardoso
- Gustavo Nunes

## Descrição
Projeto desenvolvido para demonstração do Apache Spark (PySpark) executando operações transacionais (ACID) em tabelas nos formatos **Delta Lake** e **Apache Iceberg**. 

O projeto foi atualizado para uma **Arquitetura Universal baseada em Docker**, eliminando a necessidade de configurações manuais de Java, Hadoop ou Winutils no sistema operacional hospedeiro.

👉 **Documentação Oficial (Evidências):** [Acessar o site do projeto](https://frank-cardoso.github.io/spark-lakehouse-delta-iceberg/)

## 🛠️ Setup e Ambiente (Dev Container)
Para garantir a portabilidade entre **Windows 11, Linux e macOS**, este projeto utiliza **VS Code Dev Containers**. Toda a infraestrutura (Java 17, Spark 3.5.1 e Python 3.11) é isolada automaticamente em um container.

### Requisitos
* [Docker Desktop](https://www.docker.com/products/docker-desktop/) (Com suporte a WSL 2 ativado).
* [VS Code](https://code.visualstudio.com/) com a extensão **Dev Containers** instalada.
* **Virtualização (VT-x/AMD-V)** ativada na BIOS/UEFI do computador.

### Como Executar
1. Certifique-se de que o **Docker Desktop** está rodando.
2. Abra a pasta do projeto no VS Code.
3. Quando solicitado (ou via `Ctrl+Shift+P` -> `Dev Containers: Reopen in Container`), aceite a abertura no ambiente isolado.
4. O VS Code construirá a imagem e instalará as dependências (`pyspark`, `delta-spark`, `ipykernel`) automaticamente.
5. Selecione o kernel **Python 3.11 (base)** dentro do container para rodar os notebooks.

## 🧪 Laboratórios
Os exemplos de código para instanciar os motores e manipular as tabelas (INSERT, UPDATE e DELETE) estão em:
* `notebooks/delta_lab.ipynb`
* `notebooks/iceberg_lab.ipynb`

**Nota:** Os caminhos de dados foram universalizados para `/home/jovyan/work/spark-warehouse`, garantindo que o projeto funcione sem alterações em qualquer máquina (removendo a dependência de caminhos `C:\` e `winutils.exe`).

## 📚 Documentação (MkDocs)
Toda a fundamentação teórica e as evidências práticas foram documentadas utilizando o framework MkDocs. 

**Para testar o site localmente (dentro do container):**
```bash
python -m pip install mkdocs-material
mkdocs serve

*(O site ficará disponível em [http://127.0.0.1:8000](http://127.0.0.1:8000))*

## Referências
* [Delta Lake Quickstart](https://docs.delta.io/latest/quick-start.html)
* [Apache Iceberg Spark Quickstart](https://iceberg.apache.org/spark-quickstart/)
* [MkDocs Material](https://squidfunk.github.io/mkdocs-material/)