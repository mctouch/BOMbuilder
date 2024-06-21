# BOMbuilder

The purpose of this application is to generate a Bill of Materials and a high level networking and interconnect topology diagram and optionally output build configuration sets.

This app uses a supermicro product list to scrape all relevant documentation for configuration options. This is trained against both an LLM (options openai or local) for human interaction and then trained against a recommender engine for configuration recommendation using one shot transformers.

Phase 1 provides a textural prompt quenstion and response only using Riva text processing, Phase 2 will include full conversational interaction leveraging nvidia Riva. This document only contains Phase 1 instructions and guidelines

*Note: See INSTALL.md for installation instructions.*


## Design Overview

Product data is stored in a cuDF dataframe https://github.com/rapidsai/cudf for performance over cpu based pandas.

Prompting is managed by NeMo Guardrails langchain 

https://github.com/NVIDIA/NeMo-Guardrails/blob/develop/docs/user_guides/langchain/langchain-integration.md

https://developer.nvidia.com/blog/building-safer-llm-apps-with-langchain-templates-and-nvidia-nemo-guardrails/



