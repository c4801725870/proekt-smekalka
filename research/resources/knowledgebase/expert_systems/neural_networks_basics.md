# Knowledge Base: Expert Systems — Neural Networks Basics

**Synthesized from:** Барский (Neural Networks)

## Quick Reference

| Concept | Definition | Application |
|---------|------------|-------------|
| Neural network | Parallel computation simulating brain | Recognition, control, decisions |
| Neuron model | Σ(ωᵢxᵢ) - h → f() → output | Weighted sum + threshold |
| Associative thinking | "What does this most resemble?" | Pattern recognition |
| Learning | Forming premise→consequence chains | Weight adjustment |
| Hopfield network | Associative memory, convergence | Optimization |
| Kohonen map (SOM) | Self-organizing clustering | Data mining |

## Two AI Paradigms

| Paradigm | Process | Basis |
|----------|---------|-------|
| Expert | Formalize knowledge → KB → deduction | Expert systems |
| Student | Process observations → DB → inductive learning → deduction | Self-learning systems |

**KB vs DB**: Knowledge base has logical inference capability; database does not.

## Neuron Model

```
y = f(Σ(ωᵢxᵢ) - h)
```
- ωᵢ = synaptic weights (excitatory >0, inhibitory <0)
- h = threshold
- f = activation function (e.g., ReLU analog)
- Processes **credibility** (weights), not raw data

## Two Operating Modes

| Mode | Function |
|------|----------|
| Learning | Present training data → adjust weights → assign output neuron to class |
| Recognition | Present input → find most activated output neuron = classification |

## Network Architectures

| Network | Type | Application |
|---------|------|-------------|
| Feedforward (MLP) | Layered | General classification |
| Hopfield | Recurrent, associative memory | Optimization, pattern completion |
| Hamming | Recurrent | Minimum distance classification |
| Kohonen (SOM) | Self-organizing | Clustering, data mining |

## MLP (Multi-Layer Perceptron)

### Structure
```
Input Layer → Hidden Layer(s) → Output Layer
```

### Training
- Backpropagation: propagate error backward through layers
- Adjust weights to minimize error
- Learning rate controls step size

### Applications
- Classification (handwriting, speech, images)
- Function approximation
- Time series prediction

## Hopfield Network

### Properties
- Fully recurrent
- Associative memory (content-addressable)
- Converges to stable states (energy minimum)
- Can complete partial/noisy patterns

### Applications
- Pattern completion
- Optimization problems
- Error correction

## Kohonen Self-Organizing Map (SOM)

### Properties
- Unsupervised learning
- Maps high-dimensional data to low-dimensional grid
- Preserves topological relationships
- Competitive learning (winner-take-all)

### Applications
- Data clustering
- Data visualization
- Feature extraction
- Data mining

## Applications by Domain

| Domain | Use |
|--------|-----|
| Recognition | Handwritten text, speech, images |
| Control | Self-learning control systems |
| Decisions | Bankruptcy prediction, credit risk, financial monitoring |
| Security | Information protection |
| Forecasting | Social, political, economic |

## Key Principles

1. Brain = spirit's instrument; NN = brain simulation
2. Associative thinking = basis of recognition, control, decisions
3. Brain logic is simple: IF-THEN, premise-consequence
4. Learning = forming invisible relationship tables
5. NN processes credibility, not data
6. Parallelism = key NN property
7. Universal element (neuron) solves different tasks

## Decision Matrix

| Problem | Network | Why |
|---------|---------|-----|
| Classification | MLP / Hamming | Supervised learning |
| Clustering | Kohonen SOM | Unsupervised |
| Optimization | Hopfield | Convergence to stable states |
| Time series | Recurrent NN | Sequential processing |
| Pattern completion | Hopfield | Associative memory |

## Cross-References
- See also: Expert Systems — Building Expert Systems (alternative AI approach)
- See also: Expert Systems — Knowledge-Based Decisions (knowledge representation)
- See also: Decision — Fuzzy Decisions (fuzzy neural networks)
- See also: Decision — Operations Research (optimization with NN)

## Source Books
- Барский А.Б. — Нейронные сети: распознавание, управление, принятие решений (2004)
