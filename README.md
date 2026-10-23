# Agent Learning Notebooks: smolagents and LangGraph

Two learning notebooks exploring different approaches to agent execution: generating and running Python code with smolagents, and explicitly orchestrating a stateful tool-calling workflow with LangGraph.

## Start here

| Notebook | Focus |
| --- | --- |
| [Static one-shot agent](Static_OneShot_Agent.ipynb) | Code-generating agent / Generates and executes Python with smolagents. |
| [Agent with graph orchestration](src/nb/Agent_with_LangChain_Grpah.ipynb) | State, memory, nodes, and routing in an agent workflow. |

Read the cells and any saved outputs on GitHub to explore the examples.

## Scope and status

These are learning examples rather than a production agent or a controlled evaluation study. The repository name and creation date do not establish when each notebook was developed; individual file history provides that context.

A reproducible dependency environment and complete current execution instructions are not supplied. Execution has not been revalidated for this documentation refresh. Check notebook imports, configuration, credentials, and any model-call costs before running cells.

## Tech stack

| Component | Technology | Role |
| --- | --- | --- |
| Notebook interface | Jupyter | Interactive code and saved outputs |
| Code agent | Hugging Face smolagents | `CodeAgent` generates and executes Python for a calculation task |
| Model adapter | LiteLLM | Connects the smolagents notebook to NVIDIA-hosted inference |
| Tools and messages | LangChain | Defines arithmetic tools, binds them to the model, and handles messages |
| Workflow orchestration | LangGraph | Defines state, model/tool nodes, conditional routing, and the execution loop |
| Model integration | `ChatNVIDIA` | Connects the graph workflow to NVIDIA-hosted inference |
| Model provider | NVIDIA NIM | Serves the models used by both notebooks |

### Models used

- **smolagents notebook:** `meta/llama-3.3-70b-instruct`
- **LangGraph notebook:** `nvidia/nemotron-3-super-120b-a12b`

These are separate examples, not a controlled comparison between frameworks or models.

## Related project

For a concrete business workflow with tests and live evaluation, see [Retail Agent and Evaluation](https://github.com/manimalakumar/Hermes-Agent-n-Eval).
