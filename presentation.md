% Assignment 2
% Methods: Numerical Simulation
% March 16, 2016



Stackelberg game: introduction
================

What is it about?
----------

*Adapted from Game Theory 1: Problem set 2*

Three oligopolists $i$ = 1,2,3 operate in a market with inverse demand given by $P(Q) = a - Q$, where $Q = q_1 +q_2 +q_3 < a$. Firms $i$ = 1,2,3 have constant per-unit costs of, respectively, $c_1$, $c_2$ and $c_3$. 

Sequence of moves
----------

To determine the subgame-perfect Nash equilibrium, we first consider the sequence of moves, which is as follows: 

* At time $t = 1$: Firm 1 chooses quantity $q_1 \geq 0$.
* At time $t = 2$: After observing $q_1$, firms 2 and 3 simultaneously and independently choose $q_2 \geq 0$ and $q_3 \geq 0$, respectively.

Backward induction
----------
This is a sequential game with one proper subgame that starts in $t = 2$. The subgame-perfect Nash equilibrium (SPNE) consists of a single quantity for firm 1 and functions $q_2$ = $q_2(q_1)$ and $q_3$ = $q_3(q_1)$ for firms 2 and 3 prescribing subgame perfect Nash equilibrium choices for firms 2 and 3 for every quantity choice by firm 1. We solve the game by backward induction. 


How to find the SPNE?
================

Step 1: $t = 2$ (1)
----------
Start in $t = 2$: Maximizing firm 3 profits gives:

$$q_3(q_1,q_2)= \frac{a - c_3 - q_1 - q_2}{2},$$

where $q_2$ is assumed to be given. For firm 2 analogously:

$$q_2(q_1,q_3)= \frac{a - c_2 - q_1 - q_3}{2}.$$

Step 1: $t = 2$ (2)
----------
Inserting both into each other yields the Nash equilibrium of the subgame between firms 2 and 3:

$$q_2 = \frac{1}{3}(a - 2c_2 + c_3 - q_1)\ and\ q_3 = \frac{1}{3}(a - 2c_3 + c_2 - q_1)\tag{1}$$

Step 2: $t = 1$
----------
Moving to $t$ = 1: Inserting the expressions in (1) into the objective function of firm 1 gives $\pi(q_1) = (a - c_1 - q_1 - q_2 - q_3)q_1 = (a - c_1 - q_1 - \frac{1}{3}(a - 2c_2$ <br /> $+\ c_3 - q_1) - \frac{1}{3}(a - 2c_3 + c_2 - q_1))q_1 = \frac{1}{3}(a - 3c_1 + c_2 + c_3 - q_1)q_1.$ The FOC for firm 1 is $a - 3c_1 + c_2 + c_3 - 2q_1 = 0$, which gives

$$q_1^* = \frac{1}{2}(a - 3c_1 + c_2 + c_3)\tag{2}$$

SPNE and SPNE path
----------
The expression in (1) and (2) together constitute the SPNE of the game. On the SPNE path: $q_2^* = \frac{1}{6}(a + 3c_1 - 5c_2 + c_3)$, $q_3^* = \frac{1}{6}(a + 3c_1 + c_2 - 5c_3)$ and so $Q_a^* = q_1^* + q_2^* + q_3^* = \frac{1}{6}(5a - 3c_1 - c_2 - c_3)$.

Thanks to
----------
![Heinrich von Stackelberg](images/Heinrich_von_stackelberg.gif "Heinrich von Stackelberg")

