# Conditional Probability and Distributions



## Introduction
In many real-world situations, the probability of an event depends on whether another event has occurred. This relationship is captured by **conditional probability**. Conditional probability measures the likelihood of an event occurring given that another event has already happened.

## Definition of Conditional Probability
The conditional probability of event $A$ given that event $B$ has occurred is denoted as $P(A|B)$ and is defined as:

$$P(A|B) = \frac{P(A \cap B)}{P(B)}$$

<img width="746" height="465" alt="image" src="https://github.com/user-attachments/assets/d5ec7885-e288-4e78-a99b-e15a55da9713" />


---

# Example 1: Drawing a Ball

A box contains 6 white balls and 4 red balls. We randomly (and without replacement) draw two balls from the box. What is the probability that the second ball selected is red, given that the first ball selected is white?

## Solution
Let $A$ be an event drawing a red ball; and $B$ be an event drawing a white ball. The probability of first drawing a white ball is given by:

$$P(B) = \frac{6}{10} = 0.6$$

Now, we have 9 balls left in the box, and if the first drawn ball was white, we have 5 white and 4 red balls in the box. Hence,

$$P(A|B) = \frac{4}{9} \approx 0.44$$

---

# Example 2: Deck of Cards

What is the probability that two cards drawn from a 36-card deck belong to the same suit?

## Solution
Let $A$ be an event of drawing a card of a given suit and event $B$ - an event of drawing a card of the same suit. Hence,

* $P(A) = 0.25$
* $P(B|A) = 8/35 \approx 0.23$ since among the 35 cards left only 8 cards have the same suit as the first card drawn.

---

# Multiplication Rule

The probability that two events $A$ and $B$ both occur is given by:

$$P(A \cap B) = P(A|B) \times P(B)$$

or by

$$P(A \cap B) = P(B|A) \times P(A)$$

---

# Example: Drawer of Socks

A drawer contains 6 black socks and 4 white socks. Two socks are drawn randomly, one after the other without replacement.

* a) What is the probability that the first sock is black and the second sock is also black?
* b) Use the multiplication rule to calculate the joint probability of both events.

## Solution
Let event $A$ be drawing a black sock and event $B$ - drawing a black sock the second time in a row. Then

* $P(A) = 6/10 = 0.6$
* $P(B|A) = 5/9 \approx 0.56$

And the joint probability, which is drawing black socks two times in a row, is given by

$$P(A \cap B) = P(A) \cdot P(B|A) \approx 0.6 \cdot 0.56 \approx 0.33$$

---

# Practice

Now it is time for you to practice calculating conditional and joint probabilities.

## Exercise 1
A bag contains 5 red, 3 blue, and 2 green marbles. If a marble is drawn and is known to be **not red**, what is the probability that it is **blue**?

### Solution
We have 3 blue and 2 green marbles, so a total of 5 not red marbles. Then the probability of drawing a blue marble given that it is known not to be red, is:

$$P(A|B) = \frac{3}{5} = 0.6$$

---

## Exercise 2
A company has 60 employees, 20 of whom are in management. If a randomly selected employee is in a meeting and 15 managers are currently in meetings while 25 non-managers are also in meeting, what is the probability that the employee is a **manager**?

### Solution
The probability of selecting an employee, who is a manager, under the condition they are at the meeting, is

$$P(A|B) = \frac{15}{15+25} = 0.375$$

---

## Exercise 3
A factory produces 100 lightbulbs, of which 10 are defective. Two lightbulbs are selected randomly, one after the other without replacement.

* a) What is the probability that the first lightbulb selected is defective and the second lightbulb is not defective?
* b) Use the multiplication rule to calculate the joint probability of these two events.

### Solution
We have 10 defective and 90 non defective bulbs before the experiment. The probability of the first lightbulb to be defective is

$$P(A) = \frac{10}{100} = 0.1$$

We have 99 bulbs left, 90 of which are not defective. The probability of the second lightbulb not to be defective is

$$P(B|A) = \frac{90}{99} \approx 0.91$$

And the joint probability, which stands for selecting a defective lightbulb and a non-defective one right after it is

$$P(A \cap B) = P(A) \cdot P(B|A) \approx 0.1 \cdot 0.91 = 0.091$$
