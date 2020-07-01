# Lista-de-Compras-em-Python
Lista de compras básica desenvolvida em Python para disiplina de Programação Estruturada

from pip._vendor.distlib.compat import raw_input

listaCompras = []
def exibirMenu():
    print("1 - Adicionar item a lista de compras")
    print("2 - Excluir item da lista de compras")
    print("3 - Exibir a lista de compras ")
    print("4 - Sair do menu")
    acao = int(input("Por favor, informe uma das ações acima: "))
    return acao

def adicionarItem():
    novoItem = raw_input("Por favor, digite o nome do item que deseja adicionar: ")
    listaCompras.append(novoItem)

def exclirItem():
    nomeItem = raw_input("Por favor, digite o nome do intem que deseja excluir:")
    indice = -1
    encontrou = False
    for elemento in listaCompras:
        indice += 1
        if elemento == nomeItem:
            encontrou = True
            break
    if (encontrou):
        del listaCompras[indice]
def listarItens():
    for elemento in listaCompras:
        print (elemento)

while True:
    acao = exibirMenu()
    if acao == 4:
        break
    elif acao == 3:
        listarItens()
    elif acao == 1:
        adicionarItem()
    elif acao == 2:
        exclirItem()
