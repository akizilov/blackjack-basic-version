import random
cash = 100
state = 1


def card_addition(list):
    total_value = 0
    for card in list:
        total_value = total_value + card
    return total_value







print("Welcome to blackjack. If you would like to play, type '1' and enter your desired bet amount. Your current balance is "+str(cash)+".")




while state == 1: #while the game is running
    print()
    if cash == "0":                 #Checks if user can bet
        break
    bet = int(input("Enter your bet amount: "))     #asks for bet
    while bet > cash: #Checks if bet excedes bank account
        print("Your bet cannot excede your bank balance of "+str(cash)+". Please try again.")
        print()
        bet = int(input("Enter your bet: "))
    dealers_cards = []  #assigns dealer card list
    card_select = random.randint(1,11)
    dealers_cards.append(card_select)
    dealers_total = card_addition(dealers_cards)
    users_cards = []    #assigns user card list
    dealer_hidden_card = random.randint(1,11)   #assigns the dealers hidden card
    users_second_card = random.randint(1,11)
    users_cards.append(users_second_card)
    status = "hit"
    time = 0 #keeps track for the blackjack
    
    
    while status == "hit": #while you keep hitting 
        time += 1       
        card_select = random.randint(1,11)   
        users_cards.append(card_select) 
        users_total = card_addition(users_cards)
        print()
        
        
        if users_total == 21:   
            dealers_cards.append(dealer_hidden_card)
            dealers_total = card_addition(dealers_cards)
            print("Dealer's cards: "+str(dealers_cards))
            print("Dealer's total: "+str(dealers_total))
            print()
            print("User's cards: "+str(users_cards))
            print("User's total: "+str(users_total))
            while dealers_total < 16:
                card_select = random.randint(1,11)
                dealers_cards.append(card_select)
                print(dealers_cards)
                dealers_total = card_addition(dealers_cards)
            if dealers_total < users_total:
                if time == 1:
                    print("BLACKJACK!")
                else:
                    print()
                    print("You won!")
                cash += bet
                break
            elif dealers_total == user_total:
                print("It's a tie!")
                #figure out how to continue using old bet
            else:
                print("You lost!")
                cash -= bet
                break
        elif users_total > 25:
            print("Bust!")
            cash -= bet
            break
        
        print("Dealer's cards: "+str(dealers_cards))
        print("Dealer's total: "+str(dealers_total))
        print()
        print("User's cards: "+str(users_cards))
        print("User's total cards: "+str(users_total))
        print()
        status = input("Would you like to hit or stand? Type 'hit' or 'stand': ")
        print("********************************************")
    if status == "stand":
        print()
        dealers_cards.append(dealer_hidden_card)
        dealers_total = card_addition(dealers_cards)
        
        while dealers_total < 16:
            card_select = random.randint(1,11)
            dealers_cards.append(card_select)
            print("Dealer's cards: "+str(dealers_cards))
            dealers_total = card_addition(dealers_cards)
        
        print("Dealers total: "+str(dealers_total))
        print()
        print("User's cards: "+str(users_cards))
        print("Your total: "+str(users_total))
        print()
        if dealers_total > 21 or users_total > dealers_total and users_total < 21:
            cash += bet
            print("You won!")
        elif dealers_total > users_total and dealers_total < 21:
            cash -= bet
            print("You lost")
        else:
            print('its a tie')
        
        print()
        print("Your bank balance is now "+str(cash)+".")      
        print()    
            
    print()       
    state = int(input("Would you like to play again? (1 - Play, 2 - Stop playing)"))
