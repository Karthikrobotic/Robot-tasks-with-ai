# Robotic Task Sequencing: Intelligent Task Planning via Scene Understanding

## Overview

One of the key challenges in robotics is enabling robots to understand and execute user instructions in dynamic real-world environments. This project is a proof of concept addressing the problem: **How can a robot plan tasks in sequence based on what is actually available in its environment?**

For example, if you ask the robot "Put the fruits in a bowl," the robot needs to:

- Identify which fruits are available in your home
- Locate those fruits and the bowl in the environment
- Plan the optimal sequence of actions to accomplish the task

This repository demonstrates a solution where a robot reasons over a simulated 3D scene, interprets user instructions, and generates actionable plans.

---

## Features

- **3D Environment Simulation**
  - A simple 3D workspace with a robot end effector and test objects: `apple`, `banana`, `bowl`, `water bottle`.
- **User Command Interface**
  - HTML frontend where the user specifies the robot task.
- **AI Scene Reasoning**
  - The system exports a description of the environment (objects, their positions, orientations) and sends it along with the user's instruction to an LLM (e.g., GPT).
- **Plan Generation**
  - The backend AI creates a JSON step-by-step plan for the robot end effector, specifying what actions to take and the coordinates for each action.
- **Extensible Pipeline**
  - Modular structure allows replacing simulation data with real robot data in the future.

---

## Directory Structure


---

## Technologies

- **3D Visualization**: [Add engine, e.g., Three.js or Unity]
- **Frontend**: HTML, JavaScript
- **Backend**: Python (Flask/FastAPI), OpenAI GPT
- **Planned**: Integration with ROS2, Gazebo, MoveIt for real robot pipelines

---

## Key Innovations

- **Bridges language understanding and scene perception** for dynamic robotic planning.
- **Modular architecture** enables future integration with simulation and real robots.
- **Foundational agentic AI structure**: plan to develop sub-agents dedicated to planning, object identification, and manipulation.

---

## Usage

1. Clone this repository:
    ```
    git clone https://github.com/your_username/robotic-task-sequencing.git
    cd robotic-task-sequencing
    ```
2. Start the backend server:
    ```
    cd backend
    python app.py
    ```
3. Open the frontend:
    - Open `frontend/index.html` in your browser.
    - Enter your command (e.g., "Put the apple in the bowl"), click **Connect**.
    - The AI will display the sequence of planned steps in the 3D environment.

4. To test with your own objects or scenes, update the `3d_workspace/` and object definitions.

---

## Future Directions

- **Integration with real-world robot simulators**: Import object and environment data from URDF files, Gazebo, or MoveIt.
- **Agentic AI modules**: Develop specialized agents for different robotic sub-tasks.
- **Full robotic control pipeline**: User command → scene perception → AI planning → IK/trajectory generation → real-world actuation.
- **Generalizable task planning**: Expand to arbitrary objects and more complex household scenarios.

---

## Why This Project?

- Advances intelligent robot autonomy
- Demonstrates practical integration of LLMs with physical reasoning
- Offers a scalable foundation for next-generation home robots

---

## Contact

*If you are looking for innovative, cross-disciplinary robotics talent—let’s talk!*

[Your Name]  
[Your Email/LinkedIn/GitHub]

---

*Feel free to submit pull requests or issues if you want to collaborate or contribute!*
