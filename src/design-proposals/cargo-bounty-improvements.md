# Cargo Bounty Improvements

| Designers | Implemented | GitHub Links |
|---|---|---|
| [TheMikina](https://github.com/TheMikina), Discord @mikina5638 | :x: No | TBD |

## Overview

The document proposes a rework for cargo bounties, to force more cross-department cooperation and also include a way how to provide feedback to Command about departmental performance. The feedback is provided through quotas and hidden time-limits on bounties, with Command getting regularly yelled at by CC if such quotas are not being met, to nudge players towards more conflict.

## Background

Currently, when department is underperforming or not fulfilling their responsibilities, the impact on the station is is mostly localized and rarely reaches higher command. While it can lead to minor conflict between individual players, it's rare when Command gets involved to properly scold players.

However, rounds where Command actually cares about departmental performance, performs regular check-ins, and underperformance leads to (RP) consequences and scolding are one of the more interesting rounds, because it leads to conflict, blame shifting, and the dissatisfaction can spreads through the station.

The purpose of this proposition is to nudge players towards such behavior, by implementing measurable performance indicators and more importantly quotas that should be met, which increases pressure on departments to cooperate and fulfill their obligations. More importantly, it provides and opportunity to give Command clear warnings (for example by sternly worded CC faxes) throughout the round that the current stations performance is not satisfactory, which should nudge Command into interacting with the crew to demand explanation and better performance.

Additionally, this proposition attempts to address the current state of Cargo Bounties, which in many cases can be fulfilled by Cargo itself or outright cheated - for example the surgical tools bounty can usually be done by cargo ordering a box of surgical tools and then immediately using them to fulfill the bounty for a huge profit. Most of the bounties are currently not really balanced, and do not require cross-department cooperation.

Since Cargo Bounties are the perfect opportunity how relatively easily fulfill the first stated goal of the design - providing quotas that are measurable and cross-departmental, it is necessary to address the current state of the bounties.

## Features to be added

The proposal can be split into three parts - Cargo bounty balance, Cargo bounty quotas and CC feedback when quotas are not being met in time.

The parts are kind of independent on each other, and because they require a pretty hefty amount of balancing, the Cargo bounty balance should be implemented first, so values for the quotas can be set up based on actual experience from real gameplay after the bounty balancing is done.

#### Priority bounties

A time limit on some bounty completion should be implemented, to further increase pressure on the crew. To not feel punishing, the time limit should work similarly to priority mail. A small number of bounties should be marked as "Priority bounties", and a time limit (visible in the Bounty computer) with a "priority reward" should be introduced. When the time limit runs out, the value of the bounty is reduced by the (considerable) bonus amount.

The timer will not start until the bounty is Accepted (and thus generated), but the bounty is marked as priority bounty even before accepting.

The number of failed priority bounties should be tracked and accessible from the Station Performance computer (see CC Feedback chapter below).

Priority bounties should be printed on a paper with an added bright yellow strip, and the round time when the bounty expires should be included on the printed bounty form when read.

### Cargo bounty quotas

To increase pressure on the crew, a quota of required profit made during the round should be implemented.

The quota is a simple sum of all bounties that has been successfully delivered during the shift.

The quota should be visible in the Cargo bounty computer, and a final result should be mentioned in the Game End screen. However, it should not be a win condition in itself, since the main purpose is to provide a way how to measure departmental performance during the round, and provide reason for more conflicts in RP.

#### Calculating the quota

The most difficult change that will require extensive balancing. The value should depend on expected round duration, player count, game mode and station size. While the quota has to be static, to better balance things during a round a dynamic pricing for Bounties when they are generated should be introduced, through a calculated bounty price multiplier. This allows slight room for on-the-fly balancing based on current round conditions (such as player count).

The quota should be based on experience and average results from gameplay rounds after the Cargo bounty balance has been implemented.

Give a description of what game mechanics you would like to add or change. This should be a general overview, with enough details on critical design points that someone can directly implement the feature from this design document. Exact numbers for game balance however are not necessary, as these can be adjusted later either during development or after it has been implemented, but mention *what* will have to be balanced and what needs to be considered when doing so.

## Game Design Rationale

Consider addressing:

- How does the feature align with our [Core Design Principles](../design/design-principles.md) and game philosphy?

## Roundflow & Player interaction

Consider addressing:

- At what point in the round does the feature come into play? Does it happen every round? How does it affect the round pace?
- How do you wish for players to interact with your feature and how should they not interact with it? How is this mechanically enforced?

## Administrative & Server Rule Impact (if applicable)

- Does this feature introduce any new rule enforcement challenges or additional workload for admins?
- Could this feature increase the likelihood of griefing, rule-breaking, or player disputes?
- How are the rules enforced mechanically by way the feature will be implemented?

# Technical Considerations

- Are there any anticipated performance impacts?
- Does the feature require new systems, UI elements, or refactors of existing ones?
- For required UI elements, give a short description or a mockup of how they should look like (for example a radial menu, actions & alerts, navmaps, or other window types)
