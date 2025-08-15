# LangGraph Example Folder

## Overview
This folder contains a Python script demonstrating a simple workflow using **LangGraph**. The script defines a state graph with two nodes that process a message sequentially, visualizes the graph using a Mermaid diagram, and outputs the modified message.

## Contents
- `main.py`: The main script that sets up and executes the LangGraph workflow.

## Description
The `simple.py` script includes:
- A `GraphState` type definition using `TypedDict` to manage a `message` string.
- Two node functions (`node_1` and `node_2`) that append messages to the state.
- A `StateGraph` with a linear flow: `START` → `node_1` → `node_2` → `END`.
- Code to compile the graph, visualize it with a Mermaid diagram (in IPython environments), and invoke it with an initial message ("Hello World").
- Output showing the message transformation through the nodes.

## Requirements
- Python 3.12+
- `langgraph`
- `IPython` (for diagram visualization)
- `typing`

Install dependencies:
```bash
pip install langgraph
```

## Expected Output:
- If running in an IPython environment (e.g., Jupyter), a Mermaid diagram of the graph will be displayed.
- The console will print:
```python 
User mesage: Hello World.
I have reached Node 1.
And now I have reached Node 2.
And I'm exiting the graph
```

## Notes
- The Mermaid diagram requires an IPython-compatible environment. In non-IPython environments, the diagram may not display, but the graph execution will still work.
- This script is a minimal example to illustrate LangGraph's core functionality.