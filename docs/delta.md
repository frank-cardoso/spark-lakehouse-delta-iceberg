# Delta Lake

## O que e o Delta Lake
O **Delta Lake** e um formato de tabela que adiciona confiabilidade transacional a um Data Lake. Ele registra operacoes em um **log transacional**, permitindo controle de versoes, validacao de schema e leitura consistente dos dados.

## Transacoes ACID
O Delta Lake garante **ACID** por meio do log transacional. Cada escrita gera um commit atomico com metadados do estado da tabela. Isso assegura:
- **Atomicidade:** a atualizacao so e visivel apos o commit completo.
- **Consistencia:** validacao de schema e metadados evita estados invalidos.
- **Isolamento:** leitores veem uma versao estavel dos dados.
- **Durabilidade:** o historico de versoes fica persistido no log.

## Time Travel
O **Time Travel** permite consultar versoes antigas usando numero de versao ou timestamp. O mecanismo reconstrui o estado da tabela ao ler o log ate a versao desejada, garantindo reproducibilidade e auditoria.

### Evidência Prática
![Execução do Delta Lake](assets/delta_lab.png)