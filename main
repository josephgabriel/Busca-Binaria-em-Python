def busca_normal(l, alvo):
    for i in range(len(l)):
        if l[i] == alvo:
            return i
    return -1

def busca_binaria(l, alvo, baixo=None, alto=None):
    if baixo is None:
        baixo = 0
    if alto is None:
        alto = len(l) - 1
    if alto < baixo:
        return -1

    ponto_medio = (baixo + alto) // 2

    if l[ponto_medio] == alvo:
        return ponto_medio
    elif alvo < l[ponto_medio]:
        return busca_binaria(l, alvo, baixo, ponto_medio - 1)
    else:
        return busca_binaria(l, alvo, ponto_medio + 1, alto)

if __name__ == '__main__':
    entrada = input("Digite os números separados por vírgula (ex: 10,5,3,8): ")
    try:
        l = [int(item.strip()) for item in entrada.split(",")] 
    except ValueError:
        print("Erro: certifique-se de digitar apenas números separados por vírgula.")
        exit()

    l.sort() 

    try:
        alvo = int(input("Digite o número a ser buscado: ").strip())
    except ValueError:
        print("Erro: insira um número válido.")
        exit()

    print("\nLista ordenada:", l)

    idx_normal = busca_normal(l, alvo)
    idx_binaria = busca_binaria(l, alvo)

    if idx_normal != -1:
        print(f"Busca normal: {alvo} encontrado no índice {idx_normal}")
    else:
        print(f"Busca normal: {alvo} não encontrado")

    if idx_binaria != -1:
        print(f"Busca binária: {alvo} encontrado no índice {idx_binaria}")
    else:
        print(f"Busca binária: {alvo} não encontrado")
