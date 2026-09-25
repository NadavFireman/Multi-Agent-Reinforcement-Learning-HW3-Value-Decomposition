# Multi-Agent Reinforcement Learning HW3 - Value Decomposition

**Home Assignment (Grade 97, M.Sc. Data Science, HIT). Value decomposition for common-reward tasks with the MARL textbook codebase: Independent DQN (IDQN), Value Decomposition Networks (VDN) and QMIX compared on cooperative Level-Based Foraging and on two SMAClite combat scenarios.**

## Headline Results
- **Foraging, five seeds:** VDN finishes first (0.97) with IDQN close behind (0.93), while QMIX without tuning collapses to 0.47 with a wide spread between seeds — complexity alone gives no advantage.
- **SMAClite 2s3z:** returns look tied (96.5–98.5), but win rates break the tie — VDN 95.0% and QMIX 93.3% against IDQN's 87.7%, with decomposition also more stable across seeds.
- **SMAClite 2s_vs_1sc:** the picture flips in time — VDN wins no battle until 2.3M steps while IDQN wins far earlier, and all three converge to 61–64% win rate. The choice of metric decides the conclusion.

## Key Features
- **Value Decomposition with the Book Codebase:** IDQN, VDN and QMIX compared on the course's prepared training data — five seeds on Foraging, three on each SMAClite scenario.
- **Own IDQN Run:** a shorter IDQN run with the cooperative reward, as a sanity check of the training setup.
- **Training Diagnostics:** returns, win rates, loss and ε-schedules analysed, including QMIX's loss starting orders of magnitude above the others.
- **Rollout Videos:** early and late training rollouts for Foraging and both SMAClite scenarios, showing the learned behaviour — from team wipes to wins, and from moving as a pair to splitting roles.

## Repository Structure
- `Multi_Agent_Reinforcement_Learning_HW3.ipynb`: Full solution notebook — training, comparisons, diagnostics and embedded rollout videos (explanations in Hebrew).
- `hw3_lbf_idqn_own.csv`: Metrics of the own IDQN run on Level-Based Foraging.
- `hw3_lbf_8x8-2p-3f_coop.csv`: Metrics of IDQN, VDN and QMIX on Foraging-8x8-2p-3f, five seeds each.
- `hw3_smaclite_2s3z.csv`: Metrics of the three algorithms on SMAClite 2s3z, three seeds each.
- `hw3_smaclite_2s_vs_1sc.csv`: Metrics of the three algorithms on SMAClite 2s_vs_1sc, three seeds each.
- `HW3_lbf_2p3f_vdn_early_200k.mp4`: VDN on Foraging after 200K steps.
- `HW3_lbf_2p3f_vdn_late_3800k.mp4`: VDN on Foraging after 3.8M steps.
- `HW3_smaclite_2s3z_vdn_early_100k.mp4`: VDN on SMAClite 2s3z after 100K steps.
- `HW3_smaclite_2s3z_vdn_late_1900k.mp4`: VDN on SMAClite 2s3z after 1.9M steps.
- `HW3_smaclite_2s_vs_1sc_vdn_early_200k.mp4`: VDN on SMAClite 2s_vs_1sc after 200K steps.
- `HW3_smaclite_2s_vs_1sc_vdn_late_3800k.mp4`: VDN on SMAClite 2s_vs_1sc after 3.8M steps.
- `Assignment_3.pdf`: Original assignment instructions.

## Source
The assignment is the Thursday exercise, *Value Decomposition Algorithms*, from [marl-book-exercises](https://github.com/marl-book/marl-book-exercises) — designed for the Barcelona Summer School 2024 on Multi-Agent Reinforcement Learning and based on the textbook *Multi-Agent Reinforcement Learning: Foundations and Modern Approaches*. Training uses the book's codebase.
