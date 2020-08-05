Submitters:
Name: Lia Ismailov ID:209082197
Name: Mor Balilty ID: 307955740

Instructions:

1. To add ballot:
    a.Serial number is automatically generated so you will not be asked to enter one
    b.When entering an address: Enter street number and then city, when adding a city please write it in a single string for example: Tel-aviv
    c. Type of ballot is defined by numbers:
        0 -  for regular ballot
        1 - for military  ballot
        2 - for isolation 3 - for military and isolation

2. To add citizen:
    a. Enter the id and afterwards the year then name
        - if your id exists you will have the option to re-enter it
    b. To enter if a user is in isolation 0 for no and 1 for yes
    c. You can only choose from the ballots thar are printed to you
        - if you choose a ballot you cannot vote in yu will be redirected to the main menu
        - if there aren't ballots that you can vote it you are again redirected to the main menu with the correct message(not a case that can hap
        pen because in the init we make all type of ballots because it will be unfair if someone couldn't vote)

3. To add party:
    a. Enter first the name of a party
     -if party name already exists you will have the option to re enter one
    b. afterward the date year and month - When entering a month we expect it by number
    c. and the faction: 1 for left, 2 for right, 3 for center

4. To add a candidate:
    a. We first ask for id
        - If id exists we pull the existing user and only ask for what party he wants to belong to
        -If id doesnt exist look for section 2 - adding a citizen
    b. The parties are printed before the user - we assume the user will only choose from the parties before him

5. The election:
    a. We go one by one the citizens in the list and ask if they want to vote y - Yes n - no
    b. if you press yes:
        - if you are in isolation you will be asked if you are protected if not you will be sent to the main menu
    c. if you are protected and not in isolation the parties will be printed before you
    d. choose the party - if you choose a wrong party you will have another 3 attempts to choose an existing party


General:
-When you add a member to a party if the id exists in the data pool it adds the citizen as member to the party if its a new id, it creates
 the citizen and then adds it.
-When voting the citizen gets the the list of the parties and its members so he can do an educated choice.
-A user has 3 tries to choose a party
-We added a move c'tor to address because we wrote our own c'tor , in all the other function we put the c'tor
in private on porpuse to block the option of copying.
-While initializing the election we create every single type of ballot for easy testing but if a there is no appropriate ballot
for the citizen we print a message and the user is back to the main menu
-if a user types the wrong type of ballot he is sent back to the main menu
-if there isn't a ballot for a certain citizen the citizen cannot be created and sent back to the menu
