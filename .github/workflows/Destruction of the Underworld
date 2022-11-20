import random  # imports

Combat = {'Excaliber': 50, 'Wooden_Sword': 15, 'Obsidian_Sword': 35,
          'Diamond_Gauntlets': 30, 'Punch':10}  # Setup dict. for all Shields, Swords, and Potions
Shields = {'Heroes_shield': 50, 'Bronze_Shield': 15, 'Diamond_Shield': 30, 'Obsidian_Shield': 35}
Potion = {'Blue_Heal': 50, 'Red_Heal': 40, 'Yellow_Heal': 30, 'Green_Heal': 20}
Option = [Combat, Potion, Shields]  # Inventory - when choosing to pick

Your_Weapon = {'Excaliber':Combat['Excaliber'], 'Wooden_Sword': Combat['Wooden_Sword'], 'Punch': Combat['Punch']}
Your_Potion = {'Green_Heal': Potion['Green_Heal']}
Your_Shield = {'Bronze_Shield': Shields['Bronze_Shield']}
Your_Health = {'Hp': 250}
Fight = {'Weapon': Your_Weapon}  # fighting options - includes Fight-potion a dict
Heal = {'Potions': Your_Potion}
Block = {'Shield': Your_Shield}
Inventory = [Fight, Heal, Block]
USerP = ['Weapon', 'Heal', 'Shield', 'Inventory']
W = ''
S = ''

Heroes = ('Noah', 'Brandon', 'Issac', 'Nate')  # Heroes (TUPLE) randomize
Picked_Hero = random.randrange(len(Heroes))

Mammon = {'Mammon_hp': 100, 'Punch': 10, 'Potion': 'Yellow_Heal', 'Parry':15}  # Creates Demon Guard
D_1_C = ''
Leviathan = {'Leviathan_hp': 250, 'Tail_Whip': 25, 'Potion': 'Yellow_Heal'}  # Creates Demon Lilith
Lucifer = {'Lucifer_hp': 500, 'Dragon_Claw': 50, 'Potion': Potion['Yellow_Heal']}  # Creates Demon Lucifer
Satan = {'Satan_hp': 1000, 'Storm-bringer': 100, 'Punch_OfDestruction': 1, 'Potion': Potion['Yellow_Heal']}  # Creates Demon Satan

Loot_1 = random.choice(list(random.choice(list(Option))))  # setup loots when playing the game
print(Loot_1)
Loot_2 = random.choice(list(random.choice(list(Option))))
print(Loot_2)
Loot_3 = random.choice(list(random.choice(list(Option)))
print(Loot_3)
Loot_4 = random.choice(list(random.choice(list(Option))))
print(Loot_4)

Choice = 'y'
while Choice != 'n':
    name = input('\nOpening your eyes a portal meets before your feet. The purple voids never ending swirl makes you '
                 'weary.\nYou clench your fist. You know can do this because your name is:', )  # entering your name
    print('\nLooking to your sides you are met with a group of heroes. {} is from the kingdom of the north. {} is '
          'from the kingdom of the south. {} is from the kingdom of the east. {} is from the kingdom of the '
          'west.'.format(Heroes[0], Heroes[1], Heroes[2], Heroes[3]))
    input('Any key to continue')

    print(
        '\n{} stands up I will go with you adventurer {}. The demon world stands beyond this void and we need to do '
        'everything we can to save this world from there evil violence'.format(
            Heroes[Picked_Hero], name))
    input('Any key to continue')

    print(
        '\nDemon: Who dare comes forth into the demon outpost.\n{}: I am the Mighty Hero {} and the Adventurer {}. \nYou: We '
        'have come to destroy this place and this dimension of demons who dare threatens our earth.'.format(
            Heroes[Picked_Hero], Heroes[Picked_Hero], name))
    input('Any key to continue')

    print('\nDemon: I will not let this happen as I am the Mammon the guardian of this outpost.\nFight.')
    while Mammon['Mammon_hp'] > 0:
        print('\nYour health is {}'.format(Your_Health['Hp']))
        print('Mammon Health is {}'.format(Mammon['Mammon_hp']))
        O_1 = input('{}>>'.format(USerP))

        if (len(Your_Potion) == 0) and (O_1 == 'Heal'):
            O_1 = 'reset'

        if O_1 == 'Weapon':
            W = input('Which Weapon would you like to use{}'.format(Your_Weapon))
            while W not in Your_Weapon:
                print('Enter one of the options')
                W = input('Which Weapon would you like to use{}'.format(Your_Weapon))
            print('You use {} damage {}'.format(W, Your_Weapon[W]))
        elif O_1 == 'Shield':
            S = input('Which Shield would you like to use {}'.format(Your_Shield))
            while S not in Your_Shield:
                print('Enter one of the options')
                S = input('Which Shield would you like to use{}'.format(Your_Shield))
            print('you use {} shield blocks {}'.format(S, Shields[S]))
        elif (O_1 == 'Heal') and (len(Your_Potion) > 0):
            print(len(Heal))
            P = input('Which Potion would you like to use {}'.format(Your_Potion))
            while P not in Your_Potion:
                print('Enter one of the options')
                P = input('Which Weapon would you like to use {}'.format(Your_Potion))
            print('You use {} it heals {}'.format(P, Potion[P]))
            Your_Health['Hp'] += Your_Potion[P]
            del Your_Potion[P]
        elif O_1 == 'Inventory':
            print(Inventory)
        else:
            print('\nEnter one of the options that contain an item')

        if (Mammon['Mammon_hp'] > 50) and (O_1 in USerP):
            print('Mammon uses Punch damage {}'.format(Mammon['Punch']))
        elif (Mammon['Mammon_hp'] <= 20) and (O_1 in USerP) and ('Potion' in Mammon):
            print('Mammon uses {} it heals {}'.format(Mammon['Potion'], Potion[Mammon['Potion']]))
            Mammon['Mammon_hp'] += Potion[Mammon['Potion']]
            del Mammon['Potion']
        elif (Mammon['Mammon_hp'] <= 50) and (O_1 in USerP):
            D_1_C = random.choice([Mammon['Punch'], Mammon['Parry']])
            if D_1_C == Mammon['Punch']:
                print('Mammon uses Punch damage {}'.format(Mammon['Punch']))
            elif D_1_C == Mammon['Parry']:
                print('Mammon uses Parry blocks {}'.format(Mammon['Parry']))
        if D_1_C == Mammon['Punch'] or (Mammon['Mammon_hp'] > 50):
            if O_1 != 'Shield':
                Your_Health['Hp'] -= Mammon['Punch']
            elif O_1 == 'Shield':
                if Your_Shield[S] >= Mammon['Punch']:  # This section allows for both parties action to work with one another
                    print('Blocks Mammons damage')
                elif Your_Shield[S] < Mammon['Punch']:
                    Your_Health['Hp'] -= ((Mammon['Punch'] - Your_Shield[S]) / 2)

        if O_1 == 'Weapon':
            if D_1_C == Mammon['Punch'] or Mammon['Mammon_hp'] > 50:
                Mammon['Mammon_hp'] -= Your_Weapon[W]
            elif D_1_C == Mammon['Parry']:
                if Mammon['Parry'] < Your_Weapon[W]:
                    Mammon['Mammon_hp'] -= Your_Weapon[W] - Mammon['Parry']
                elif Mammon['Parry'] >= Your_Weapon[W]:
                    print('Mammon negated your attack')


        if O_1 == 'Shield' and D_1_C == Mammon['Parry']:
            print('Nothing happened')

        if Your_Health['Hp'] <= 0:
            print('your health is now {}, you have died'.format(Your_Health['Hp']))
            break

    Loot_1
    print('In the ruckage you see an object portruding. You pick it up.\n You have now gained {}'.format(Loot_1))

    while Leviathan['Leviathan_hp'] > 0:
        O_2 = input('{}>>'.format(Option))

        if O_2 == 'Weapon':
            print('')
        elif O_2 == 'Shield':
            print('')

        elif O_2 == 'Potion':
            print('')

        else:
            print('Enter one of the options')
    Loot_2

    while Lucifer['Lucifer_hp'] > 0:
        O_3 = input('{}>>'.format(Option))

        if O_3 == 'Weapon':
            print('')
        elif O_3 == 'Shield':
            print('')

        elif O_3 == 'Potion':
            print('')

        else:
            print('Enter one of the options')
    Loot_3

    Loot_4
    while Satan['Satan_hp'] > 0:
        O_4 = input('{}>>'.format(Option))

        if O_4 == 'Weapon':
            print('')
        elif O_4 == 'Shield':
            print('')

        elif O_4 == 'Potion':
            print('')

        else:
            print('Enter one of the options')

    Choice = input('\nGame Over.\nWould You like to play again?(y, n)')
