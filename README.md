#🧬 Genetic Algorithm for Solving the Traveling Salesman Problem (TSP)

This project implements a **Genetic Algorithm (GA)** to solve the **Traveling Salesman Problem (TSP)** for a large number of cities (e.g., 400). It includes parameter optimization and performance benchmarking to find the best route with the shortest possible distance.

## 📘 Description

Solves the Traveling Salesman Problem (TSP) using a Genetic Algorithm with support for elite selection, mutation tuning, and population size variation. Includes performance benchmarking and visual analysis for 400+ cities.

## 📌 Features

- Population initialization with random routes
- Support for multiple parent selection methods (Tournament, Proportional, etc.)
- Customizable:
  - eliteSize
  - mutationProbability
  - popSize
  - iteration_limit
- Records and plots:
  - Best distance per generation
  - Average distance per generation
  - Execution time
  - Final improvement percentage
- Benchmark summary with visual and tabular comparison of parameter settings

## 🧪 Parameters Tested

- **Iteration Counts**: 500, 2500, 5000
- **Elite Sizes**: 2, 3, 7, 10
- **Mutation Probabilities**: 0.001, 0.02, 0.05, 0.1, 0.5
- **Population Sizes**: 100, 400, 800

## 📊 Evaluation Metrics

The improvement is calculated using:
improvement = initial_best - final_best
improvement_percentage = (improvement / initial_best) * 100

====================================================================================================
COMPREHENSIVE BENCHMARK SUMMARY
====================================================================================================

SELECTION METHODS                                 
--------------------------------------------------
Method                         Time (s)   Final Dist   Improvement 
Random Selection               3.396      17869.63     14.7        %
Tournament Selection           5.612      15405.03     26.5        %
Proportional Selection         3.679      17801.33     15.0        %

ITERATION TESTING                                 
--------------------------------------------------
Method                         Time (s)   Final Dist   Improvement 
Tournament Selection           5.612      15405.03     26.5        %
Tournament (Iter=500)          30.968     11871.41     43.3        %
Tournament (Iter=2500)         156.083    10982.41     47.6        %
Tournament (Iter=5000)         314.549    11015.48     47.4        %

ELITE SIZE TESTING                                
--------------------------------------------------
Method                         Time (s)   Final Dist   Improvement 
Tournament (Elite=2)           8.389      14799.99     29.4        %
Tournament (Elite=3)           7.111      14846.69     29.1        %
Tournament Selection           5.612      15405.03     26.5        %
Tournament (Elite=7)           4.989      15882.46     24.2        %
Tournament (Elite=10)          4.704      15291.03     27.0        %
MUTATION RATE TESTING                             
--------------------------------------------------
Method                         Time (s)   Final Dist   Improvement 
Tournament (Mutation=0.001)    5.416      15625.60     25.4        %
Tournament Selection           5.612      15405.03     26.5        %
Tournament (Mutation=0.02)     6.618      14441.54     31.1        %
Tournament (Mutation=0.05)     7.075      14950.70     28.6        %
Tournament (Mutation=0.1)      5.921      15313.00     26.9        %
Tournament (Mutation=0.5)      7.698      15422.83     26.4        %

POPULATION SIZE TESTING                           
--------------------------------------------------
Method                         Time (s)   Final Dist   Improvement 
Tournament Selection           5.612      15405.03     26.5        %
Tournament (PopSize=100)       164.297    13201.74     33.5        %
Tournament (PopSize=400)       164.297    13201.74     33.5        %
Tournament (PopSize=800)       337.676    14052.57     30.1        %
====================================================================================================

🏆 OVERALL WINNERS:
Best Final Distance: Tournament (Best Settings) (10325.41)
Fastest Execution: Random Selection (3.396s)
Best Improvement: Tournament (Best Settings) (48.6%)

📊 PARAMETER RECOMMENDATIONS:
Best Elite Size: Tournament (Elite=2)
Best Mutation Rate: Tournament (Mutation=0.02)
Best Population Size: Tournament (PopSize=400)
Best Iteration Count: Tournament (Iter=2500)

🔍 DETAILED PARAMETER ANALYSIS:
------------------------------------------------------------
Elite Size Ranking (Best to Worst):
  1. Tournament (Elite=2): 14799.99
  2. Tournament (Elite=3): 14846.69
  3. Tournament (Elite=10): 15291.03
  4. Tournament Selection: 15405.03
  5. Tournament (Elite=7): 15882.46

Mutation Rate Ranking (Best to Worst):
  1. Tournament (Mutation=0.02): 14441.54
  2. Tournament (Mutation=0.05): 14950.70
  3. Tournament (Mutation=0.1): 15313.00
  4. Tournament Selection: 15405.03
  5. Tournament (Mutation=0.5): 15422.83
  6. Tournament (Mutation=0.001): 15625.60

Population Size Ranking (Best to Worst):
  1. Tournament (PopSize=400): 13201.74
  2. Tournament (PopSize=100): 13201.74
  3. Tournament (PopSize=800): 14052.57
  4. Tournament Selection: 15405.03

⚖️ TIME vs PERFORMANCE TRADE-OFF:
------------------------------------------------------------
Best Performance (regardless of time):
  1. Tournament (Best Settings): 10325.41 (Time: 4029.489s)
  2. Tournament (Iter=2500): 10982.41 (Time: 156.083s)
  3. Tournament (Iter=5000): 11015.48 (Time: 314.549s)
  4. Tournament (Iter=500): 11871.41 (Time: 30.968s)
  5. Tournament (PopSize=400): 13201.74 (Time: 164.297s)

Fastest Execution (regardless of performance):
  1. Random Selection: 3.396s (Distance: 17869.63)
  2. Proportional Selection: 3.679s (Distance: 17801.33)
  3. Tournament (Elite=10): 4.704s (Distance: 15291.03)
  4. Tournament (Elite=7): 4.989s (Distance: 15882.46)
  5. Tournament (Mutation=0.001): 5.416s (Distance: 15625.60)
