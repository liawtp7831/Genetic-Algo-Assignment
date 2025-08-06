# Genetic Algorithm for Traveling Salesman Problem (TSP)

A high-performance **Genetic Algorithm** implementation for solving the **Traveling Salesman Problem** optimized for large-scale instances (400+ cities). Features comprehensive parameter optimization and performance benchmarking.

## 🎯 Overview

This project tackles the classic NP-hard Traveling Salesman Problem using evolutionary computation techniques. The implementation supports various selection methods, mutation strategies, and population configurations to find near-optimal solutions for complex routing problems.

## ✨ Key Features

- **Flexible Population Management**: Random route initialization with configurable population sizes
- **Multiple Selection Methods**: Tournament, Proportional, and Random selection strategies
- **Adaptive Parameters**:
  - Elite preservation size
  - Mutation probability rates
  - Population size scaling
  - Iteration limits
- **Comprehensive Analytics**:
  - Generation-by-generation distance tracking
  - Performance metrics and execution timing
  - Improvement percentage calculations
  - Visual plotting capabilities

## 🧬 Algorithm Parameters

### Tested Configurations

| Parameter | Values Tested |
|-----------|---------------|
| **Iterations** | 500, 2,500, 5,000 |
| **Elite Size** | 2, 3, 7, 10 |
| **Mutation Probability** | 0.001, 0.02, 0.05, 0.1, 0.5 |
| **Population Size** | 100, 400, 800 |

### Performance Metrics

The algorithm evaluates performance using:

```
improvement = initial_best_distance - final_best_distance
improvement_percentage = (improvement / initial_best_distance) × 100
```

## 📊 Benchmark Results

### Selection Method Comparison

| Method | Time (s) | Final Distance | Improvement |
|--------|----------|----------------|-------------|
| **Tournament Selection** | 5.61 | 15,405.03 | **26.5%** |
| Proportional Selection | 3.68 | 17,801.33 | 15.0% |
| Random Selection | 3.40 | 17,869.63 | 14.7% |

### Iteration Count Analysis

| Configuration | Time (s) | Final Distance | Improvement |
|---------------|----------|----------------|-------------|
| **Tournament (2,500 iter)** | 156.08 | **10,982.41** | **47.6%** |
| Tournament (5,000 iter) | 314.55 | 11,015.48 | 47.4% |
| Tournament (500 iter) | 30.97 | 11,871.41 | 43.3% |
| Tournament (baseline) | 5.61 | 15,405.03 | 26.5% |

### Elite Size Optimization

| Elite Size | Time (s) | Final Distance | Improvement |
|------------|----------|----------------|-------------|
| **2** | 8.39 | **14,799.99** | **29.4%** |
| 3 | 7.11 | 14,846.69 | 29.1% |
| 10 | 4.70 | 15,291.03 | 27.0% |
| 5 (baseline) | 5.61 | 15,405.03 | 26.5% |
| 7 | 4.99 | 15,882.46 | 24.2% |

### Mutation Rate Impact

| Mutation Rate | Time (s) | Final Distance | Improvement |
|---------------|----------|----------------|-------------|
| **0.02** | 6.62 | **14,441.54** | **31.1%** |
| 0.05 | 7.08 | 14,950.70 | 28.6% |
| 0.1 | 5.92 | 15,313.00 | 26.9% |
| 0.01 (baseline) | 5.61 | 15,405.03 | 26.5% |
| 0.5 | 7.70 | 15,422.83 | 26.4% |
| 0.001 | 5.42 | 15,625.60 | 25.4% |

### Population Size Effects

| Population Size | Time (s) | Final Distance | Improvement |
|-----------------|----------|----------------|-------------|
| **400** | 164.30 | **13,201.74** | **33.5%** |
| 100 | 164.30 | 13,201.74 | 33.5% |
| 800 | 337.68 | 14,052.57 | 30.1% |
| 200 (baseline) | 5.61 | 15,405.03 | 26.5% |

## 🏆 Optimal Configuration

Based on comprehensive benchmarking, the **recommended parameter set** is:

- **Selection Method**: Tournament Selection
- **Elite Size**: 2
- **Mutation Rate**: 0.02
- **Population Size**: 400
- **Iterations**: 2,500

**Expected Performance**: 
- Final Distance: ~10,982
- Improvement: ~47.6%
- Execution Time: ~156 seconds

## ⚖️ Performance vs Speed Trade-offs

### Best Performance (Time-Agnostic)
1. **Optimal Settings**: 10,325.41 distance (4,029s)
2. **2,500 Iterations**: 10,982.41 distance (156s) ⭐ *Recommended*
3. **5,000 Iterations**: 11,015.48 distance (315s)

### Fastest Execution (Performance-Agnostic)
1. **Random Selection**: 3.4s (17,869 distance)
2. **Proportional Selection**: 3.7s (17,801 distance)
3. **Tournament (Elite=10)**: 4.7s (15,291 distance) ⭐ *Quick & Good*

## 📈 Analysis Insights

- **Tournament selection** consistently outperforms other methods
- **Sweet spot** at 2,500 iterations balances quality and computation time
- **Small elite sizes** (2-3) prevent premature convergence
- **Moderate mutation rates** (0.02) provide optimal exploration
- **Larger populations** improve solution quality but increase runtime

## 📊 Visualization

The implementation includes built-in plotting capabilities for:
- Convergence analysis (best/average distance per generation)
- Route visualization
- Parameter sensitivity analysis
- Performance comparison charts

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues, feature requests, or pull requests.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
