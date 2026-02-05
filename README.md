# Problem 5: Rules Shape Behaviour  
*(Document is attached in `Problem5_Trosmic_Sports.pdf` for better understanding)*

## Modelling Kabaddi Rules as an Incentive System

Kabaddi rules can be modelled as an incentive system that maps player actions to rewards and penalties under uncertainty. Rather than simply regulating play, rules determine the expected value of actions, thereby shaping risk-taking and strategy.

### Game State Definition
At any moment in a match, the game state can be defined by:
- Score difference  
- Time remaining  
- Number of players on the mat  
- Raid type (normal vs do-or-die)  

### Player Actions
- **Raiders**: conservative, aggressive, or time-consuming raids  
- **Defenders**: containment, high-risk tackles, or retreat  

Each action has an expected value that depends on:
- Probability of success (estimated from historical data)  
- Immediate payoff (points scored or conceded)  
- Future impact (all-out potential, player count changes, momentum)  

From a statistical perspective, these probabilities can be estimated using raid-level data (e.g., logistic or multinomial regression), allowing behavior to be explained as rational optimization rather than intuition.

---

## How Rules Shape Risk-Taking and Strategy
- Trailing teams face lower opportunity costs for failure → higher-variance strategies (aggressive raids, risky tackles).  
- Leading teams prefer low-variance actions → safe raids, containment defense.  
- Rules such as do-or-die raids and bonus points modify constraints and payoffs, forcing aggression even when success probabilities are low.  

---

## Example: Small Rule Change with Large Effect
**Rule change:** Reduce the all-out bonus from 2 points to 1 point.  

**Effect on incentives:**  
- Expected value of multi-touch raids near an all-out decreases.  
- Single-point, low-risk raids become more attractive.  

**Behavioral consequences:**  
- Raiders attempt fewer high-risk multi-touch raids.  
- Defenders attempt more collective tackles.  

**Match-level impact:**  
- Lower score variance  
- Fewer sudden momentum swings  
- Matches become more incremental and strategy-driven  

---

## Statistical Extensions
This framework can be empirically implemented using:
- Logistic regression → estimate raid success probabilities  
- Markov decision processes → model state transitions  
- Monte Carlo simulations → test hypothetical rule changes before implementation  

Such models allow leagues to quantitatively evaluate how rule design affects competitiveness, risk, and match dynamics.

---

## Summary
Kabaddi rules function as a dynamic incentive system that shapes behavior by altering expected values under uncertainty. Even small rule changes can significantly shift risk-taking, strategy, and match outcomes.  

Modelling these effects statistically enables **evidence-based rule evaluation and design**, demonstrating how data science can directly inform decision-making in professional sports.
