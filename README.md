import os
import platform

def verifica(v_arquivo):
    if not os.path.isfile(v_arquivo):
        print(f"O arquivo '{v_arquivo}' não existe.")
        return
      
    if os.path.getsize(v_arquivo) == 0:
        print(f"O arquivo '{v_arquivo}' está vazio.")
        return
   
    with open(v_arquivo, 'r') as arquivo:
        conteudo = arquivo.read()
        print("Conteúdo do arquivo:")
        print(conteudo)

    with open(v_arquivo, 'r') as arquivo:
        linhas = arquivo.readlines()
        num_linhas = len(linhas)
        print(f"Quantidade de linhas no arquivo: {num_linhas}")
      
# Exemplo de uso
arquivo = 'teste.csv'  
verifica(arquivo)# atividade-python
