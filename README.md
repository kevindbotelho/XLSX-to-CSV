Claro, vou simplificar e ajustar o texto para você copiar e colar diretamente no README:

---

# Conversão de Arquivos XLSX para CSV com UTF-8

Este projeto converte arquivos Excel (XLSX) para CSV com codificação UTF-8, facilitando a importação dos arquivos para o Google BigQuery e outras ferramentas que utilizam CSV. Muitas vezes, ao salvar diretamente do Excel, os arquivos CSV acabam com a codificação ISO-8859-1, o que pode causar problemas com caracteres especiais. Esta solução usa Python e Pandas para automatizar a conversão, garantindo a codificação UTF-8.

## Funcionalidade

- Converte arquivos XLSX para CSV.
- Todos os arquivos são salvos diretamente com a codificação UTF-8, evitando problemas de caracteres especiais no BigQuery e em qualquer outra ferramenta que trabalhe com CSV.
- Automatiza a conversão de vários arquivos XLSX de uma vez.

## Como usar

1. Coloque todos os arquivos XLSX que você deseja converter em uma pasta.
2. Defina o caminho da pasta de entrada (onde os arquivos XLSX estão) e o caminho da pasta de saída (onde os arquivos CSV serão salvos).
3. Execute o código para converter os arquivos.

### Exemplo

```python
import pandas as pd
import os

def converter_xlsx_para_csv(diretorio_entrada: str, diretorio_saida: str):
    arquivos = [f for f in os.listdir(diretorio_entrada) if f.endswith('.xlsx')]
    for arquivo in arquivos:
        caminho_arquivo = os.path.join(diretorio_entrada, arquivo)
        caminho_saida = os.path.join(diretorio_saida, arquivo.replace('.xlsx', '.csv'))
        df = pd.read_excel(caminho_arquivo)
        df.to_csv(caminho_saida, encoding='utf-8', index=False)
        print(f'Arquivo {arquivo} convertido e salvo em: {caminho_saida}')

# Exemplo de uso
diretorio_entrada = r'C:\Users\seu_usuario\Downloads\xlsx_entrada'
diretorio_saida = r'C:\Users\seu_usuario\Downloads\csv_saida'

converter_xlsx_para_csv(diretorio_entrada, diretorio_saida)
```

## Contribuições

Se tiver sugestões ou melhorias, fique à vontade para contribuir.

---

Feito com ❤️ e com a ajuda do ChatGPT.

---
