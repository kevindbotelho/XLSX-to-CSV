# Conversão de Arquivos XLSX para CSV com UTF-8

Este projeto tem como objetivo converter arquivos Excel (XLSX) para CSV com codificação UTF-8, facilitando a importação dos arquivos para o Google BigQuery. Muitas vezes, ao salvar diretamente do Excel, os arquivos CSV acabam com a codificação ISO-8859-1, o que pode causar problemas com caracteres especiais. Esta solução usa Python e Pandas para automatizar a conversão, garantindo a codificação UTF-8.

## Funcionalidade

- Converte arquivos XLSX para CSV.
- Todos os arquivos são salvos diretamente com a codificação UTF-8, evitando problemas de caracteres especiais no BigQuery.
- Automatiza a conversão de vários arquivos XLSX de uma vez.
