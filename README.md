import random

class hilo:
    sentence = "\nWelcome to Hi-Lo! \nStart with 300 points. Each round a card will be be drawn and shown. \nSelect whether you think the 2nd card will be higher or lower than than the 1st card. \nIf you are right, you win 100 points, otherwise you lose 75 points. \nTry to make it to 700 points within 10 tries. Good luck!"
    def get_sentence(self):
        return self.sentence

intro = hilo()
print(intro.get_sentence())

starting_points = 300
current_points = starting_points
gameplay = True
current_round = 1
maximum_rounds = 10

class Card_Numbers:
    cards = {1:"Ace (1)", 2:"2", 3:"3", 4:"4", 5:"5", 6:"6", 7:"7", 8:"8", 9:"9", 10:"10", 11:"Jack (11)", 12:"Queen (12)", 13:"King (13)"}
    def get_cards(self):
        return self.cards

Something_Ridiculous = Card_Numbers()

Something_Ridiculous.get_cards()

def getCardValue():
    return random.randint(1,13)

def getCardStr(cardValue):
    return Something_Ridiculous.get_cards()[cardValue]

def getHLGuess():
    bet = ""
    while bet not in ["H","L","h","l"]:
        bet = input("Higher or Lower (H/L)?: ")

    if bet in ["H","h"]:
        return "HIGH"
    elif bet in ["L","l"]:
        return "LOW"
 
def playerGuessCorrect(card1, card2, betType):
    if (card1>card2 and betType=="LOW") or ((card1<card2 and betType=="HIGH")):
        return True
    else:
        return False









