+++
title = 'Probability exercises'
date = 2026-08-19
draft = false
description = "Exercises to build intuition about probability and statistics"
tags = ["Probability", "Factorials", "Statistics"]
group = "Probability"
weight = 2
math = true
toc = true
meta = true
+++

# Counting & Probability — 20 Exercises

Work through these in order. Before computing anything, always ask the two diagnostic questions:

1. **Does order matter?**
2. **Is sampling with or without replacement?**

<div class="rules-table">

| Order? | Replacement? | Formula |
|---|---|---|
| Yes | Yes | $n^r$ |
| Yes | No | $P(n,r) = \dfrac{n!}{(n-r)!}$ |
| No | No | $\binom{n}{r} = \dfrac{n!}{r!\\,(n-r)!}$ |

</div>

Solutions with reasoning start on page 2 (below the divider). Try each problem fully before scrolling.

---

## Part A — Identifying the right tool (1–5)

**1.** A fair six-sided die is rolled 4 times and the results are written down in order. How many different sequences are possible?

**2.** A fair coin is flipped 10 times. How many of the 1024 sequences contain exactly 3 heads? What is the probability of getting exactly 3 heads?

**3.** A password is 8 characters long, drawn from the 26 lowercase letters plus the 10 digits.
(a) How many passwords are possible if characters may repeat?
(b) How many if no character may repeat?

**4.** In how many distinct orders can 5 different books be arranged on a shelf?

**5.** A club of 12 people must select a committee of 3. How many different committees are possible? How would the answer change if the three roles were President, Treasurer, and Secretary?

---

## Part B — Replacement and its absence (6–10)

**6.** Three cards are drawn from a standard 52-card deck, and the order of drawing is recorded.
(a) How many ordered outcomes are there if each card is returned and the deck reshuffled between draws?
(b) How many if the cards are not returned?

**7.** Three cards are dealt from a 52-card deck without replacement. What is the probability that all three are hearts? (Order is irrelevant here — count hands.)

**8.** In a lottery you choose 6 distinct numbers from 1 to 49; the draw is unordered.
(a) How many possible tickets are there?
(b) What is the probability that a single ticket matches all 6 numbers?
(c) What is the probability of matching exactly 5 of the 6?

**9.** License plates have the format 4 letters followed by 2 digits, with repetition allowed.
(a) How many plates are possible?
(b) How many have four *distinct* letters?
(c) What is the probability that a randomly chosen plate has four distinct letters?

**10.** Five people are in a room. Assuming birthdays are independent and uniformly distributed over 365 days, what is the probability that no two share a birthday? Set up the expression and identify which counting rule appears in the numerator and which in the denominator.

---

## Part C — Poker hands (11–14)

All hands are 5 cards dealt without replacement from a standard 52-card deck; order does not matter.

**11.** How many distinct 5-card hands exist? Then verify that $\dfrac{52!/47!}{5!}$ gives the same number, and explain *why* dividing by $5!$ is the correct correction.

**12.** What is the probability of being dealt a flush (all five cards of the same suit, straight flushes included)?

**13.** What is the probability of being dealt **exactly one pair** — two cards of one rank and three other cards of three different ranks, none matching each other or the pair?

**14.** What is the probability of a full house (three cards of one rank, two of another)?

---

## Part D — Mixed and conceptual (15–20)

**15.** Without computing either number, argue why $\binom{52}{5} = \binom{52}{47}$. State the general identity and give a one-sentence combinatorial reason.

**16.** A fair coin is flipped 10 times. What is the probability of getting **at least 8 heads**?

**17.** A bag contains 5 red, 4 blue, and 3 green marbles. Four marbles are drawn without replacement. What is the probability that exactly 2 are red?

**18.** Eight people are seated in a row of 8 chairs at random. What is the probability that two specific people, Ana and Bruno, end up seated next to each other?

**19.** *(Stretch — extends the lecture slightly.)* How many distinct arrangements are there of the letters in the word **BANANA**? Explain why the answer is not $6!$, and connect your correction to the same logic used in problem 11.

**20.** A committee of 5 is chosen at random from 6 men and 7 women. What is the probability that the committee contains at least 3 women?

---
---

# Solutions

**1.** Order matters, with replacement: $6^4 = 1296$.

**2.** Order matters, with replacement — but two different counts are needed, and each formula uses $n$ and $r$ differently:
- **Total sequences:** sampling with replacement, $n^r$, with $n = 2$ (heads or tails per flip) and $r = 10$ (flips): $2^{10} = 1024$.
- **Favorable sequences:** a sequence is fixed once you decide *which* 3 of the 10 positions hold heads — order within that choice is already accounted for by the positions themselves. This is a combination, $\binom{n}{r}$, with $n = 10$ (positions to choose from) and $r = 3$ (positions chosen to be heads): $\binom{10}{3} = 120$.

$P = 120/1024 = 15/128 \approx 0.117$.

**3.** Order matters (a password is a sequence), $n = 36$.
(a) With replacement: $36^8 = 2{,}821{,}109{,}907{,}456$.
(b) Without replacement: $\dfrac{36!}{28!} = 36 \cdot 35 \cdot 34 \cdot 33 \cdot 32 \cdot 31 \cdot 30 \cdot 29 = 1{,}220{,}096{,}908{,}800$.
Note how much smaller (b) is — forbidding repeats costs you a factor of about 2300.

**4.** Order matters, without replacement (each book is placed once): $5! = 120$. This is $P(5,5) = 5!/0! = 120$ (recall $0! = 1$).

**5.** Plain committee — order does not matter, without replacement: $\binom{12}{3} = \dfrac{12 \cdot 11 \cdot 10}{3 \cdot 2 \cdot 1} = 220$. With named roles, order matters (still without replacement): $P(12,3) = 12 \cdot 11 \cdot 10 = 1320 = 220 \cdot 3!$. Same selections, each counted $3!$ times.

**6.** Order matters (the order of drawing is recorded).
(a) With replacement: $52^3 = 140{,}608$.
(b) Without replacement: $52 \cdot 51 \cdot 50 = 132{,}600 = \dfrac{52!}{49!}$.

**7.** Order does not matter, without replacement: $P = \dfrac{\binom{13}{3}}{\binom{52}{3}} = \dfrac{286}{22{,}100} = \dfrac{11}{850} \approx 0.0129$.
Equivalently, as sequential draws (order matters here, but it cancels out): $\frac{13}{52} \cdot \frac{12}{51} \cdot \frac{11}{50}$ — same value. Both are valid as long as you're consistent about order in numerator and denominator.

**8.** Order does not matter, without replacement.
(a) $\binom{49}{6} = 13{,}983{,}816$.
(b) $1/13{,}983{,}816 \approx 7.15 \times 10^{-8}$.
(c) Choose which 5 of your 6 numbers hit, then one of the 43 losing numbers for the sixth: $\dfrac{\binom{6}{5}\binom{43}{1}}{\binom{49}{6}} = \dfrac{258}{13{,}983{,}816} \approx 1.85 \times 10^{-5}$.

**9.** Order matters (a plate is a sequence).
(a) With replacement (letters and digits both repeatable): $26^4 \cdot 10^2 = 456{,}976 \cdot 100 = 45{,}697{,}600$.
(b) Letters without replacement, digits still with replacement: $(26 \cdot 25 \cdot 24 \cdot 23) \cdot 10^2 = 358{,}800 \cdot 100 = 35{,}880{,}000$.
(c) The digits cancel: $\dfrac{358{,}800}{456{,}976} \approx 0.785$.

**10.** Order matters throughout: $P = \dfrac{365 \cdot 364 \cdot 363 \cdot 362 \cdot 361}{365^5} = \dfrac{365!/360!}{365^5} \approx 0.9729$.
Numerator: sampling **without** replacement (each birthday, once assigned, can't be reused). Denominator: sampling **with** replacement (birthdays are independent, so any day can repeat). This is the whole birthday problem in miniature — grow it to 23 people and the probability of a collision passes 50%.

**11.** Order does not matter, without replacement: $\binom{52}{5} = 2{,}598{,}960$. The ordered count is $52!/47! = 311{,}875{,}200$; every unordered hand appears among those ordered sequences exactly $5! = 120$ times, once for each way to permute its 5 cards. Dividing by $5!$ collapses each of those groups to a single hand. $311{,}875{,}200 / 120 = 2{,}598{,}960$. ✓

**12.** Order does not matter, without replacement. Pick a suit (4 ways), then 5 of its 13 cards: $4 \cdot \binom{13}{5} = 4 \cdot 1287 = 5148$.
$P = 5148/2{,}598{,}960 \approx 0.00198$, roughly 1 in 505.

**13.** Order does not matter, without replacement. Build the hand in stages:
- Rank of the pair: 13
- Which 2 of that rank's 4 suits: $\binom{4}{2} = 6$
- Ranks of the 3 kickers, all distinct and different from the pair: $\binom{12}{3} = 220$
- Suit of each kicker: $4^3 = 64$

$13 \cdot 6 \cdot 220 \cdot 64 = 1{,}098{,}240$, so $P = 1{,}098{,}240/2{,}598{,}960 \approx 0.4226$.
Note that the kicker *ranks* use a combination (unordered, no replacement) while the suits use the with-replacement rule — a single problem can mix all three tools.

**14.** Order does not matter, without replacement: $13 \cdot \binom{4}{3} \cdot 12 \cdot \binom{4}{2} = 13 \cdot 4 \cdot 12 \cdot 6 = 3744$. $P = 3744/2{,}598{,}960 \approx 0.00144$.
Watch the trap: $13 \cdot 12$, not $\binom{13}{2}$, because the triple-rank and the pair-rank play different roles — kings-full-of-twos is a different hand from twos-full-of-kings.

**15.** Order does not matter (both sides are combinations): $\binom{n}{r} = \binom{n}{n-r}$. Every choice of 5 cards to *keep* is simultaneously a choice of 47 cards to *leave behind*; the two selections determine each other, so the counts are equal. Algebraically the formula is symmetric in $r$ and $n-r$: $\frac{n!}{r!(n-r)!}$ is unchanged when you swap them.

**16.** Order matters, with replacement for the 1024 total sequences — but "at least 8 heads" is again counted with combinations (order doesn't matter among the chosen positions), the same trick as problem 2. "At least 8" means 8, 9, or 10 heads — disjoint cases, so add:
$\binom{10}{8} + \binom{10}{9} + \binom{10}{10} = 45 + 10 + 1 = 56$.
$P = 56/1024 = 7/128 \approx 0.0547$.

**17.** Order does not matter, without replacement. Total: $\binom{12}{4} = 495$. Favorable: choose 2 of the 5 reds and 2 of the 7 non-reds: $\binom{5}{2}\binom{7}{2} = 10 \cdot 21 = 210$.
$P = 210/495 = 14/33 \approx 0.424$.
The blue/green split is a red herring — once you only care about "red vs not red," collapse the other categories.

**18.** Order matters, without replacement (people are seated, no repeats). Glue Ana and Bruno into a single block: 7 objects to arrange in $7!$ ways, times 2 for their internal order → $2 \cdot 7! = 10{,}080$ favorable arrangements out of $8! = 40{,}320$.
$P = 2 \cdot 7!/8! = 2/8 = 1/4$.
Sanity check without any factorials: given where Ana sits, Bruno has 7 equally likely remaining chairs, and either 1 or 2 of them are adjacent depending on whether Ana is on an end — averaging gives $\frac{2 \cdot 1 + 6 \cdot 2}{8 \cdot 7} = 14/56 = 1/4$. ✓

**19.** Order matters (an arrangement is a sequence), without replacement — with a correction for repeated letters: $\dfrac{6!}{3!\\,2!\\,1!} = \dfrac{720}{12} = 60$.
$6!$ would be right if the letters were all distinguishable ($B, A_1, N_1, A_2, N_2, A_3$). They aren't: the three A's can be permuted $3!$ ways and the two N's $2!$ ways without changing the visible word, so each real arrangement was counted $3! \cdot 2! = 12$ times. Dividing by the overcount is exactly the move from problem 11 — there we divided by $5!$ because the order *within* a hand was irrelevant; here we divide because the order *among identical letters* is invisible.

**20.** Order does not matter, without replacement: total committees $\binom{13}{5} = 1287$. "At least 3 women" splits into disjoint cases:
- 3 women, 2 men: $\binom{7}{3}\binom{6}{2} = 35 \cdot 15 = 525$
- 4 women, 1 man: $\binom{7}{4}\binom{6}{1} = 35 \cdot 6 = 210$
- 5 women, 0 men: $\binom{7}{5}\binom{6}{0} = 21 \cdot 1 = 21$

Total favorable: $525 + 210 + 21 = 756$, so $P = 756/1287 = 84/143 \approx 0.587$.

---

## If you want more practice

Good self-generated variations on the same problems:

- Redo #9 assuming digits also cannot repeat, and assuming the *whole plate* must have distinct characters.
- Compute the probability of two pair and of three of a kind, then check that all your poker probabilities sum sensibly with "high card" as the remainder.
- Redo #17 asking for "at least 2 red," and check it against $1 - P(0 \text{ red}) - P(1 \text{ red})$.
- Extend #16 to 20 flips and at least 15 heads — the point where enumeration is hopeless but the formula is unchanged.
