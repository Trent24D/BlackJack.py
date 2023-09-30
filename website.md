---
title: "Black Jack with Money"
permalink: /
layout: default
theme: Tactile
---

'''
python
import random
import time
import os


Money = 180

os.system('clear')
print("Welcome to Black Jack!!")
print('\n')
time.sleep(1)
print("You will start the game with $200, but to sit at the table it costs $20. (So $180)")
time.sleep(1)
input("Press Enter to continue...")
os.system('clear')
print("At the start of each game you can place a bet equal too or less than $100 as well as higher than $10. (Keep it an integer)")
time.sleep(1)
input("Press Enter to continue...")
os.system('clear')
print("The winner will get the higher bet from the loser.")
time.sleep(1)
input("Press Enter to continue...")
os.system('clear')
print("You can chose to leave at anytime, but the goal is too get $1000.")
time.sleep(1)
input("Press Enter to continue...")
os.system('clear')
print("If you cheat or break a rule, the house will kick you from the casino.")
time.sleep(1)
input("Press Enter to continue...")
os.system('clear')

while True:
			os.system('clear')

			if Money <= 0:
							print("You have gone in debt and have been kicked from the casino.")
							exit()


			
			try:

							print("How much would you like to bet this round?")
							print("Money left: $" ,int(Money))
							PlayerBet = int(input("$"))

			except ValueError:
							print("Invalid input. Please enter an integer.")
							time.sleep(2)
							continue

			if PlayerBet <= 0:
							print("The casino did not like your joke. You have been kicked from the casino. ")
							exit()


			elif PlayerBet >= 181:
							print("The casinos maximum bet is $100. You have been kicked from the casino.")
							exit()
			elif PlayerBet <=9:
				print("The minimum bet is $10.")
				time.sleep(2)
				continue

			
			Money -= PlayerBet

			if Money < 0:
				print("You have gone into debt and have been kicked from the casino.")
				exit()
			print("The Dealer checks. The bet is $",int(PlayerBet))
			Bet = PlayerBet



			print("Welcome to BlackJack!")

			input("Press Enter to continue...")
			os.system('clear')

			print("Shuffling...")

			time.sleep(3)

			os.system('clear')

			print("Dealing Cards...")

			time.sleep(2.2)

			os.system('clear')

			DealerAceOne = 0
			DealerAceTwo = 0
			DealerAceThree = 0
			DealerAceFour = 0
			DealerAceFive = 0
			AceOne = 0
			AceTwo = 0
			AceThree = 0
			AceFour = 0
			AceFive = 0

			ParL = '{'
			ParR = '}'

			for CardOne in range (1):
							CardOne = random.randint(0, 51)


			for CardTwo in range (1):
							CardTwo = random.randint(0, 51)

			for CardThree in range (1):
							CardThree = random.randint(0, 51)

			for CardFour in range (1):
							CardFour = random.randint(0, 51)

			for CardFive in range (1):
							CardFive = random.randint(0, 51)

			for DealerOne in range (1):
							DealerOne = random.randint(0, 51)

			for DealerTwo in range (1):
							DealerTwo = random.randint(0, 51)

			for DealerThree in range (1):
							DealerThree = random.randint(0, 51)

			for DealerFour in range (1):
							DealerFour = random.randint(0, 51)

			for DealerFive in range (1):
							DealerFive = random.randint(0, 51)
			

			while (CardOne == CardTwo or CardOne == CardThree or CardOne == CardFour or CardOne == CardFive or CardOne == DealerOne or CardOne == DealerTwo or CardOne == DealerThree or CardOne == DealerFour == CardOne == DealerFive or CardTwo == CardThree or CardTwo == CardFour or CardTwo == CardFive or CardTwo == DealerOne or CardTwo == DealerTwo or CardTwo == DealerThree or CardTwo == DealerFour or CardTwo == DealerFive or CardThree == CardFour or CardThree == CardFive or CardThree == DealerOne or CardThree == DealerTwo or CardThree == DealerThree or CardThree == DealerFour or CardThree == DealerFive or CardFour == CardFive or CardFour == DealerOne or CardFour == DealerTwo or CardFour == DealerThree or CardFour == DealerFour == CardFour == DealerFive or CardFive == DealerOne or CardFive == DealerTwo or CardFive == DealerThree or CardFive == DealerFour or CardFive == DealerFive or DealerOne == DealerTwo or DealerOne == DealerThree or DealerOne == DealerFour or DealerOne == DealerFive or DealerTwo == DealerThree or DealerTwo == DealerFour or DealerTwo == DealerFive or DealerThree == DealerFour or DealerThree == DealerFive or DealerFour == DealerFive ):
							if   (CardOne == CardTwo or CardOne == CardThree or CardOne == CardFour or CardOne == CardFive or CardOne == DealerOne or CardOne == DealerTwo or CardOne == DealerThree or CardOne == DealerFour or CardOne == DealerFive):
															if (CardOne == 51):
																			CardOne -= 5
															else: 
																			CardOne += 1

							if (CardTwo == CardThree or CardTwo == CardFour or CardTwo == CardFive or CardTwo == DealerOne or CardTwo == DealerTwo or CardTwo == DealerThree or CardTwo == DealerFour or CardTwo == DealerFive):
															if (CardTwo == 51):
																			CardTwo -= 3
															else:
																			CardTwo += 1

							if (CardThree == CardFour or CardThree == CardFive or CardThree == DealerOne or CardThree == DealerTwo or CardThree == DealerThree or CardThree == DealerFour or CardThree == DealerFive):
															if (CardThree == 51):
																			CardThree -= 3
															else:
																			CardThree += 1

							if (CardFour == CardFive or CardFour == DealerOne or CardFour == DealerTwo or CardFour == DealerThree or CardFour == DealerFour or CardFour == DealerFive):
															if (CardFour == 51):
																			CardFour -= 2
															else: 
																			CardFour += 1

							if (CardFive == DealerOne or CardFive == DealerTwo or CardFive == DealerThree or CardFive == DealerFour or CardFive == DealerFive):
															if (CardFive == 51):
																			CardFive -= 3
															else: 
																			CardFive += 1

							if (DealerOne == DealerTwo or DealerOne == DealerThree or DealerOne == DealerFour or DealerOne == DealerFive):
															if (DealerOne == 51):
																			DealerOne -= 3
															else: 
																			DealerOne += 1
							if (DealerTwo == DealerThree or DealerTwo == DealerFour or DealerTwo == DealerFive):
															if (DealerTwo == 51):
																			DealerTwo -= 3
															else: 
																			DealerTwo += 1
							if (DealerThree == DealerFour or DealerThree == DealerFive):
															if (DealerThree == 51):
																			DealerThree -= 5
															else: 
																			DealerThree += 1
							if (DealerFour == DealerFive):
															if (DealerFour == 51):
																			DealerFour -= 10
															else: 
																			DealerFour += 1

			cards = ["Ace of Spades","Ace of Clubs","Ace of Diamonds", "Ace of Hearts", "Two of Hearts", "Two of Spades", "Two of Clubs", "Two of Diamonds", "Three of Clubs", "Three of Spades", "Three of Hearts", "Three of Diamonds", "Four of Spades", "Four of Hearts", "Four of Clubs", "Four of Diamonds", "Five of Spades", "Five of Clubs", "Five of Hearts", "Five of Diamonds", "Six of Clubs", "Six of Spades", "Six of hearts", "Six of Diamonds", "Seven of Spades", "Seven of Clubs", "Seven of Hearts", "Seven of Diamonds", "Eight of Clubs", "Eight of Spades", "Eight of Hearts", "Eight of Diamonds", "Nine of Spades", "Nine of Clubs", "Nine of Hearts", "Nine of Diamonds", "Ten of Clubs", "Ten of Spades", "Ten of Diamonds", "Ten of Hearts", "Jack of Spades", "Jack of Hearts", "Jack of Clubs", "Jack of Diamonds", "Queen of Hearts", "Queen of Diamonds", "Queen of Spades", "Queen of Clubs", "King of Spades", "King of Clubs", "King of Diamonds", "King of Hearts"]

			# Score One here
			if (CardOne ==  0 or CardOne == 1 or CardOne == 2 or CardOne == 3):
							CardOneScore = 11
			elif (CardOne == 4 or CardOne == 5 or CardOne == 6 or CardOne == 7):
							CardOneScore = 2
			elif (CardOne == 8 or CardOne == 9 or CardOne == 10 or CardOne == 11):
							CardOneScore = 3
			elif (CardOne == 12 or CardOne == 13 or CardOne == 14 or CardOne == 15):
							CardOneScore = 4
			elif (CardOne == 16 or CardOne == 17 or CardOne == 18 or CardOne == 19):
							CardOneScore = 5
			elif (CardOne == 20 or CardOne == 21 or CardOne == 22 or CardOne == 23):
							CardOneScore = 6
			elif (CardOne == 24 or CardOne == 25 or CardOne == 26 or CardOne == 27):
							CardOneScore = 7
			elif (CardOne == 28 or CardOne == 29 or CardOne == 30 or CardOne == 31):
							CardOneScore = 8
			elif (CardOne == 32 or CardOne == 33 or CardOne == 34 or CardOne == 35):
							CardOneScore = 9
			elif (CardOne == 36 or CardOne == 37 or CardOne == 38 or CardOne == 39):
							CardOneScore = 10
			elif (CardOne == 40 or CardOne == 41 or CardOne == 42 or CardOne == 43):
							CardOneScore = 10
			elif (CardOne == 44 or CardOne == 45 or CardOne == 46 or CardOne == 47):
							CardOneScore = 10
			elif (CardOne == 48 or CardOne == 49 or CardOne == 50 or CardOne == 51):
							CardOneScore = 10
			# CardTwo Score

			if (CardTwo ==  0 or CardTwo == 1 or CardTwo == 2 or CardTwo == 3):
							CardTwoScore = 11
			elif (CardTwo == 4 or CardTwo ==  5 or CardTwo ==  6 or CardTwo ==  7):
							CardTwoScore = 2
			elif (CardTwo == 8 or CardTwo ==  9 or CardTwo ==  10 or CardTwo ==  11):
							CardTwoScore = 3
			elif (CardTwo == 12 or CardTwo ==  13 or CardTwo ==  14 or CardTwo ==  15):
							CardTwoScore = 4
			elif (CardTwo == 16 or CardTwo ==  17 or CardTwo ==  18 or CardTwo ==  19):
							CardTwoScore = 5
			elif (CardTwo == 20 or CardTwo ==  21 or CardTwo ==  22 or CardTwo ==  23):
							CardTwoScore = 6
			elif (CardTwo == 24 or CardTwo ==  25 or CardTwo ==  26 or CardTwo ==  27):
							CardTwoScore = 7
			elif (CardTwo == 28 or CardTwo ==  29 or CardTwo ==  30 or CardTwo ==  31):
							CardTwoScore = 8
			elif (CardTwo == 32 or CardTwo ==  33 or CardTwo ==  34 or CardTwo ==  35):
							CardTwoScore = 9
			elif (CardTwo == 36 or CardTwo ==  37 or CardTwo ==  38 or CardTwo ==  39):
							CardTwoScore = 10
			elif (CardTwo == 40 or CardTwo ==  41 or CardTwo ==  42 or CardTwo ==  43):
							CardTwoScore = 10
			elif (CardTwo == 44 or CardTwo ==  45 or CardTwo ==  46 or CardTwo ==  47):
							CardTwoScore = 10
			elif (CardTwo == 48 or CardTwo ==  49 or CardTwo ==  50 or CardTwo ==  51):
							CardTwoScore = 10
			# CardThree Score

			if (CardThree == 0 or CardThree == 1 or CardThree == 2 or CardThree == 3):
							CardThreeScore = 11
			elif (CardThree == 4 or CardThree == 5 or CardThree == 6 or CardThree == 7):
							CardThreeScore = 2
			elif (CardThree == 8 or CardThree == 9 or CardThree == 10 or CardThree == 11):
							CardThreeScore = 3
			elif (CardThree == 12 or CardThree == 13 or CardThree == 14 or CardThree == 15):
							CardThreeScore = 4
			elif (CardThree == 16 or CardThree == 17 or CardThree == 18 or CardThree == 19):
							CardThreeScore = 5
			elif (CardThree == 20 or CardThree == 21 or CardThree == 22 or CardThree == 23):
							CardThreeScore = 6
			elif (CardThree == 24 or CardThree == 25 or CardThree == 26 or CardThree == 27):
							CardThreeScore = 7
			elif (CardThree == 28 or CardThree == 29 or CardThree == 30 or CardThree == 31):
							CardThreeScore = 8
			elif (CardThree == 32 or CardThree == 33 or CardThree == 34 or CardThree == 35):
							CardThreeScore = 9
			elif (CardThree == 36 or CardThree == 37 or CardThree == 38 or CardThree == 39):
							CardThreeScore = 10
			elif (CardThree == 40 or CardThree == 41 or CardThree == 42 or CardThree == 43):
							CardThreeScore = 10
			elif (CardThree == 44 or CardThree == 45 or CardThree == 46 or CardThree == 47):
							CardThreeScore = 10
			elif (CardThree == 48 or CardThree == 49 or CardThree == 50 or CardThree == 51):
							CardThreeScore = 10
			# ScoreFour Score

			if (CardFour == 0 or CardFour == 1 or CardFour == 2 or CardFour == 3):
							CardFourScore = 11
			elif (CardFour == 4 or CardFour == 5 or CardFour == 6 or CardFour == 7):
							CardFourScore = 2
			elif (CardFour == 8 or CardFour == 9 or CardFour == 10 or CardFour == 11):
							CardFourScore = 3
			elif (CardFour == 12 or CardFour == 13 or CardFour == 14 or CardFour == 15):
							CardFourScore = 4
			elif (CardFour == 16 or CardFour == 17 or CardFour == 18 or CardFour == 19):
							CardFourScore = 5
			elif (CardFour == 20 or CardFour == 21 or CardFour == 22 or CardFour == 23):
							CardFourScore = 6
			elif (CardFour == 24 or CardFour == 25 or CardFour == 26 or CardFour == 27):
							CardFourScore = 7
			elif (CardFour == 28 or CardFour == 29 or CardFour == 30 or CardFour == 31):
							CardFourScore = 8
			elif (CardFour == 32 or CardFour == 33 or CardFour == 34 or CardFour == 35):
							CardFourScore = 9
			elif (CardFour == 36 or CardFour == 37 or CardFour == 38 or CardFour == 39):
							CardFourScore = 10
			elif (CardFour == 40 or CardFour == 41 or CardFour == 42 or CardFour == 43):
							CardFourScore = 10
			elif (CardFour == 44 or CardFour == 45 or CardFour == 46 or CardFour == 47):
							CardFourScore = 10
			elif (CardFour == 48 or CardFour == 49 or CardFour == 50 or CardFour == 51):
							CardFourScore = 10
			# ScoreFive Score

			if (CardFive == 0 or CardFive == 1 or CardFive == 2 or CardFive == 3):
							CardFiveScore = 11
			elif (CardFive == 4 or CardFive == 5 or CardFive == 6 or CardFive == 7):
							CardFiveScore = 2
			elif (CardFive == 8 or CardFive == 9 or CardFive == 10 or CardFive == 11):
							CardFiveScore = 3
			elif (CardFive == 12 or CardFive == 13 or CardFive == 14 or CardFive == 15):
							CardFiveScore = 4
			elif (CardFive == 16 or CardFive == 17 or CardFive == 18 or CardFive == 19):
							CardFiveScore = 5
			elif (CardFive == 20 or CardFive == 21 or CardFive == 22 or CardFive == 23):
							CardFiveScore = 6
			elif (CardFive == 24 or CardFive == 25 or CardFive == 26 or CardFive == 27):
							CardFiveScore = 7
			elif (CardFive == 28 or CardFive == 29 or CardFive == 30 or CardFive == 31):
							CardFiveScore = 8
			elif (CardFive == 32 or CardFive == 33 or CardFive == 34 or CardFive == 35):
							CardFiveScore = 9
			elif (CardFive == 36 or CardFive == 37 or CardFive == 38 or CardFive == 39):
							CardFiveScore = 10
			elif (CardFive == 40 or CardFive == 41 or CardFive == 42 or CardFive == 43):
							CardFiveScore = 10
			elif (CardFive == 44 or CardFive == 45 or CardFive == 46 or CardFive == 47):
							CardFiveScore = 10
			elif (CardFive == 48 or CardFive == 49 or CardFive == 50 or CardFive == 51):
							CardFiveScore = 10
			# DealerOne Score

			if (DealerOne == 0 or DealerOne == 1 or DealerOne == 2 or DealerOne == 3):
							DealerOneScore = 11
			elif (DealerOne == 4 or DealerOne == 5 or DealerOne == 6 or DealerOne == 7):
							DealerOneScore = 2
			elif (DealerOne == 8 or DealerOne == 9 or DealerOne == 10 or DealerOne == 11):
							DealerOneScore = 3
			elif (DealerOne == 12 or DealerOne == 13 or DealerOne == 14 or DealerOne == 15):
							DealerOneScore = 4
			elif (DealerOne == 16 or DealerOne == 17 or DealerOne == 18 or DealerOne == 19):
							DealerOneScore = 5
			elif (DealerOne == 20 or DealerOne == 21 or DealerOne == 22 or DealerOne == 23):
							DealerOneScore = 6
			elif (DealerOne == 24 or DealerOne == 25 or DealerOne == 26 or DealerOne == 27):
							DealerOneScore = 7
			elif (DealerOne == 28 or DealerOne == 29 or DealerOne == 30 or DealerOne == 31):
							DealerOneScore = 8
			elif (DealerOne == 32 or DealerOne == 33 or DealerOne == 34 or DealerOne == 35):
							DealerOneScore = 9
			elif (DealerOne == 36 or DealerOne == 37 or DealerOne == 38 or DealerOne == 39):
							DealerOneScore = 10
			elif (DealerOne == 40 or DealerOne == 41 or DealerOne == 42 or DealerOne == 43):
							DealerOneScore = 10
			elif (DealerOne == 44 or DealerOne == 45 or DealerOne == 46 or DealerOne == 47):
							DealerOneScore = 10
			elif (DealerOne == 48 or DealerOne == 49 or DealerOne == 50 or DealerOne == 51):
							DealerOneScore = 10
			# DealerTwo Score

			if (DealerTwo == 0 or DealerTwo == 1 or DealerTwo == 2 or DealerTwo == 3):
							DealerTwoScore = 11
			elif (DealerTwo == 4 or DealerTwo == 5 or DealerTwo == 6 or DealerTwo == 7):
							DealerTwoScore = 2
			elif (DealerTwo == 8 or DealerTwo == 9 or DealerTwo == 10 or DealerTwo == 11):
							DealerTwoScore = 3
			elif (DealerTwo == 12 or DealerTwo == 13 or DealerTwo == 14 or DealerTwo == 15):
							DealerTwoScore = 4
			elif (DealerTwo == 16 or DealerTwo == 17 or DealerTwo == 18 or DealerTwo == 19):
							DealerTwoScore = 5
			elif (DealerTwo == 20 or DealerTwo == 21 or DealerTwo == 22 or DealerTwo == 23):
							DealerTwoScore = 6
			elif (DealerTwo == 24 or DealerTwo == 25 or DealerTwo == 26 or DealerTwo == 27):
							DealerTwoScore = 7
			elif (DealerTwo == 28 or DealerTwo == 29 or DealerTwo == 30 or DealerTwo == 31):
							DealerTwoScore = 8
			elif (DealerTwo == 32 or DealerTwo == 33 or DealerTwo == 34 or DealerTwo == 35):
							DealerTwoScore = 9
			elif (DealerTwo == 36 or DealerTwo == 37 or DealerTwo == 38 or DealerTwo == 39):
							DealerTwoScore = 10
			elif (DealerTwo == 40 or DealerTwo == 41 or DealerTwo == 42 or DealerTwo == 43):
							DealerTwoScore = 10
			elif (DealerTwo == 44 or DealerTwo == 45 or DealerTwo == 46 or DealerTwo == 47):
							DealerTwoScore = 10
			elif (DealerTwo == 48 or DealerTwo == 49 or DealerTwo == 50 or DealerTwo == 51):
							DealerTwoScore = 10
			# DealerThree Score

			if (DealerThree == 0 or DealerThree == 1 or DealerThree == 2 or DealerThree == 3):
							DealerThreeScore = 11
			elif (DealerThree == 4 or DealerThree == 5 or DealerThree == 6 or DealerThree == 7):
							DealerThreeScore = 2
			elif (DealerThree == 8 or DealerThree == 9 or DealerThree == 10 or DealerThree == 11):
							DealerThreeScore = 3
			elif (DealerThree == 12 or DealerThree == 13 or DealerThree == 14 or DealerThree == 15):
							DealerThreeScore = 4
			elif (DealerThree == 16 or DealerThree == 17 or DealerThree == 18 or DealerThree == 19):
							DealerThreeScore = 5
			elif (DealerThree == 20 or DealerThree == 21 or DealerThree == 22 or DealerThree == 23):
							DealerThreeScore = 6
			elif (DealerThree == 24 or DealerThree == 25 or DealerThree == 26 or DealerThree == 27):
							DealerThreeScore = 7
			elif (DealerThree == 28 or DealerThree == 29 or DealerThree == 30 or DealerThree == 31):
							DealerThreeScore = 8
			elif (DealerThree == 32 or DealerThree == 33 or DealerThree == 34 or DealerThree == 35):
							DealerThreeScore = 9
			elif (DealerThree == 36 or DealerThree == 37 or DealerThree == 38 or DealerThree == 39):
							DealerThreeScore = 10
			elif (DealerThree == 40 or DealerThree == 41 or DealerThree == 42 or DealerThree == 43):
							DealerThreeScore = 10
			elif (DealerThree == 44 or DealerThree == 45 or DealerThree == 46 or DealerThree == 47):
							DealerThreeScore = 10
			elif (DealerThree == 48 or DealerThree == 49 or DealerThree == 50 or DealerThree == 51):
							DealerThreeScore = 10
			# DealerFour Score

			if (DealerFour == 0 or DealerFour == 1 or DealerFour == 2 or DealerFour == 3):
							DealerFourScore = 11
			elif (DealerFour == 4 or DealerFour == 5 or DealerFour == 6 or DealerFour == 7):
							DealerFourScore = 2
			elif (DealerFour == 8 or DealerFour == 9 or DealerFour == 10 or DealerFour == 11):
							DealerFourScore = 3
			elif (DealerFour == 12 or DealerFour == 13 or DealerFour == 14 or DealerFour == 15):
							DealerFourScore = 4
			elif (DealerFour == 16 or DealerFour == 17 or DealerFour == 18 or DealerFour == 19):
							DealerFourScore = 5
			elif (DealerFour == 20 or DealerFour == 21 or DealerFour == 22 or DealerFour == 23):
							DealerFourScore = 6
			elif (DealerFour == 24 or DealerFour == 25 or DealerFour == 26 or DealerFour == 27):
							DealerFourScore = 7
			elif (DealerFour == 28 or DealerFour == 29 or DealerFour == 30 or DealerFour == 31):
							DealerFourScore = 8
			elif (DealerFour == 32 or DealerFour == 33 or DealerFour == 34 or DealerFour == 35):
							DealerFourScore = 9
			elif (DealerFour == 36 or DealerFour == 37 or DealerFour == 38 or DealerFour == 39):
							DealerFourScore = 10
			elif (DealerFour == 40 or DealerFour == 41 or DealerFour == 42 or DealerFour == 43):
							DealerFourScore = 10
			elif (DealerFour == 44 or DealerFour == 45 or DealerFour == 46 or DealerFour == 47):
							DealerFourScore = 10
			elif (DealerFour == 48 or DealerFour == 49 or DealerFour == 50 or DealerFour == 51):
							DealerFourScore = 10
			# DealerFive Score

			if (DealerFive == 0 or DealerFive == 1 or DealerFive == 2 or DealerFive == 3):
							DealerFiveScore = 11
			elif (DealerFive == 4 or DealerFive == 5 or DealerFive == 6 or DealerFive == 7):
							DealerFiveScore = 2
			elif (DealerFive == 8 or DealerFive == 9 or DealerFive == 10 or DealerFive == 11):
							DealerFiveScore = 3
			elif (DealerFive == 12 or DealerFive == 13 or DealerFive == 14 or DealerFive == 15):
							DealerFiveScore = 4
			elif (DealerFive == 16 or DealerFive == 17 or DealerFive == 18 or DealerFive == 19):
							DealerFiveScore = 5
			elif (DealerFive == 20 or DealerFive == 21 or DealerFive == 22 or DealerFive == 23):
							DealerFiveScore = 6
			elif (DealerFive == 24 or DealerFive == 25 or DealerFive == 26 or DealerFive == 27):
							DealerFiveScore = 7
			elif (DealerFive == 28 or DealerFive == 29 or DealerFive == 30 or DealerFive == 31):
							DealerFiveScore = 8
			elif (DealerFive == 32 or DealerFive == 33 or DealerFive == 34 or DealerFive == 35):
							DealerFiveScore = 9
			elif (DealerFive == 36 or DealerFive == 37 or DealerFive == 38 or DealerFive == 39):
							DealerFiveScore = 10
			elif (DealerFive == 40 or DealerFive == 41 or DealerFive == 42 or DealerFive == 43):
							DealerFiveScore = 10
			elif (DealerFive == 44 or DealerFive == 45 or DealerFive == 46 or DealerFive == 47):
							DealerFiveScore = 10
			elif (DealerFive == 48 or DealerFive == 49 or DealerFive == 50 or DealerFive == 51):
							DealerFiveScore = 10

			CardOne = cards[CardOne]
			CardTwo = cards[CardTwo]
			CardThree = cards[CardThree]
			CardFour = cards[CardFour]
			CardFive = cards[CardFive]

			DealerOne = cards[DealerOne]
			DealerTwo = cards[DealerTwo]
			DealerThree = cards[DealerThree]
			DealerFour = cards[DealerFour]
			DealerFive = cards[DealerFive]

			if CardOneScore == 11:
											AceOne = CardOneScore
											CardOneScore = 0
							
			if CardTwoScore == 11:
											AceTwo = CardTwoScore
											CardTwoScore = 0
							
			if CardThreeScore == 11:
											AceThree = CardThreeScore
											CardThreeScore = 0

			if CardFourScore == 11:
											AceFour = CardFourScore
											CardFourScore = 0

			if CardFiveScore == 11:
											AceFive = CardFiveScore
											CardFiveScore = 0

			if DealerOneScore == 11:
											DealerAceOne = DealerOneScore
											DealerOneScore = 0
							
			if DealerTwoScore == 11:
											DealerAceTwo = DealerTwoScore
											DealerTwoScore = 0
							
			if DealerThreeScore == 11:
											DealerAceThree = DealerThreeScore
											DealerThreeScore = 0
							
			if DealerFourScore == 11:
											DealerAceFour = DealerFourScore
											DealerFourScore = 0
							
			if DealerFiveScore == 11:
											DealerAceFive = DealerFiveScore
											DealerFiveScore = 0
							
			#Round One
			Total = int(CardOneScore + CardTwoScore + AceOne + AceTwo)
			DealerTotal = int(DealerOneScore + DealerTwoScore + DealerAceOne + DealerAceTwo)


			print("Your cards: " + CardOne+ " and " + CardTwo , "{", str(Total) ,"}" + "          Money left: $" ,int(Money))
			print("Dealer's face up card: " + DealerOne )

			if (Total == 21):             
							os.system('clear')
							print("Your cards: " + CardOne+ " and " + CardTwo , "{", str(Total) ,"}" + "          Money left: $" ,int(Money))
							print("Dealer's Hand: " + DealerOne + " and " + DealerTwo)
							print("Congrats you have beaten the dealer and made $"+ str(Bet) + "!" )
							Money += 2 * Bet
							input("Press Enter to continue...")
							continue

			if (DealerTotal == 21):
							os.system('clear')
							print("Your cards: " + CardOne+ " and " + CardTwo , "{", str(Total) ,"}" + "          Money left: $" ,int(Money) )
							print("Dealer's Hand: " + DealerOne + " and " + DealerTwo)
							print("The Dealer has 21 you have lost $"+ str(Bet) + "." )
							
							input("Press Enter to continue...")
							continue


			#Round 2 
			time.sleep(1)
			HitStayOne = str(input("Would you like to hit (h) or stay (s)?" ))
			HitStayOne = HitStayOne.lower()
			if (HitStayOne == "h" or HitStayOne == "hit"):

							os.system('clear')

							Total = CardOneScore + CardTwoScore + CardThreeScore + AceOne + AceTwo + AceThree

							if (Total > 21 and AceOne > 5):
											AceOne = 1
											CardOneScore = 0
											
							if (Total > 21 and AceTwo > 2):
											AceTwo = 1
											CardTwoScore = 0
											
							if (Total > 21 and AceThree > 2):
											AceThree = 1
											CardThreeScore = 0
							
							Total = CardOneScore + CardTwoScore + CardThreeScore + AceOne + AceTwo + AceThree

							print("Your cards are: " + CardOne + ", " + CardTwo +", " + CardThree + " " + ParL + str(Total) + ParR + "          Money left: $" , int(Money) )
							print("The Dealer's face up card is: " + DealerOne)
							if (Total > 21 and AceTwo == 1 and AceOne == 1 and AceThree == 1):
											os.system('clear')
											print("Your cards are: " + CardOne + ", " + CardTwo +", " + CardThree + " " + ParL + str(Total) + ParR + "          Money left: $" , int(Money) )
											print("Dealer's Hand: " + DealerOne + " and " + DealerTwo + ", " + DealerThree)
											print("You have gone bust and have lost $"+ str(Bet) + "." )
								
											input("Press Enter to continue...")
											continue
							elif (Total > 21 and AceOne == 0 and AceTwo == 0 and AceThree == 0):
											os.system('clear')
											print("Your cards are: " + CardOne + ", " + CardTwo +", " + CardThree + " " + ParL + str(Total) + ParR +  "          Money left: $" , int(Money) )
											print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " and " + DealerThree)
											print("You have gone bust and have lost $" ,str(Bet) + "." )
							
											input("Press Enter to continue...")
											continue

							elif (Total == 21):
											os.system('clear')
											print("Your cards are: " + CardOne + ", " + CardTwo +", " + CardThree + " " + ParL + str(Total) + ParR+ "          Money left: $" , int(Money) )
											print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " and " + DealerThree)
											print("Congrats you have beaten the dealer and made $"+ str(Bet) + "!" )
											Money += 2 * Bet
											input("Press Enter to continue...")
											continue
							elif Total > 21:
											os.system('clear')
											print("Your cards are: " + CardOne + ", " + CardTwo +", " + CardThree + " " + ParL + str(Total) + ParR +  "          Money left: $" , int(Money) )
											print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " and " + DealerThree)
											print("You have gone bust and have lost $" ,str(Bet) + "." )
							
											input("Press Enter to continue...")
											continue
								

							#Dealer Turn One
			elif (HitStayOne == "s" or HitStayOne == "stay"):
							DealerTotal = DealerOneScore + DealerTwoScore + DealerAceOne + DealerAceTwo

							
							
							if (DealerTotal > 21 and DealerAceOne > 5):
															DealerAceOne = 1
															DealerOneScore = 0
															DealerTotal = DealerOneScore + DealerTwoScore + DealerAceOne + DealerAceTwo
											
							if (DealerTotal > 21 and DealerAceTwo > 2):
															DealerAceTwo = 1
															DealerTwoScore = 0
															DealerTotal = DealerOneScore + DealerTwoScore + DealerAceOne + DealerAceTwo
							if (DealerTotal > 21 and DealerAceThree > 2):
															DealerAceThree = 1
															DealerThreeScore = 0

							DealerTotal = DealerOneScore + DealerTwoScore + DealerAceOne + DealerAceTwo

							if (DealerTotal > 21 and DealerAceOne == 0 and DealerAceTwo == 0 and DealerAceThree == 0):
											os.system('clear')
											print("Your hand: " + CardOne + " and " + CardTwo + " " + ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
											print("Dealer's Hand: " + DealerOne + " and " + DealerTwo)
											print("The Dealer has gone bust so you made $"+ str(Bet) + "!" )
											Money += 2 * Bet
											input("Press Enter to continue...")
											continue
											
											
											exit()
							if (DealerTotal >= 17 and DealerTotal < 21):
											if (DealerTotal > Total):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + " and " + DealerTwo + " "+ParL + str(DealerTotal) + ParR)
															print("Your Hand: " + CardOne + ', ' + CardTwo + " " + ParL + str(Total) + ParR+ "          Money left: $" , int(Money) )
															print("The Dealer won so you lost $" ,str(Bet) + ".")
															
															input("Press Enter to continue...")
															continue
											if (DealerTotal < Total):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " "+ParL + str(DealerTotal) + ParR)
															print("Your Hand: " + CardOne + ', ' + CardTwo + " "+ ParL + str(Total) + ParR+ "          Money left: $" , int(Money) )
															print("Congrats you have beaten the dealer and made $"+ str(Bet) + "!" )
															Money += 2 * Bet
															input("Press Enter to continue...")
															continue
															
											if (DealerTotal  == Total):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " "+ParL + str(DealerTotal) + ParR)
															print("Your Hand: " + CardOne + ', ' + CardTwo + " "+ ParL + str(Total) + ParR+  "          Money left: $" , int(Money) )
															print("The game is a draw. Your money has been returned.")
															input("Press Enter to continue...")
															Money += Bet
															continue
															
							if (DealerTotal < 17):

							
								DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerAceOne + DealerAceTwo + DealerAceThree


								if (DealerTotal > 21 and DealerAceOne > 5):
												DealerAceOne = 1
												DealerOneScore = 0
								
								if (DealerTotal > 21 and DealerAceTwo > 2):
												DealerAceTwo = 1
												DealerTwoScore = 0
								if (DealerTotal > 21 and DealerAceThree > 2):
												DealerAceThree = 1
												DealerThreeScore = 0
							
								DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerAceOne + DealerAceTwo + DealerAceThree


								if (DealerTotal > 21 and DealerAceOne == 0 and DealerAceTwo == 0 and DealerAceThree == 0):
											print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " and " + DealerThree)
											time.sleep(2)
											print("The Dealer has gone bust so you won $" ,str(Bet) )
											Money += 2 * Bet
											input("Press Enter to continue...")
											continue
											
											
											
								if (DealerTotal >= 17 and DealerTotal < 21):
											if (DealerTotal > Total):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree+ " " + ParL + str(DealerTotal) + ParR)
															print("Your Hand: " + CardOne + ', ' + CardTwo + " " + ParL + str(Total) + ParR+  "          Money left: $" , int(Money) )
															print("The Dealer won so you lost $" ,str(Bet) + ".")
															
															input("Press Enter to continue...")
															continue

											if (DealerTotal < Total):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree+ " " + ParL + str(DealerTotal) + ParR)
															print("Your Hand: " + CardOne + ' and ' + CardTwo + " " + ParL + str(Total) + ParR+ "          Money left: $" , int(Money) )
															print("Congrats you have beaten the dealer and made $"+ str(Bet) + "!" )
															Money += 2 * Bet
															input("Press Enter to continue...")
															continue

											if (DealerTotal  == Total):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree+ " " + ParL + str(DealerTotal) + ParR)
															print("Your Hand: " + CardOne + ', ' + CardTwo + " " + ParL + str(Total) + ParR+  "          Money left: $" , int(Money) )
															print("The game is a draw. Your money has been returned.")
															input("Press Enter to continue...")
															Money += Bet
															continue
															
															

							if (DealerTotal > 21 and DealerAceOne ==1 and DealerAceTwo ==1 and DealerAceThree ==1):
											print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree)
											time.sleep(2)
											print("The Dealer has gone bust so you won $" ,str(Bet) + "!" )
											Money += 2 * Bet
											input("Press Enter to continue...")
											continue

							if (DealerTotal == 21):
											print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree)
											time.sleep(2)
											print("The Dealer has made 21 and you lose $" ,str(Bet) + ".")
												
											input("Press Enter to continue...")
											continue

							if (DealerTotal < 17 ):
											DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerFourScore + DealerAceOne + DealerAceTwo + DealerAceThree + DealerAceFour

											if (DealerTotal > 21 and DealerAceOne > 5):
															DealerAceOne = 1
															DealerOneScore = 0
											
											if (DealerTotal > 21 and DealerAceTwo > 2):
															DealerAceTwo = 1
															DealerTwoScore = 0
											

											if (DealerTotal > 21 and DealerAceThree > 2):
															DealerAceThree = 1
															DealerThreeScore = 0

											if (DealerTotal > 21 and DealerAceFour > 2):
															DealerAceFour = 1 
															DealerFourScore = 0

											
											DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerFourScore + DealerAceOne + DealerAceTwo + DealerAceThree + DealerAceFour

											if (DealerTotal > 21 and DealerAceOne == 0 and DealerAceTwo == 0 and DealerAceThree == 0 and DealerAceFour == 0):
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour)
															time.sleep(2)
															print("The Dealer has gone bust so you won $" ,str(Bet) + "!")
															Money += 2 * Bet
															input("Press Enter to continue...")
															continue

											if (DealerTotal > 21 and DealerAceOne ==1 and DealerAceTwo ==1 and DealerAceThree ==1 and DealerAceFour == 1):
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour)
															time.sleep(2)
															print("The Dealer has gone bust so you won $" ,str(Bet) + "!")
															Money += 2 * Bet
															input("Press Enter to continue...")
															continue
											if (DealerTotal > 17 and DealerTotal < 21):
															if (DealerTotal > Total):
																			os.system('clear')
																			print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour + " "+ParL + str(DealerTotal) + ParR)
																			print("Your Hand: " + CardOne + ", " + CardTwo + " "+ParL + str(Total) + ParR + "          Money left: $" , int(Money))
																			print("The Dealer won so you lost $" ,str(Bet) + ".")
																			
																			input("Press Enter to continue...")
																			continue

															if (DealerTotal < Total):
																			os.system('clear')
																			print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + DealerThree + DealerFour + " "+ParL + str(DealerTotal) + ParR)
																			print("Your Hand: " + CardOne + ", " + CardTwo +" "+ ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																			print("Congrats you have beaten the dealer and made $"+ str(Bet) + "!" )
																			Money += 2 * Bet
																			input("Press Enter to continue...")
																			continue

															if (DealerTotal  == Total):
																			os.system('clear')
																			print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + DealerThree + DealerFour + " "+ParL + str(DealerTotal) + ParR)
																			print("Your Hand: " + CardOne + ", " + CardTwo + " "+ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																			print("The game is a draw. Your money has been returned.")
																			input("Press Enter to continue...")
																			Money += Bet
																			continue
															

											if (DealerTotal == 21):
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour)
															time.sleep(2)
															print("The Dealer has made 21 and you lost $" ,str(Bet) + ".")
															
															input("Press Enter to continue...")
															continue
															

											if (DealerTotal < 17 ):
															DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerFourScore + DealerFiveScore + DealerAceOne + DealerAceTwo + DealerAceThree + DealerAceFour+ DealerAceFive

															if (DealerTotal > 21 and DealerAceOne > 5):
																			DealerAceOne = 1
																			DealerOneScore = 0
															
															if (DealerTotal > 21 and DealerAceTwo > 2):
																			DealerAceTwo = 1
																			DealerTwoScore = 0
															

															if (DealerTotal > 21 and DealerAceThree > 2):
																			DealerAceThree = 1
																			DealerThreeScore = 0

															if (DealerTotal > 21 and DealerAceFour > 2):
																			DealerAceFour = 1 
																			DealerFourScore = 0
															
															if (DealerTotal > 21 and DealerAceFour > 2):
																			DealerAceFive = 1
																			DealerFiveScore = 0

															
															DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerFourScore + DealerFiveScore + DealerAceOne + DealerAceTwo + DealerAceThree + DealerAceFour+ DealerAceFive

											
															if (DealerTotal > 17 and DealerTotal < 21):
																if (DealerTotal > Total):
																			os.system('clear')
																			print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ParL + str(DealerTotal) + ParR)
																			print("Your Hand: " + CardOne + ", " + CardTwo + " "+ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																			print("The Dealer won so you lost $" ,str(Bet) + ".")
																				
																			input("Press Enter to continue...")
																			continue
																			
																if (DealerTotal < Total):
																			os.system('clear')
																			print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ParL + str(DealerTotal) + ParR)
																			print("Your Hand: " + CardOne + ", " + CardTwo + " "+ParL + str(Total) + ParR + "          Money left: $" , int(Money))
																			print("Congrats you have beaten the dealer and made $"+ str(Bet) + "!" )
																			Money += 2 * Bet
																			input("Press Enter to continue...")
																			continue

																if (DealerTotal  == Total):
																			os.system('clear')
																			print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ParL + str(DealerTotal) + ParR)
																			print("Your Hand: " + CardOne + ", " + CardTwo + " "+ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																			print("The game is a draw. Your money has been returned.")
																			input("Press Enter to continue...")
																			Money += Bet
																			continue

																			

															if (DealerTotal > 21 and DealerAceOne == 0 and DealerAceTwo == 0 and DealerAceThree == 0 and DealerAceFour == 0 and DealerAceFive == 0):
																print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour+ ", " + DealerFive + " " + ParL + str(DealerTotal) + ParR)
																time.sleep(2)
																print("The Dealer has gone bust so you won $" ,str(Bet) + "!")
																Money += 2 * Bet
																input("Press Enter to continue...")
																continue

															if (DealerTotal > 21 and DealerAceOne ==1 and DealerAceTwo ==1 and DealerAceThree ==1 and DealerAceFour == 1):
																			print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour + ", " + DealerFive + " " +ParL + str(DealerTotal) + ParR)
																			time.sleep(2)
																			print("The Dealer has gone bust so you won $" ,str(Bet) + "!")
																			Money += 2 * Bet
																			input("Press Enter to continue...")
																			continue

															if (DealerTotal == 21):
																			print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour + ", " + DealerFive)
																			time.sleep(2)
																			print("The Dealer has made 21 so you lost $" ,str(Bet) + ".")
																			
																			input("Press Enter to continue...")
																			continue
							#Round Three
			else:
				print("Invalid input. Please restart.")
				exit()
			time.sleep(1)
			HitStayTwo = str(input("Would you like to hit (h) or stay (s)?"))
			HitStayTwo = HitStayTwo.lower()
			if (HitStayTwo == "h" or HitStayTwo == "hit"):

							os.system('clear')
							Total = CardOneScore + CardTwoScore + CardThreeScore + CardFourScore + AceOne + AceTwo + AceThree + AceFour
							if (Total > 21 and AceOne > 5):
											AceOne = 1
											CardOneScore = 0
							
							if (Total > 21 and AceTwo > 2):
											AceTwo = 1
											CardTwoScore = 0
							
							if (Total > 21 and AceThree > 2):
											AceThree = 1
											CardThreeScore = 0
							if (Total > 21 and AceFour > 2):
											AceFour = 1 
											CardFourScore = 0

							

							Total = CardOneScore + CardTwoScore + CardThreeScore + CardFourScore + AceOne + AceTwo + AceThree + AceFour

							print("Your cards are: " + CardOne + ", " + CardTwo + ", " + CardThree + ", " + CardFour + " " + ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
							print("The Dealer's face up card is: " + DealerOne)

							if (Total > 21 and AceTwo == 1 and AceOne == 1 and AceThree == 1):
											os.system('clear')
											print("Dealer's Hand: " + DealerOne + ", " + DealerTwo)
											print("Your hand: " + CardOne + ", " + CardTwo + ", " + CardThree + ", " + CardFour + " " + ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
											print("You have gone bust and have lost $" ,str(Bet) + "." )
											
											input("Press Enter to continue...")
											continue

							if (Total > 21 and AceOne == 0 and AceTwo == 0 and AceThree == 0):
											os.system('clear')
											print("Dealer's Hand: " + DealerOne + ", " + DealerTwo)
											print("Your hand: " + CardOne + ", " + CardTwo + ", " + CardThree + ", " + CardFour + " " + ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
											print("You have gone bust and have lost $" ,str(Bet) + "." )
											
											input("Press Enter to continue...")
											continue

							if (Total == 21):
											os.system('clear')
											print("Dealer's Hand: " + DealerOne + ", " + DealerTwo)
											print("Your hand: " + CardOne + ", " + CardTwo + ", " + CardThree + ", " + CardFour + " " + ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
											print("Congrats you have beaten the dealer and won $" ,str(Bet) + "!" )
											Money += 2 * Bet
											input("Press Enter to continue...")
											continue

							if Total > 21:
											os.system('clear')
											print("Your cards are: " + CardOne + ", " + CardTwo +", " + CardThree + " " + ParL + str(Total) + ParR +  "          Money left: $" , int(Money) )
											print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " and " + DealerThree)
											print("You have gone bust and have lost $" ,str(Bet) + "." )
							
											input("Press Enter to continue...")
											continue

							#Dealer Turn Two
			elif (HitStayTwo == "s" or HitStayTwo == "stay"):
							os.system('clear')

							DealerTotal = DealerOneScore + DealerTwoScore + DealerAceOne + DealerAceTwo
							
							
							if (DealerTotal > 21 and DealerAceOne > 5):
															DealerAceOne = 1
															DealerOneScore = 0
															DealerTotal = DealerOneScore + DealerTwoScore + DealerAceOne + DealerAceTwo
											
							if (DealerTotal > 21 and DealerAceTwo > 2):
															DealerAceTwo = 1
															DealerTwoScore = 0
															DealerTotal = DealerOneScore + DealerTwoScore + DealerAceOne + DealerAceTwo
							if (DealerTotal > 21 and DealerAceThree > 2):
															DealerAceThree = 1
															DealerThreeScore = 0

															DealerTotal = DealerOneScore + DealerTwoScore + DealerAceOne + DealerAceTwo

							if (DealerTotal > 21 and DealerAceOne == 0 and DealerAceTwo == 0 and DealerAceThree == 0):
											os.system('clear')
											print("Your hand: " + CardOne + " and " + CardTwo + ", " + CardThree + " "+ ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
											print("Dealer's Hand: " + DealerOne + " and " + DealerTwo)
											print("The Dealer has gone bust so you made $"+ str(Bet) + "!" )
											Money += 2 * Bet
											input("Press Enter to continue...")
											continue
											
											
											exit()
							if (DealerTotal >= 17 and DealerTotal < 21):
											if (DealerTotal > Total):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + " and " + DealerTwo + " "+ParL + str(DealerTotal) + ParR)
															print("Your Hand: " + CardOne + ', ' + CardTwo + ", " +CardThree + " "+  ParL + str(Total) + ParR+ "          Money left: $" , int(Money) )
															print("The Dealer won so you lost $" ,str(Bet) + ".")
															
															input("Press Enter to continue...")
															continue
											if (DealerTotal < Total):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " "+ParL + str(DealerTotal) + ParR)
															print("Your Hand: " + CardOne + ', ' + CardTwo + ", "+ CardThree + " "+ ParL + str(Total) + ParR+ "          Money left: $" , int(Money) )
															print("Congrats you have beaten the dealer and made $"+ str(Bet) + "!" )
															Money += 2 * Bet
															input("Press Enter to continue...")
															continue
															
											if (DealerTotal  == Total):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " "+ParL + str(DealerTotal) + ParR)
															print("Your Hand: " + CardOne + ', ' + CardTwo + ", "+CardThree + " "+  ParL + str(Total) + ParR+  "          Money left: $" , int(Money) )
															print("The game is a draw. Your money has been returned.")
															input("Press Enter to continue...")
															Money += Bet
															continue
															
							elif (DealerTotal < 17):

							
											DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerAceOne + DealerAceTwo + DealerAceThree


											if (DealerTotal > 21 and DealerAceOne > 5):
															DealerAceOne = 1
															DealerOneScore = 0
											
											if (DealerTotal > 21 and DealerAceTwo > 2):
															DealerAceTwo = 1
															DealerTwoScore = 0
											if (DealerTotal > 21 and DealerAceThree > 2):
															DealerAceThree = 1
															DealerThreeScore = 0
							
											DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerAceOne + DealerAceTwo + DealerAceThree


											if (DealerTotal > 21 and DealerAceOne == 0 and DealerAceTwo == 0 and DealerAceThree == 0):
												print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " and " + DealerThree)
												time.sleep(2)
												print("The Dealer has gone bust so you won $" ,str(Bet) )
												Money += 2 * Bet
												input("Press Enter to continue...")
												continue
												
												
											
											if (DealerTotal >= 17 and DealerTotal < 21):
												if (DealerTotal > Total):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " and " + DealerThree+ " " + ParL + str(DealerTotal) + ParR)
															print("Your Hand: " + CardOne + ', ' + CardTwo + ", " +CardThree + " "+  ParL + str(Total) + ParR+  "          Money left: $" , int(Money) )
															print("The Dealer won so you lost $" ,str(Bet) + ".")
															
															input("Press Enter to continue...")
															continue

												if (DealerTotal < Total):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " and " + DealerThree+ " " + ParL + str(DealerTotal) + ParR)
															print("Your Hand: " + CardOne + ' and ' + CardTwo + ", " +CardThree + " "+  ParL + str(Total) + ParR+ "          Money left: $" , int(Money) )
															print("Congrats you have beaten the dealer and made $"+ str(Bet) + "!" )
															Money += 2 * Bet
															input("Press Enter to continue...")
															continue

												if (DealerTotal  == Total):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " and " + DealerThree+ " " + ParL + str(DealerTotal) + ParR)
															print("Your Hand: " + CardOne + ', ' + CardTwo + ", " +CardThree + " "+  ParL + str(Total) + ParR+  "          Money left: $" , int(Money) )
															print("The game is a draw. Your money has been returned.")
															input("Press Enter to continue...")
															Money += Bet
															continue
															
															

												if (DealerTotal > 21 and DealerAceOne ==1 and DealerAceTwo ==1 and DealerAceThree ==1):
																print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " and " + DealerThree)
																time.sleep(2)
																print("The Dealer has gone bust so you won $" ,str(Bet) + "!" )
																Money += 2 * Bet
																input("Press Enter to continue...")
																continue

												if (DealerTotal == 21):
																print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " and " + DealerThree)
																time.sleep(2)
																print("The Dealer has made 21 and you lose $" ,str(Bet) + ".")
																	
																input("Press Enter to continue...")
																continue

												if (DealerTotal < 17 ):
																DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerFourScore + DealerAceOne + DealerAceTwo + DealerAceThree + DealerAceFour

																if (DealerTotal > 21 and DealerAceOne > 5):
																				DealerAceOne = 1
																				DealerOneScore = 0
																
																if (DealerTotal > 21 and DealerAceTwo > 2):
																				DealerAceTwo = 1
																				DealerTwoScore = 0
											

																if (DealerTotal > 21 and DealerAceThree > 2):
																				DealerAceThree = 1
																				DealerThreeScore = 0

																if (DealerTotal > 21 and DealerAceFour > 2):
																				DealerAceFour = 1 
																				DealerFourScore = 0

											
											DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerFourScore + DealerAceOne + DealerAceTwo + DealerAceThree + DealerAceFour

											if (DealerTotal > 21 and DealerAceOne == 0 and DealerAceTwo == 0 and DealerAceThree == 0 and DealerAceFour == 0):
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour)
															time.sleep(2)
															print("The Dealer has gone bust so you won $" ,str(Bet) + "!")
															Money += 2 * Bet
															input("Press Enter to continue...")
															continue

											if (DealerTotal > 21 and DealerAceOne ==1 and DealerAceTwo ==1 and DealerAceThree ==1 and DealerAceFour == 1):
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour)
															time.sleep(2)
															print("The Dealer has gone bust so you won $" ,str(Bet) + "!")
															Money += 2 * Bet
															input("Press Enter to continue...")
															continue
											if (DealerTotal > 17 and DealerTotal < 21):
															if (DealerTotal > Total):
																			os.system('clear')
																			print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour + " "+ParL + str(DealerTotal) + ParR)
																			print("Your Hand: " + CardOne + ", " + CardTwo + ", "+CardThree + " "+ ParL + str(Total) + ParR + "          Money left: $" , int(Money))
																			print("The Dealer won so you lost $" ,str(Bet) + ".")
																			
																			input("Press Enter to continue...")
																			continue

															if (DealerTotal < Total):
																			os.system('clear')
																			print("Dealer's Hand: " + DealerOne + ", " + DealerTwo +", "+ DealerThree +", "+ DealerFour + " "+ParL + str(DealerTotal) + ParR)
																			print("Your Hand: " + CardOne + ", " + CardTwo +", "+CardThree + " "+  ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																			print("Congrats you have beaten the dealer and made $"+ str(Bet) + "!" )
																			Money += 2 * Bet
																			input("Press Enter to continue...")
																			continue

															if (DealerTotal  == Total):
																			os.system('clear')
																			print("Dealer's Hand: " + DealerOne + ", " + DealerTwo +", "+ DealerThree +", "+ DealerFour + " "+ParL + str(DealerTotal) + ParR)
																			print("Your Hand: " + CardOne + ", " + CardTwo + ", "+CardThree + " "+ ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																			print("The game is a draw. Your money has been returned.")
																			input("Press Enter to continue...")
																			Money += Bet
																			continue
															

											if (DealerTotal == 21):
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + " and " + DealerFour)
															time.sleep(2)
															print("The Dealer has made 21 and you lost $" ,str(Bet) + ".")
															
															input("Press Enter to continue...")
															continue
															

											if (DealerTotal < 17 ):
															DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerFourScore + DealerFiveScore + DealerAceOne + DealerAceTwo + DealerAceThree + DealerAceFour+ DealerAceFive

															if (DealerTotal > 21 and DealerAceOne > 5):
																			DealerAceOne = 1
																			DealerOneScore = 0
															
															if (DealerTotal > 21 and DealerAceTwo > 2):
																			DealerAceTwo = 1
																			DealerTwoScore = 0
															

															if (DealerTotal > 21 and DealerAceThree > 2):
																			DealerAceThree = 1
																			DealerThreeScore = 0

															if (DealerTotal > 21 and DealerAceFour > 2):
																			DealerAceFour = 1 
																			DealerFourScore = 0
															
															if (DealerTotal > 21 and DealerAceFour > 2):
																			DealerAceFive = 1
																			DealerFiveScore = 0

															
															DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerFourScore + DealerFiveScore + DealerAceOne + DealerAceTwo + DealerAceThree + DealerAceFour+ DealerAceFive

											
											if (DealerTotal > 17 and DealerTotal < 21):
															if (DealerTotal > Total):
																			os.system('clear')
																			print("Dealer's Hand: " + DealerOne + " and " + DealerTwo + ParL + str(DealerTotal) + ParR)
																			print("Your Hand: " + CardOne + ", " + CardTwo + ", "+CardThree + " "+ ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																			print("The Dealer won so you lost $" ,str(Bet) + ".")
																				
																			input("Press Enter to continue...")
																			continue
																			
															if (DealerTotal < Total):
																			os.system('clear')
																			print("Dealer's Hand: " + DealerOne + " and " + DealerTwo + ParL + str(DealerTotal) + ParR)
																			print("Your Hand: " + CardOne + ", " + CardTwo + ", "+CardThree + " "+ ParL + str(Total) + ParR + "          Money left: $" , int(Money))
																			print("Congrats you have beaten the dealer and made $"+ str(Bet) + "!" )
																			Money += 2 * Bet
																			input("Press Enter to continue...")
																			continue

															if (DealerTotal  == Total):
																			os.system('clear')
																			print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ParL + str(DealerTotal) + ParR)
																			print("Your Hand: " + CardOne + ", " + CardTwo + ", "+CardThree + " "+ ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																			print("The game is a draw. Your money has been returned.")
																			input("Press Enter to continue...")
																			Money += Bet
																			continue
																			

											if (DealerTotal > 21 and DealerAceOne == 0 and DealerAceTwo == 0 and DealerAceThree == 0 and DealerAceFour == 0 and DealerAceFive == 0):
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour+ ", " + DealerFive + " " + ParL + str(DealerTotal) + ParR)
															time.sleep(2)
															print("The Dealer has gone bust so you won $" ,str(Bet) + "!")
															Money += 2 * Bet
															input("Press Enter to continue...")
															continue

											if (DealerTotal > 21 and DealerAceOne ==1 and DealerAceTwo ==1 and DealerAceThree ==1 and DealerAceFour == 1):
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour + ", " + DealerFive + " " +ParL + str(DealerTotal) + ParR)
															time.sleep(2)
															print("The Dealer has gone bust so you won $" ,str(Bet) + "!")
															Money += 2 * Bet
															input("Press Enter to continue...")
															continue

											if (DealerTotal == 21):
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour + ", " + DealerFive)
															time.sleep(2)
															print("The Dealer has made 21 so you lost $" ,str(Bet) + ".")
															
															input("Press Enter to continue...")
															continue

			else:
				print("Invalid input. Please restart.")
				exit()		
			time.sleep(1)
			HitStayThree = str(input("Would you like to hit (h) or stay (s)?"))

			HitStayThree = HitStayThree.lower()
			if (HitStayThree == "h" or HitStayThree == "hit"):

											os.system('clear')

											Total = CardOneScore + CardTwoScore + CardThreeScore + CardFourScore + CardFiveScore + AceOne + AceTwo + AceThree +  AceFour + AceFive

											if (Total > 21 and AceOne > 5):
															AceOne = 1
															CardOneScore = 0
															
											if (Total > 21 and AceTwo > 2):
															AceTwo = 1
															CardTwoScore = 0
															
											if (Total > 21 and AceThree > 2):
															AceThree = 1
															CardThreeScore = 0

											if (Total > 21 and AceFour > 2):
															AceFour = 1 
															CardFourScore = 0
											
											if (Total > 21 and AceFive > 2):
															AceFive = 1
															CardFiveScore = 0
															
											
											Total = CardOneScore + CardTwoScore + CardThreeScore + CardFourScore + CardFiveScore + AceOne + AceTwo + AceThree + AceFour + AceFive

											print("Your cards are: " + CardOne + ", " + CardTwo + ", " + CardThree + ", " + CardFour + ", "+ CardFive+" " + ParL + str(Total) + ParR + "          Money left: $" , int(Money))
											print("The Dealer's face up card is: " + DealerOne)

											if (Total > 21 and AceTwo == 1 and AceOne == 1 and AceThree == 1):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo)
															print("Your cards are: " + CardOne + ", " + CardTwo + ", " + CardThree + ", " + CardFour + ", "+ CardFive+" " + ParL + str(Total) + ParR + "          Money left: $" , int(Money))
															print("You have gone bust and have lost $"+ str(Bet) + "." )
															
															input("Press Enter to continue...")
															continue
											
											

											if (Total > 21 and AceOne == 0 and AceTwo == 0 and AceThree == 0):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo)
															print("Your cards are: " + CardOne + ", " + CardTwo + ", " + CardThree + ", " + CardFour + ", "+ CardFive+" " + ParL + str(Total) + ParR + "          Money left: $" , int(Money))
															print("You have gone bust and have lost $"+ str(Bet) + "." )
															
															input("Press Enter to continue...")
															continue

											if (Total == 21):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo)
															print("Your cards are: " + CardOne + ", " + CardTwo + ", " + CardThree + ", " + CardFour + ", "+ CardFive+" " + ParL + str(Total) + ParR + "          Money left: $" , int(Money))
															print("Congrats you have beaten the dealer and won $" ,str(Bet) + "!")
															Money += 2 * Bet
															input("Press Enter to continue...")
															continue

											if (Total <= 20):
															os.system('clear')
															print("Dealer's Hand: " + DealerOne + ", " + DealerTwo)
															print("Your cards are: " + CardOne + ", " + CardTwo + ", " + CardThree + ", " + CardFour + ", "+ CardFive+" " + ParL + str(Total) + ParR + "          Money left: $" , int(Money))
															print("You have 5 cards and are not busted. You have beaten the dealer and won $" ,str(Bet) + "!" )
															Money += 2 * Bet
															input("Press Enter to continue...")
															continue
											if Total > 21:
												os.system('clear')
												print("Your cards are: " + CardOne + ", " + CardTwo +", " + CardThree + " " + ParL + str(Total) + ParR +  "          Money left: $" , int(Money) )
												print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " and " + DealerThree)
												print("You have gone bust and have lost $" ,str(Bet) + "." )
								
												input("Press Enter to continue...")
												continue

			#Dealer Turn Three
			elif  (HitStayThree == "s" or HitStayThree == "stay"):
											DealerTotal = DealerOneScore + DealerTwoScore + DealerAceOne + DealerAceTwo
															
															
											if (DealerTotal > 17 and DealerTotal < 21):
															if (DealerTotal > Total):
																							os.system('clear')
																							print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ParL + str(DealerTotal) + ParR)
																							print("Your Hand: " + CardOne + ", " + CardTwo + ", " + CardThree + ", " + CardFour + " " + ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																							print("The Dealer won so you lost $" ,str(Bet) + ".")
																							
																							input("Press Enter to continue...")
																							continue
											if (DealerTotal < Total):
																							os.system('clear')
																							print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " " + ParL + str(DealerTotal) + ParR)
																							print("Your Hand: " + CardOne + ", " + CardTwo + ", " + CardThree + ", " + CardFour + " " + ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																							print("Congrats you have beaten the dealer and made $"+ str(Bet) + "!" )
																							Money += 2 * Bet
																							input("Press Enter to continue...")
																							continue
											if (DealerTotal  == Total):
																							os.system('clear')
																							print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " " + ParL + str(DealerTotal) + ParR)
																							print("Your Hand: " + CardOne + ", " + CardTwo + ", " + CardThree + ", " + CardFour + " " + ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																							print("The game is a draw. Your money has been returned.")
																							input("Press Enter to continue...")
																							Money += Bet
																							continue


											if (DealerTotal < 17):
															
												DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerAceOne + DealerAceTwo + DealerAceThree

												if (DealerTotal > 21 and DealerAceOne > 5):
																								DealerAceOne = 1
																								DealerOneScore = 0
																				
												if (DealerTotal > 21 and DealerAceTwo > 2):
																								DealerAceTwo = 1
																								DealerTwoScore = 0
												if (DealerTotal > 21 and DealerAceThree > 2):
																								DealerAceThree = 1
																								DealerThreeScore = 0
															
															

												DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerAceOne + DealerAceTwo + DealerAceThree
																
												if (DealerTotal > 21 and DealerAceOne == 0 and DealerAceTwo == 0 and DealerAceThree == 0):
																				print("Dealer's Hand:" + DealerOne + ", " + DealerTwo + ", " + DealerThree)
																				time.sleep(2)
																				print("The Dealer has gone bust so you won $" ,str(Bet) + "!")
																				Money += 2 * Bet
																				input("Press Enter to continue...")
																				continue

												if (DealerTotal > 21 and DealerAceOne ==1 and DealerAceTwo ==1 and DealerAceThree ==1):
																				print("Dealer's Hand:" + DealerOne + ", " + DealerTwo + ", " + DealerThree)
																				time.sleep(2)
																				print("The Dealer has gone bust so you win $" ,str(Bet) + "!")
																				Money += 2 * Bet
																				input("Press Enter to continue...")
																				continue
												if (DealerTotal > 17 and DealerTotal <= 21):

																				
																if (DealerTotal > Total):
																								os.system('clear')
																								print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + " " + ParL + str(DealerTotal) + ParR)
																								print("Your Hand: " + CardOne + ", " + CardTwo + ", " + CardThree + ", " + CardFour + " " + ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																								print("The Dealer won so you lost $" ,str(Bet) + ".")
																								
																								input("Press Enter to continue...")
																								continue
																if (DealerTotal < Total):
																								os.system('clear')
																								print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + " " + ParL + str(DealerTotal) + ParR)
																								print("your Hand: " + CardOne + ", " + CardTwo + ", " + CardThree + ", " + CardFour + " " + ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																								print("Congrats you have beaten the dealer and made $"+ str(Bet) + "!" )
																								Money += 2 * Bet
																								input("Press Enter to continue...")
																								continue                                                
																if (DealerTotal  == Total):
																								os.system('clear')
																								print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + " " + ParL + str(DealerTotal) + ParR)
																								print("Your Hand: " + CardOne + ", " + CardTwo + ", " + CardThree + ", " + CardFour + " " + ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																								print("The game is a draw. Your money has been returned.")
																								input("Press Enter to continue...")
																								Money += Bet
																								continue
																								

																if (DealerTotal == 21 and Total < 21):
																				print("Dealer's Hand:" + DealerOne + ", " + DealerTwo + ", " + DealerThree)
																				time.sleep(2)
																				print("The Dealer has made 21 so you lost $" ,str(Bet) + ".")
																				
																				input("Press Enter to continue...")
																				continue

												if (DealerTotal < 17 ):
													DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerFourScore + DealerAceOne + DealerAceTwo + DealerAceThree + DealerAceFour


													if (DealerTotal > 17 and DealerTotal <= 21):
														if (DealerTotal > Total):
																						os.system('clear')
																						print("Dealer's Hand: " + DealerOne + ", " + DealerTwo +" "+ ParL + str(Total) + ParR)
																						print("Your Hand: " + CardOne + ", " + CardTwo + ", "+CardThree + ", "+ CardFour + " " +ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																						print("The Dealer won so yoy lost $" ,str(Bet) + ".")
																						
																						input("Press Enter to continue...")
																						continue
														
														if (DealerTotal < Total):
																						os.system('clear')
																						print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " "+ParL + str(Total) + ParR)
																						print("Your Hand: " + CardOne + ", " + CardTwo + " "+", "+CardThree + ", "+ CardFour + " " +ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																						print("Congrats you have beaten the dealer and made $"+ str(Bet) + "!" )
																						Money += 2 * Bet
																						input("Press Enter to continue...")
																						continue
														if (DealerTotal  == Total):
																						os.system('clear')
																						print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " "+ParL + str(Total) + ParR)
																						print("Your Hand: " + CardOne + ", " + CardTwo + " "+", "+CardThree + ", "+ CardFour + " " +ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																						print("The game is a draw. Your money has been returned.")
																						input("Press Enter to continue...")
																						Money += Bet
																						continue
																													



														if (DealerTotal > 21 and DealerAceOne > 5):
																		DealerAceOne = 1
																		DealerOneScore = 0
														
														if (DealerTotal > 21 and DealerAceTwo > 2):
																		DealerAceTwo = 1
																		DealerTwoScore = 0
														

														if (DealerTotal > 21 and DealerAceThree > 2):
																		DealerAceThree = 1
																		DealerThreeScore = 0

														if (DealerTotal > 21 and DealerAceFour > 2):
																		DealerAceFour = 1 
																		DealerFourScore = 0
																	
														DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerFourScore + DealerAceOne + DealerAceTwo + DealerAceThree + DealerAceFour


													if (DealerTotal > 21 and DealerAceOne == 0 and DealerAceTwo == 0 and DealerAceThree == 0 and DealerAceFour == 0):
																print("Dealer's Hand: "+DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour)
																time.sleep(2)
																print("The Dealer has gone bust so you won $" ,str(Bet) + ".")
																Money += 2 * Bet
																input("Press Enter to continue...")
																continue

													if (DealerTotal > 17 and DealerTotal < 21):
																				if (DealerTotal > Total):
																								os.system('clear')
																								print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " "+ ParL + str(Total) + ParR)
																								print("Your Hand: " + CardOne + ", " + CardTwo +", "+CardThree + ", "+ CardFour + " " +ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																								print("The Dealer won so you lost $" ,str(Bet) + ".")
																								
																								input("Press Enter to continue...")
																								continue
																				if (DealerTotal < Total):
																								os.system('clear')
																								print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " "+ParL + str(Total) + ParR)
																								print("Your Hand: " + CardOne + ", " + CardTwo + ", "+CardThree + ", "+ CardFour + " " +ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																								print("Congrats you have beaten the dealer and made $"+ str(Bet) + "!" )
																								Money += 2 * Bet
																								input("Press Enter to continue...")
																								continue
																				if (DealerTotal  == Total):
																								os.system('clear')
																								print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + " "+ParL + str(Total) + ParR)
																								print("Your Hand: " + CardOne + ", " + CardTwo + ", "+CardThree + ", "+ CardFour + " " +ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																								print("The game is a draw. Your money has been returned.")
																								input("Press Enter to continue...")
																								Money += Bet
																								continue
																												

													if (DealerTotal > 21 and DealerAceOne ==1 and DealerAceTwo ==1 and DealerAceThree ==1 and DealerAceFour == 1):
																				print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour)
																				time.sleep(2)
																				print("The Dealer has gone bust so you win $" ,str(Bet) + "!")
																				Money += 2 * Bet
																				input("Press Enter to continue...")
																				continue

													if (DealerTotal == 21 and Total < 21):
																				print(DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour)
																				time.sleep(2)
																				print("The Dealer has made 21 so you lost $" ,str(Bet) + ".")
																				
																				input("Press Enter to continue...")
																				continue



													if (DealerTotal < 17 ):
																DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerFourScore + DealerFiveScore + DealerAceOne + DealerAceTwo + DealerAceThree + DealerAceFour+ DealerAceFive

																if (DealerTotal > 21 and DealerAceOne > 5):
																				DealerAceOne = 1
																				DealerOneScore = 0
																
																if (DealerTotal > 21 and DealerAceTwo > 2):
																				DealerAceTwo = 1
																				DealerTwoScore = 0
																

																if (DealerTotal > 21 and DealerAceThree > 2):
																				DealerAceThree = 1
																				DealerThreeScore = 0

																if (DealerTotal > 21 and DealerAceFour > 2):
																				DealerAceFour = 1 
																				DealerFourScore = 0
																
																if (DealerTotal > 21 and DealerAceFour > 2):
																				DealerAceFive = 1
																				DealerFiveScore = 0

																DealerTotal = DealerOneScore + DealerTwoScore + DealerThreeScore + DealerFourScore + DealerFiveScore + DealerAceOne + DealerAceTwo + DealerAceThree + DealerAceFour+ DealerAceFive

																if (DealerTotal > 21 and DealerAceOne == 0 and DealerAceTwo == 0 and DealerAceThree == 0 and DealerAceFour == 0 and DealerAceFive == 0):
																				print("Dealer's Hand:" + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour+ ", " + DealerFive)
																				time.sleep(2)
																				print("The Dealer has gone bust so you win $" ,str(Bet) + "!")
																				Money += 2 * Bet
																				input("Press Enter to continue...")
																				continue

																if (DealerTotal > 21 and DealerAceOne ==1 and DealerAceTwo ==1 and DealerAceThree ==1 and DealerAceFour == 1):
																				print("Dealer's Hand:" + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour + ", " + DealerFive)
																				time.sleep(2)
																				print("The Dealer has gone bust so you win $" ,str(Bet) + "!")
																				Money += 2 * Bet
																				input("Press Enter to continue...")
																				continue
																if (DealerTotal > 17 and DealerTotal < 21):
																				if (DealerTotal > Total):
																								os.system('clear')
																								print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour + ", "+ DealerFive+ " " + ParL + DealerTotal +ParR)
																								print("Your Hand: " + CardOne + ", " + CardTwo + ", "+CardThree + ", "+ CardFour + " " +ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																								print("The Dealer won so you lost $" ,str(Bet) + ".")
																								
																								input("Press Enter to continue...")
																								continue

																				if (DealerTotal < Total):
																								os.system('clear')
																								print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour + ", "+ DealerFive+ " " + ParL + DealerTotal +ParR)
																								print("Your Hand: " + CardOne + ", " + CardTwo + ", "+CardThree + ", "+ CardFour + " " +ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																								print("Congrats you have beaten the dealer and made $"+ str(Bet) + "!" )
																								Money += 2 * Bet
																								input("Press Enter to continue...")
																								continue

																				if (DealerTotal  == Total):
																								os.system('clear')
																								print("Dealer's Hand: " + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour + " and "+ DealerFive+ " " + ParL + DealerTotal +ParR)
																								print("Your Hand: " + CardOne + ', ' + CardTwo + ", "+CardThree + ", "+ CardFour + " " +ParL + str(Total) + ParR+ "          Money left: $" , int(Money))
																								print("The game is a draw. Your money has been returned.")
																								input("Press Enter to continue...")
																								Money += Bet
																								continue
																						
																if (DealerTotal == 21 and Total < 21):
																						print("Dealer's Hand:" + DealerOne + ", " + DealerTwo + ", " + DealerThree + ", " + DealerFour + " and " + DealerFive)
																						time.sleep(2)
																						print("The Dealer has made 21 so you lost $" ,str(Bet) + ".")
																						
																						input("Press Enter to continue...")
																						continue

'''

