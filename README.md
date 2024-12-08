# Interactive-Casino

As a team member of the Interactive Casino project, my primary responsibility was designing and implementing the Blackjack game. This involved me creating a logical structure for the game, ensuring a seamless user experience, and also adhering to the rules of the traditional Blackjack game.
I started with the game mechanics, including the random card generation for both the player and the dealer, and implemented the comparison logic to determine the outcome of each round. The winning, losing, and tie scenarios were carefully coded to reflect the real-world dynamics of Blackjack. I also integrated a betting system that dynamically updates the player’s balance based on their performance in the game using pointer for the player balance.
To enhance user engagement and ensure clarity, I added detailed instructions for the game and implemented input validation to handle invalid bets. My work also focused on balancing simplicity and functionality, which enabled users to enjoy an authentic Blackjack experience in a simple and risk-free environment.
By coding the Blackjack module, I contributed to the overall modularity and functionality of the project, ensuring that it aligns with the goals of the Casino Game Simulator. My work highlights the strategic part of Blackjack while demonstrating the practical application of C programming concepts such as randomization, conditional statements, and functions. This module plays a vital role in offering users a comprehensive and enjoyable gaming experience.

My contribution, Code Snipet: 


`void blackjack(int *balance)
{
    int player_card, dealer_card, bet;

    printf("<---BlackJack--->\n\n");
    printf("Rules for BlackJack:\n");
    printf("1. Betting Rule: The player must place a bet before each round, and the bet cannot exceed their current balance or be less than or equal to zero.\n");
    printf("2. Card Values: Both the player and the dealer are randomly assigned a card value between 1 and 21. The player and dealer compare their cards, and the one with the higher card wins.\n");
    printf("3. Winning Rule: If the player's card value is greater than the dealer's, they win the round and gain the amount they bet.\n");
    printf("4. Losing Rule: If the dealer's card value is greater than the player's, the player loses their bet, and the balance is reduced accordingly.\n");
    printf("5. Draw Rule: If the player and dealer have the same card value, the round is a draw, and there is no change in the player's balance.\n\n");
    
    printf("Enter your bet: ");
    scanf("%d", &bet);

    if (bet > *balance || bet <= 0) 
    {
        printf("Invalid bet amount. Please try again.\n\n");
        return;
    }

    player_card = rand() % 21+1;
    dealer_card = rand() % 21+1;

    printf("Your card: %d\n", player_card);
    printf("Dealer's card: %d\n", dealer_card);

    if (player_card > dealer_card)
    {
        printf("Congratulations! You win!\n");
        *balance = *balance + bet;
    }
    else if (player_card < dealer_card)
    {
        printf("You Lose. Better luck next time!\n");
        *balance = *balance - bet;
    }
    else
    {
        printf("It's a draw! no gain or loss\n");
    }
    
    show_bal(*balance);
}    
`

- Pavan S
