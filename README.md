# lyzr-experimental-automata
The version 0.2 is a prompt based agent workflow that integrates with other Lyzr agents

# Lyzr Automata - Parallel-Processing Agent Automation Framework

Lyzr Automata is a sophisticated parallel-processing agent automation framework designed to enhance workflow efficiency and effectiveness. It enables a seamless transition between states, leverages recursive checks for continual improvement, and ensures the achievement of end goals in line with assigned objectives.

## How to Install

Get started with Lyzr Automata by installing the experimental package using pip:

pip install lyzr-experimental-automata

## Configuring Agents

Begin by configuring your agents and assigning them unique personas:

```python
agent1 = Agent(persona="enter the persona of agent1")
agent2 = Agent(persona="enter the persona of agent2")
agent3 = Agent(persona="enter the persona of agent3")

Example Configuration:

agent1 = Agent(persona="Marketing Consultant")
agent2 = Agent(persona="Tweet Generator")
agent3 = Agent(persona="Linkedin Post Creator")

Creating Tasks
Create tasks by providing specific instructions and desired outcomes. Assign these tasks to your agents:

task1 = Task("enter the instructions", "enter the desired outcome", agent1, display_output='no')

Task1 is the initial task in the workflow. You can control the visibility of its output by setting display_output to either 'yes' or 'no'.

Example Task 1:

task1 = Task("Do research and pull out interesting marketing tips for SaaS companies. The research articles should not be more than 500 words.", "Ensure that you bring the best content from the likes of HBS, YCombinator", agent1, display_output='no')

Setting Up Dependencies
Leverage the multi-thread, parallel-processing capabilities of Lyzr Automata by specifying task dependencies:

task2 = Task("enter the instructions", "enter the desired outcome", agent1, display_output='yes', dependencies=[task1])

Example Task 2:

task2 = Task("Use the research material provided and write 5 engaging tweets. Display only the tweets. No explanation or additional comments required.", "Ensure that the tweets are as engaging as if it was written by the best influencer in the world", agent2, display_output='yes', dependencies=[task1])

Continue adding tasks as required, defining their dependencies to optimize parallel processing.

Further Tasks
Add additional tasks (like Task 3) and define their dependencies for continued workflow.

task3 = Task("enter the instructions", "enter the desired outcome", agent1, display_output='yes', dependencies=[task1])

Example Task 3:

task3 = Task("Use the research material provided and write 1 short form LinkedIn post. Display only the LinkedIn post. No explanation or additional comments required.", "Ensure that the post is as if it was written by the best influencer in the world", agent3, display_output='yes', dependencies=[task1])

Lyzr Automata is your go-to solution for creating an efficient, automated workflow powered by the capabilities of OpenAI.

