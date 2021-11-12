# Login_The_Users
Login De Usuarios Em Python
from PySimpleGUI import PySimpleGUI as sg

sg.theme('Reddit')
layout = [
    [sg.Text('Usuário'),sg.Input(key='usuario',size=(20,1))],
    [sg.Text('Senha'),sg.Input(key='Senha',password_char='*',size=(20,1))],
    [sg.Checkbox('Salvar o login?')],
    [sg.Button('Entrar')]
]

janela = sg.Window('Tela de Login', layout)
while True:
    eventos, valores = janela.read()
    if eventos == sg.WINDOW_CLOSED:
        break
    if eventos == 'Entrar':
        if valores['usuario'] == 'steve' and valores['senha'] == '123456789':
            print('Ola Seja Bem Vindo!')
