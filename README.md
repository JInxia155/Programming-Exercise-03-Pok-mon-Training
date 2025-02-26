
Download Link : https://programming.engineering/product/rogramming-exercise-03-pokemon-training/



# Programming-Exercise-03-Pok-mon-Training
Programming Exercise 03 – Pokémon Training
Topics: Math, Random, Scanner, enums

Problem Description

This assignment will assess your knowledge of the Math, Random, and Scanner classes, and the creation of an enum type.

You’ve been training your Pokémon for days, and you decide that you want to practice your attacks at a Pokémon Trainer Gym. Your Pokémon has three possible attacks: Scratch, Tackle, and Surf, each of which does a random amount of damage in each interval. On each turn, you can choose only one attack to carry out. The battle will continue until your rival’s Pokémon faints. When you defeat your rival, you will get to walk away with some prize money!

Notes:

    When generating a random number, you must use java.util.Random.

    When generating a floating-point value, round the value to 2 decimal places immediately after generation. You can use the Math.round() method to round the value and remember that you have basic arithmetic operators (*, /) to help you achieve proper rounding. It is highly recommended to write a private static helper method that does this for code reuse.

    When displaying a number, it should be rounded to 2 decimal places.

    To clarify, floating-point numbers should only be rounded during or directly after random number generation and while printing.

    Interval notation is used throughout this document.

        [ , ] means a number such that ≤ ≤ .

        ( , ] means a number such that < ≤ .

        [ , ) means a number such that ≤ < .

        ( , ) means a number such that < < .

    Every command-line prompt must occur on a separate line, with the user input typed on the same line as the prompt. For example, asking for you and your rival Pokémon’s nickname should appear as follows:

Enter your Pokemon’s nickname: Bob

Enter your rival Pokemon’s nickname: Karen

Solution Description

You will need to complete and turn in 2 classes: AttackType.java and PokemonBattle.java.

AttackType.java

This is a public enum that represents the three possible attacks your Pokémon can perform. Populate this enum with the values TACKLE, SCRATCH, and SURF.

.

PokemonBattle.java

    Create a public class named PokemonBattle.

    Create the main method inside the PokemonBattle class. The code for all following steps should be written inside the main method.

    Declare a variable named rand and initialize it to an instance of the Random class.

    Declare and initialize an instance of the Scanner class that will read from the user’s terminal.

    Declare a String for your Pokémon’s nickname. This will be initialized in step 8.

    Declare a String for your rival Pokémon’s nickname. This will also be initialized in step 8.

    Declare a double variable for your rival Pokémon’s health and initialize it to a randomly generated integer in the range [40, 60).

    Prompt for your and your opponent’s Pokémon nicknames: a. Print the following to the console:

Enter your Pokemon’s nickname:

    Read in the input as a String and assign it to the appropriate variable. Note that names may contain spaces in them. Additionally, you should use String’s trim() method to remove any leading and trailing whitespace.

    Print the following to the console:

Enter your rival Pokemon’s nickname:

        Read in the input as a String and assign it to the appropriate variable. Note that names may contain spaces in them. Additionally, you should use String’s trim() method to remove any leading and trailing whitespace.

    Print the following on its own line (without the curly braces):

Your rival has chosen {your rival’s Pokemon’s nickname} to fight, which has {rival’s health} health.

    Create a do-while loop that terminates when your rival’s Pokémon faints (health ≤ 0). Do NOT use break to exit the loop. Steps 10a – 10e should be performed inside this loop:

        Randomly choose the attack. Create a local AttackType variable (i.e., within the loop) named attack and assign a random AttackType to it.

i. You can do so using the following line of code:

AttackType attack = AttackType.values()[rand.nextInt(3)];

    Each move will do a different amount of damage to your opponent.

        If the attack is SCRATCH, you will:

                Generate a random integer in the range of [1, 3]. This is the number of times your Pokémon will scratch during that turn.

                Generate a random double in the range [1.0, 6.0). This is how much damage you will inflict per scratch in that turn.

                Use these values to determine the total damage inflicted during that turn.

            If the attack is SURF, you will inflict random damage as a double in the range

[2.0, 11.0).

        If the attack is TACKLE, you will inflict random damage as a double in the range

[7.0, 9.0).

        Don’t forget to subtract the damage you inflict from your rival’s health.

c. After your turn is complete, print the following on its own line (without the curly braces):

{your Pokemon’s nickname} used {attack} and did {damage} damage. Your rival has {health} health remaining.

Note: When printing your rival’s remaining health, the value displayed should not be less than 0. You can use a ternary expression or the Math.max() method to make this easy!

        Keep a total of the number of turns taken (i.e., the total number of attacks).

        If your opponent fainted, exit the loop. Do NOT use break to accomplish this. Write the boolean expression in the while to appropriately use this information.

    The battle goes on until your rival’s Pokémon faints. After exiting the loop, print the following on its own line (without the curly braces):

{your rival Pokemon’s nickname} fainted after {total turns} turns!

    Store a random double in the range (1200.0, 2400.0] as the prize money from the battle. Hint: Think about how multiplying by −1 affects the inclusivity/exclusivity of the boundaries.

    Use printf to display the following message on its own line (without the curly braces):

You have earned ${prize money}!

Turn-In Procedure

Submission

To submit, upload the files listed below to the corresponding assignment on Gradescope:

    AttackType.java

    PokemonBattle.java

Make sure you see the message stating the assignment was submitted successfully. From this point, Gradescope will run a basic autograder on your submission as discussed in the next section. Any autograder tests are provided as a courtesy to help “sanity check” your work and you may not see all the test cases used to grade your work. You are responsible for thoroughly testing your submission on your own to ensure you have fulfilled the requirements of this assignment. If you have questions about the requirements given, reach out to a TA or Professor via the class forum for clarification.

You can submit as many times as you want before the deadline, so feel free to resubmit as you make substantial progress on the assignment. We will only grade your latest submission. Be sure to submit every file each time you resubmit.
