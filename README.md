# Senior_Desafio
Desafio da Lógica de Programação da Senior(Usar no Visual Studio Code)


import PySimpleGUI as sg

class TelaEvento:
    def __init__(self):
        layout = [
            [sg.Text('Nome'),sg.Input(key='nome')],
            [sg.Text('Sobrenome'),sg.Input(key='sobrenome')],
            [sg.Text('Salas'),sg.Input(key='sala')],
            [sg.Text('Nome da Sala'),sg.Input(key='nome da sala')],
            [sg.Text('Lotação da Sala'),sg.Input(key='lotação da sala')],
            [sg.Text('Cafe'),sg.Input(key='cafe')],
            [sg.Text('Lotação da Café'),sg.Input(key='lotação do cafe')],
            [sg.Button('Cadastrar Dados')],
            [sg.Output(size=(30,20))]
        ]

        self.janela = sg.Window("Dados do Usuário").layout(layout)


    def Iniciar(self):
        while True:
            self.button, self.values = self.janela.Read()
            nome = self.values['nome']
            sobrenome = self.values['sobrenome']
            salas = self.values['sala']
            nome_da_sala = self.values['nome da sala']
            lotação_da_sala = self.values['lotação da sala']
            cafe = self.values['cafe']
            lotação_do_cafe = self.values['lotação do cafe']
            print(f'nome: {nome}')
            print(f'sobrenome: {sobrenome}')
            print(f'salas: {salas}')
            print(f'nome da sala: {nome_da_sala}')
            print(f'lotação da sala: {lotação_da_sala}')
            print(f'café: {cafe}')
            print(f'lotação do cafe: {lotação_do_cafe}')

tela = TelaEvento()
tela.Iniciar()
