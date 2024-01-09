# Passo a passo do projeto =========================================

# Passo 1 - Entrar no sistema da empresa ---------------------------

# pip install pyautogui
import pyautogui
import time

# clicar -> pyautogui.click
# escrever -> pyautogui.write
# apertar uma tecla -> pyautogui.press
# apertar -> pyautogui.hotkey
# scroll (rolar) -> pyautogui.scroll

pyautogui.PAUSE = 1
# aperta a tecla do windows
pyautogui.press("win") 
# digita o nome do programa
pyautogui.write("edge") 
# aperta enter
pyautogui.press("enter") 
time.sleep(1)
# digitar o link
link = "https://dlp.hashtagtreinamentos.com/python/intensivao/login"
pyautogui.write(link) 
# apertar enter
pyautogui.press("enter") 
# espera 3 segundos
time.sleep(3) 

# Passo 2 - Fazer login ------------------------------------------

# clicar no campo de email
pyautogui.click(x=787, y=406)
# digitar o email
pyautogui.write("eu@email.com")
# passar para o campo de senha
pyautogui.press("tab")
# digitar a senha
pyautogui.write("****")
# clicar no botão
pyautogui.click(x=957, y=569)
time.sleep(3)

# Passo 3 - Importar a base de dados -----------------------------
import pandas

tabela = pandas.read_csv("produtos.csv")
print(tabela)

# Passo 4 - Cadastrar um produto ---------------------------------
# Passo 5 - Repetir isso até acabar a base de dados --------------

for linha in tabela.index:
    pyautogui.click(x=747, y=284)
    # codigo
    codigo = tabela.loc[linha, "codigo"]
    pyautogui.write(codigo)
    pyautogui.press("tab")
    # marca
    pyautogui.write(tabela.loc[linha, "marca"])
    pyautogui.press("tab")
    # tipo
    pyautogui.write(tabela.loc[linha, "tipo"])
    pyautogui.press("tab")
    # categoria
    pyautogui.write(str(tabela.loc[linha, "categoria"]))
    pyautogui.press("tab")
    # preço
    pyautogui.write(str(tabela.loc[linha, "preco_unitario"]))
    pyautogui.press("tab")
    # custo
    pyautogui.write(str(tabela.loc[linha, "custo"]))
    pyautogui.press("tab")
    # obs
    obs = tabela.loc[linha, "obs"]
    if not pandas.isna(obs):
        pyautogui.write(obs)
    pyautogui.press("tab")
    # enviar o produto
    pyautogui.press("enter")
    # rolar pra cima
    pyautogui.scroll(5000)


