# Apache Iceberg

## O que e o Apache Iceberg
O **Apache Iceberg** e um formato de tabela para Data Lakes que organiza dados e metadados de forma estruturada. Ele foi criado para escalar em ambientes distribuidos, mantendo consultas consistentes e facilitando a evolucao do schema.

## Metadados e organizacao do Data Lake
O Iceberg usa metadados para evitar a necessidade de listar todos os arquivos em cada consulta. A estrutura inclui:
- **Metadata file:** descreve a tabela e aponta para o snapshot atual.
- **Manifest list:** lista os manifest files de um snapshot.
- **Manifest files:** descrevem os data files e suas estatisticas.

Essa organizacao melhora desempenho, facilita manutencao e permite evoluir particionamento sem reescrever dados.

[COLAR PRINTS DO ICEBERG AQUI]
