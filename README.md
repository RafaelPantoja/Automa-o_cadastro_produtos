# Automação_produtos
Sistema desenvolvido para ajudar no cadastro de produtos usando automação computacional.

import pyautogui
from time import sleep

# parâmetros da localização da tela do app em tela
pyautogui.click(1012,542, duration=2)
pyautogui.write('rafael')
pyautogui.click(990,577, duration=2)
pyautogui.write('123456')
pyautogui.click(858,607, duration=2)

with open('produtos.txt', 'r') as arquivo:
    for linha in arquivo:
        produto = linha.split(',')[0]
        quantidade = linha.split(',')[1]
        preco = linha.split(',')[2]

        pyautogui.click(690,526,duration=2)
        pyautogui.write(produto)
        pyautogui.click(687,557,duration=2)
        pyautogui.write(quantidade)
        pyautogui.click(688,591,duration=2)
        pyautogui.write(preco)
        pyautogui.click(513,787,duration=1)
