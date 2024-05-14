import random

class AgentePedraPapelTesoura:
    def __init__(self):
        self.estrategias = ['pedra', 'papel', 'tesoura']
        
    def jogar(self):
        return random.choice(self.estrategias)

# Função para determinar o resultado do jogo
def determinar_vencedor(jogada_agente, jogada_jogador):
    if jogada_agente == jogada_jogador:
        return "Empate"
    elif (jogada_agente == 'pedra' and jogada_jogador == 'tesoura') or \
         (jogada_agente == 'tesoura' and jogada_jogador == 'papel') or \
         (jogada_agente == 'papel' and jogada_jogador == 'pedra'):
        return "Você perdeu"
    else:
        return "Você ganhou"

# Função principal do jogo
def jogar_pedra_papel_tesoura():
    agente = AgentePedraPapelTesoura()
    while True:
        print("\nEscolha sua jogada: pedra, papel ou tesoura (ou 'sair' para terminar o jogo)")
        jogada_jogador = input("Sua escolha: ").lower()
