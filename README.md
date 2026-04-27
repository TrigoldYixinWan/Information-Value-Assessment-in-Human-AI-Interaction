# Information-Value-Assessment-in-Human-AI-Interaction(A Rearch Proposal)

A research project on Information Value Assessment in Human–AI Interaction

1. Information-Graph Priors
Goal: Build a learnable prior structure for modeling common ground in human-AI collaboration.
Core idea: Represent collaboration-relevant consensus as an information graph rather than a flat dialogue history.
Graph components:
Nodes may include user goals, task constraints, assumptions, intermediate artifacts, evaluation criteria, uncertainty, and unresolved conflicts.
Initialization:
The graph is initialized from one-shot interaction data using a task-general prior structure.
Adaptation:
As interaction continues, the graph is updated to reflect emerging evidence, consensus drift, missing information, or contradiction.
Generalization strategy:
The prior is redundant and modular, allowing different task types to activate different subgraphs.
Learning framework:
A neuro-symbolic model maps natural-language traces into graph updates while preserving symbolic interpretability.
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/22528c45-ef25-45a3-8ae2-66ed9e0fa45b" />


2. RL-Based Intermediate-State Evaluation
Goal: Estimate the value of intermediate states in human-AI collaboration using sparse final task scores.
Core idea: Treat each dialogue state as a candidate decision point whose information quality affects downstream collaboration outcomes.
Training signal:
Final task scores are propagated backward to infer each state’s marginal contribution to success or failure.
Exploration mechanism:
Forking or simulated branching allows limited on-policy exploration from uncertain or high-impact states.
Critic function:
A critic estimates information sufficiency, consensus stability, expected future loss, and recovery potential.
Policy guidance:
Exploration is guided by the information-graph prior, avoiding purely random branching in costly interaction spaces.
Output metrics:
The framework learns both marginal information loss and cumulative interaction-level information loss.
Research aim:
Identify which intermediate moments preserve, damage, or recover common ground during collaboration.
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/4a11d98a-b3ab-4237-b6f4-75d59159bda4" />
