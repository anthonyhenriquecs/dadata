# dadata

def obter_datas(pessoa):
    """Solicita que a pessoa insira suas datas disponíveis e retorna uma lista de datas."""
    datas = []
    print(f"Olá, {pessoa}! Por favor, digite as datas em que você está disponível (dd/mm/aaaa).")
    print("Digite 'sair' para terminar.")
    
    while True:
        data = input("> ")
        if data.lower() == "sair":
            break
        datas.append(data)
    
    return datas

# Solicite suas datas
suas_datas = obter_datas("Você")

# Solicite as datas da sua namorada
datas_namorada = obter_datas("Sua namorada")

# Encontre datas em comum
datas_em_comum = list(set(suas_datas) & set(datas_namorada))

# Exiba as datas em comum
if datas_em_comum:
    print("\nAqui estão as datas em que ambos estão disponíveis:")
    for data in datas_em_comum:
        print(data)
else:
    print("\nInfelizmente, não há datas em comum. Talvez possam tentar sugerir novas datas.")

