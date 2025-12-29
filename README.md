# RL Learning Tool

A **web-based interactive platform** for learning and experimenting with **Reinforcement Learning (RL)** algorithms. This tool provides an intuitive interface for exploring key RL algorithms, environments, and real-time training visualization.

---

## Features

### 1. Environments
The platform supports a variety of RL environments:

- **GridWorld**: 2D grid navigation with start, goal, walls, and holes.
- **CartPole**: Classic cart-pole balancing problem (discretized states).
- **MountainCar**: Classic control problem with position and velocity discretization.
- **FrozenLake**: Grid with holes and slippery movements.
- **Breakout**: Tiny discrete breakout game with bricks, paddle, and ball.
- **Gym4ReaL**: Custom grid training sim with energy levels and goal-oriented movement.

Each environment provides:
- `reset()` to initialize the state
- `step(action)` to advance one timestep
- State and action space queries
- Transition models for planning algorithms

---

### 2. Algorithms
Implemented RL algorithms include:

- **Policy Iteration**
- **Value Iteration**
- **Monte Carlo (MC)**
- **Temporal Difference (TD)**
- **n-step TD**
- **SARSA**
- **Q-Learning**

Each algorithm supports:
- Parameter adjustments (learning rate, discount factor, epsilon, etc.)
- Training loops for multiple episodes
- Real-time tracking of value functions, Q-tables, and policies

---

### 3. Parameter Adjustment
Users can modify key parameters through the frontend UI, including:

- Learning rate (`alpha`)
- Discount factor (`gamma`)
- Exploration rate (`epsilon`)
- Maximum steps per episode
- Environment-specific parameters (grid size, slip probability, max energy, etc.)

---

### 4. Visualization
The platform provides **real-time visualizations**:

- Grid/world maps with agent position
- CartPole/MountainCar state visualization
- Breakout game paddle, ball, and brick layout
- Gym4ReaL energy and progress HUD
- Value functions and Q-tables heatmaps
- Training progress graphs

---

### 5. My Project Structure
rl-learning-tool/
├── backend/
│ ├── app/
│ │ ├── environments/ # RL environment classes
│ │ ├── algorithms/ # RL algorithms
│ │ ├── trainer.py # Training loop logic
│ │ ├── main.py # FastAPI entrypoint
│ │ └── utils.py # Helper functions
│ └── requirements.txt
├── frontend/
│ ├── index.html
│ ├── styles.css
│ └── script.js
├── README.md
└── .gitignore


---

### 6. Getting the thing  Started

#### 6.1 Install Dependencies
```bash
cd backend
python -m venv venv
source venv/bin/activate # Linux/macOS
venv\Scripts\activate    # Windows
pip install -r requirements.txt

###6.2 Run Backend
uvicorn app.main:app --reload

6.3 Open Frontend

Open frontend/index.html in your browser to access the interactive UI.

7. Notes

The project is built using FastAPI for the backend and HTML/CSS/JS for the frontend.

All environments provide tabular RL interfaces, compatible with value iteration, policy iteration, and Q-learning.

Visualization is updated in real time to provide intuitive understanding of agent behavior and learning dynamics.








