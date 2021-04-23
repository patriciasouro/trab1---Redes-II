#Patricia Rocha

import requests
import socket
from requests import get
from datetime import datetime
from getmac import get_mac_address

def internet ():
    try:
        requests.get('https://google.com.br') # envia uma solicitação GET para o url especificado
        return True
    except OSError:
        return False

if not internet (): # imprime na tela se a internet esta ativa ou não de acordo com o retorno da função internet()
    print('Internet não está ativa!')
else:
    print('Internet ativa!')


t1 = datetime.now() #salva o horario antes de executar a requisição
res = requests.get('https://google.com') #fazendo uma requisição ao site do google

if res:
    print('Requisição bem sucedida!')
else:
    print('Requisição falhou!')

t2 = datetime.now() # pega o tempo depois da requisição feita
total = t2-t1 #calcula o tempo que a requisicao demorou
print('Tempo de requisição: ', total, res)


hostname = socket.gethostname() #Retorne uma string contendo o nome do host da máquina onde o interpretador Python está executando atualmente.
ip = socket.gethostbyname(hostname) # traduz novamente um nome de host para o formato de endereço IPv4. O endereço IPv4 é retornado como uma string
nat = get('https://api.ipify.org').text # usando api do ipify para consultar ip externo
mac = get_mac_address()

print(f' IP: {ip} \n Nat: {nat} \n Mac: {mac}')
