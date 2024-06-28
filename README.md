# Council of AIs

This repository contains a Python script that demonstrates how to use the `autogen` library to create a simulated council of AI advisors. Each advisor specializes in a different domain and collaborates to evaluate and create an execution plan for a given proposal.

## Overview

### Purpose

The script's primary goal is to simulate a decision-making process involving multiple AI advisors. The head advisor consults various domain-specific advisors to gather insights and formulate a comprehensive plan.

### Components

1. **ConversableAgent**: Represents an AI advisor in a specific domain (e.g., legal, health, economic, etc.).
    - Each advisor is given a distinct role and system message that defines their domain of expertise and their task in evaluating the proposal.

2. **GroupChat**: Facilitates communication among the advisors.
    - Advisors interact in a round-robin fashion to ensure a balanced contribution from each advisor.

3. **GroupChatManager**: Manages the group chat session.
    - Orchestrates the flow of messages and ensures the proper execution of chat rounds.

4. **Head Advisor**: The main AI agent responsible for initiating the chat and synthesizing the input from other advisors.
    - The head advisor's task is to decide whether to accept, reject, or modify the proposal based on the collective input and to create a detailed execution plan.

### Process

1. **Proposal Initialization**: 
    - A proposal is defined, in this case, making it mandatory for schools to provide food to students.

2. **Advisor Configuration**:
    - Each advisor is configured with a specific role and system message, defining their input scope and consultation task.

3. **Group Chat Setup**:
    - A `GroupChat` object is created with all advisors.
    - The group chat is managed by a `GroupChatManager` that handles the communication rounds.

4. **Execution**:
    - The head advisor initiates the group chat, consulting all advisors to gather their insights.
    - After the defined number of turns, the head advisor summarizes the collective input into a comprehensive execution plan.

### Example Use Case

- The script can be used in scenarios where a multi-faceted analysis is required for decision-making, such as policy evaluation, strategic planning, or complex problem-solving.

## Running the Script

1. **Install Dependencies**:
    ```bash
    pip install autogen
    ```

2. **Configure API Key**:
    - Update the `llm_config` dictionary with your actual API key.

3. **Execute the Script**:
    - Run the script to see the council of AIs in action.

## Conclusion

This script provides a framework for leveraging multiple AI advisors to collaboratively evaluate proposals and create detailed execution plans. It demonstrates the power of combining domain-specific AI expertise to tackle complex decision-making tasks.
