🐍 Snake Q-Learning (Pygame + NumPy)

This project is my attempt to learn Q-learning by building a simple Snake game using Pygame for visualization and NumPy for the Q-table.

The snake learns how to move around a 5x5 grid, collect food, and avoid collisions by updating its Q-values based on rewards.

📖 What I Learned

How Q-learning works:

Representing states and actions in a Q-table.

Updating Q-values using the Bellman equation.

Using exploration vs. exploitation (epsilon-greedy strategy).

Designing reward functions:

+10 for eating food

-1 for each step (to encourage faster solutions)

-100 for collisions

Integrating reinforcement learning into a game loop with Pygame.

Visualizing the snake and food while training.

⚙️ How It Works

Environment:

5x5 grid world.

Snake moves UP, DOWN, LEFT, or RIGHT.

Food appears randomly.

Q-table:

Shape: (GRID_SIZE, GRID_SIZE, 4) → (x, y, action).

Stores expected rewards for each state-action pair.

Training:

For each episode, the snake starts fresh.

Chooses actions with epsilon-greedy.

Updates Q-table using:

Q(s, a) ← Q(s, a) + α [ r + γ max(Q(s’, a’)) – Q(s, a) ]
