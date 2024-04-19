# Knights

This code is designed to solve a series of logic puzzles where characters can only be knights (who always tell the truth) or knaves (who always lie). The knowledge for each puzzle represents the statements made by the characters, and the main function uses logical inference to determine which characters are knights and which are knaves.

## logic.py

Sentence: This is the base class for all logical sentences. It provides the basic structure and methods that all logical sentences should have. These methods include evaluate, formula, symbols, validate, and parenthesize.

Symbol: This class represents a logical symbol. It inherits from the Sentence class and overrides its methods to provide functionality specific to logical symbols.

Not: This class represents the logical NOT operation. It takes a Sentence as an operand and negates its truth value.

And: This class represents the logical AND operation. It takes one or more Sentence objects as conjuncts and evaluates to True if all the conjuncts are True.

Or: This class represents the logical OR operation. It takes one or more Sentence objects as disjuncts and evaluates to True if at least one of the disjuncts is True.

Implication: This class represents a logical implication. It takes two Sentence objects as the antecedent and the consequent. It evaluates to True if the antecedent is False or both the antecedent and the consequent are True.

Biconditional: This class represents a logical biconditional (if and only if). It takes two Sentence objects and evaluates to True if both Sentence objects have the same truth value.

model_check: This is a function that checks if a given knowledge base entails a query. It uses a recursive algorithm to check all possible models of the symbols in the knowledge base and the query.

## puzzle.py

The symbol class is used to represent the statements "A is a Knight", "A is a Knave", "B is a Knight", "B is a Knave", "C is a Knight", and "C is a Knave".

knowledge0, knowledge1, knowledge2, knowledge3: These are logical expressions that represent the knowledge gained from the statements made by A, B, and C in each puzzle. They use logical operations like And, Or, Not, and Biconditional to combine the Symbol objects into a logical sentence that represents the puzzle's conditions.

The main function is the entry point of the program. It defines a list of symbols and a list of puzzles, then loops over the puzzles. For each puzzle, it prints the puzzle's name and checks if the knowledge for that puzzle has been implemented. If it has, it uses the model_check function to check which symbols are true under the puzzle's knowledge and prints them.

## Run locally

Clone the repository and execute the logic.py file. You will see the results in the console.

