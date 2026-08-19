+++
title = 'Probability Theory I: Counting & Combinatorics'
date = 2026-08-19
draft = false
description = "Lecture notes on the fundamentals of probability, counting, permutations, and combinations"
tags = ["Probability", "Combinatorics", "Statistics"]
group = "Probability"
weight = 1
math = true
toc = true
meta = true
+++

# Fundamentals of Probability and Combinatorics in Counting Events



This lecture explores the basic principles of probability focused on counting and combinatorics, illustrating how to calculate the likelihood of certain events by enumerating all possible outcomes. Through examples involving coin flips, poker hands, and license plates, the professor introduces key concepts such as order significance, replacement rules, factorial notation, and combinations. These foundational tools enable efficient computation of probabilities without exhaustive listing.

* Gentle Introduction to Probability: Counting Coin Flips and Dice
* Steve Brunton
This are notes from : https://www.youtube.com/watch?v=4T3aOIfNdTY&list=PLMrJAkhIeNNR3sNYvfgiKgcStwuPSts9V&index=2


## 1. Basic Probability: Event Counting and Outcome Enumeration

Probability measures how likely an event $A$ is to occur, by dividing the number of favorable outcomes by the total possible outcomes. Direct enumeration quickly becomes infeasible as the number of outcomes grows exponentially, demanding combinatorial approaches to counting efficiently.

$$
P(A) = \dfrac{\text{Number of ways } A \text{ can happen}}{\text{Total number of possible outcomes}}
$$

- Direct listing works for simple problems but becomes impractical for large sample spaces (e.g., poker hands).
- Probability calculation is closely tied to combinatorics, specifically counting combinations and permutations.
- A critical first step: count the total number of possible outcomes, then count outcomes in event $A$.

## 2. Coin Flips: Counting Sequences with Order and Replacement

An example with 10 coin flips illustrates counting sequences where order matters and each trial is independent (with replacement).

- Each coin flip has 2 outcomes: Heads (H) or Tails (T).
- The total number of possible sequences in 10 flips is $2^{10} = 1024$.
- **Order matters.** For example, sequence HT is different from TH.
- This is an example of **sampling with replacement**, because the outcome of one flip does not affect the others.

General formula for sampling with replacement where order matters:

$$
n^r
$$

where

- $n$ = number of possible outcomes per trial (here 2)
- $r$ = number of independent trials (here 10)

## 3. Poker Hands: Counting Ordered 5-Card Runs Without Replacement

Next, the lecture tackles dealing 5 cards from a standard 52-card deck as an example of sampling without replacement.

- Each card drawn reduces the deck size by 1 for the next draw.
- Number of ordered 5-card sequences (order matters): $52 \times 51 \times 50 \times 49 \times 48$.

Shortcut using factorial notation:

$$
\dfrac{52!}{(52-5)!} = \dfrac{52!}{47!}
$$

Factorial ($n!$): the product of all positive integers from $n$ down to 1, for example:

$$
5! = 5 \times 4 \times 3 \times 2 \times 1 = 120
$$

- $52!$ is the product of all integers from 52 down to 1.
- Without replacement means once an item is chosen, it is not returned, shrinking the pool.
- Dealing cards is a standard example of sampling without replacement where order matters.

General formula for sampling without replacement where order matters (permutations):

$$
P(n,r) = \dfrac{n!}{(n-r)!}
$$

- $n$: total number of items to choose from
- $r$: number of items chosen

## 4. Order Does Not Matter: Combinations (Poker Hands Without Sequence)

Poker hands typically do not consider the order of the cards (e.g., {King, Queen, 3, 5, 7} is identical to {Queen, King, 3, 5, 7}).

Counting hands where order does not matter differs from counting ordered sequences. Since there are $r!$ ways to order $r$ items, divide by $r!$ to avoid counting permutations as distinct.

The number of unique hands (combinations) is

$$
\binom{n}{r} = \dfrac{n!}{r!\\,(n-r)!}
$$

This is called "n choose r" and represents the number of ways to choose $r$ elements from $n$ without considering order.

**Key insight:** Permutations count order, combinations do not.

<div class="rules-table">

| Concept | Formula | Order Matters? | Replacement? | Description |
|---|---|---|---|---|
| Sampling with replacement | $n^r$ | Yes | Yes | Independent trials, order matters |
| Sampling without replacement (permutations) | $\dfrac{n!}{(n-r)!}$ | Yes | No | Order matters, pool shrinks |
| Sampling without replacement (combinations) | $\binom{n}{r} = \dfrac{n!}{r!\\,(n-r)!}$ | No | No | Order does not matter |

</div>

## 5. Key Definitions and Distinctions

- **Order matters:** Different sequences count separately (e.g., HT vs TH).
- **Order does not matter:** Only combinations of elements count (e.g., poker hand cards).
- **With replacement:** Chosen item can be selected again, trials independent.
- **Without replacement:** Items removed after selection; pool decreases.
- **Factorial** ($n!$): $n \times (n-1) \times \cdots \times 2 \times 1$.
- **Permutation:** Ordered arrangements without repetition.
- **Combination:** Selections where order is irrelevant.

## 6. Application Example: Counting License Plates

A practical illustration applying these principles is counting possible license plates:

- Format: 4 letters followed by 2 digits.
- Letter options: 26 (A–Z), digit options: 10 (0–9).
- Order matters (ABCDE ≠ ACBDE).
- Are repetitions allowed? Assumed yes ("with replacement"), so letters or digits can repeat.

Total number of license plates under these assumptions:

$$
26^4 \times 10^2
$$

- Variations where repetition is disallowed ("without replacement") lead to different counts.
- Questions for exploration include the probability that all letters are distinct.

## 7. Summary of Counting Approaches and Their Use in Probability

Counting combinations and permutations is fundamental for evaluating probabilities in card games, coin flips, lotteries, license plates, and many other contexts.

- Start by enumerating total possible outcomes using appropriate combinatorial formulas.
- Count favorable outcomes via counting methods.
- Calculate probability as favorable ÷ total.
- Factorials and the $n$ choose $r$ notation are essential tools.
- As sample sizes grow (e.g., 1000 coin flips), direct enumeration is impossible; combinatorial formulas enable computation.
- Mastery builds intuition and speed in calculating odds across diverse scenarios like games and lotteries.

## 8. Important Takeaways

- Probability in discrete cases is about clever counting rather than brute-force enumeration.
- Always determine if order matters and if sampling is with or without replacement.
- Factorials simplify counting sequences and arrangements.

Key formula to remember:

$$
\text{Number of combinations} = \binom{n}{r} = \dfrac{n!}{r!\\,(n-r)!}
$$

These concepts provide the foundation to understand more complex probability distributions and real-world probabilistic modeling. This framework paves the way to more advanced probability topics by establishing the fundamental combinatorial logic behind counting event outcomes efficiently and accurately.
