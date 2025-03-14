# Crimson LangGraph Development Tools

A lightweight library for LangGraph that provides useful shortcuts and additional utility functions.

[![PyPI - Version](https://img.shields.io/pypi/v/crimson-langgraph-dev-tool.svg)](https://pypi.org/project/crimson-langgraph-dev-tool/)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/crimson-langgraph-dev-tool.svg)](https://pypi.org/project/crimson-langgraph-dev-tool/)

## Installation

```bash
pip install crimson-langgraph-dev-tool
```

## Overview

This library provides a set of tools and examples to make working with LangGraph easier and more efficient. It includes utility functions for visualization and a collection of examples demonstrating common patterns and use cases.

## Modules

### `crimson.langgraph_dev_tool.display`

This module contains functions for visualizing LangGraph objects:

- `display_graph(graph)`: Renders a compiled state graph as a Mermaid diagram in Jupyter notebooks

Example usage:
```python
from crimson.langgraph_dev_tool.display import display_graph
from langgraph.graph import StateGraph

# Create your graph
builder = StateGraph(State)
# Add nodes and edges
# ...
graph = builder.compile()

# Display the graph
display_graph(graph)
```

## Examples

The repository includes several examples demonstrating the use of LangGraph in different scenarios:

### Conditional Edge Examples

Located in [example/langgraph/conditional_edge.ipynb](./example/langgraph/conditional_edge.ipynb)

This example demonstrates how to use conditional edges in LangGraph to create dynamic branching logic based on state conditions. It covers:

- Basic conditional branching
- Using typed dictionaries for state management
- Creating functions that return a list of destinations
- Using `RunnableLambda` with conditional edges
- Adding listeners for debugging and monitoring

Highlights:
- Using `route_chars` function to conditionally route to multiple nodes
- Demonstrating the differences between using a `Callable` vs a `Runnable` for path selection
- Examples of advanced typehints and their usage in LangGraph

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.