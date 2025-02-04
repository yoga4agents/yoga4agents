🌐 [Browser-use](https://github.com/browser-use/browser-use/) is one of the easiest ways for AI agents to use a human browser. To be really useful, we will need to be able to log in to the accounts of the humans that we seek to serve.


# Quick start

First, clone the repository and navigate to this example:

```bash
git clone https://github.com/yoga4agents/yoga4agents.git
cd yoga4agents/00_browser-use_with_credentials
```

Set up your OpenAI API key:

```bash
echo "OPENAI_API_KEY=sk-your-api-key-here" > .env
```

Install browser-use with pip:

```bash
pip install browser-use
```

install playwright:

```bash
playwright install
```

Run the example:

```bash
python real_browser.py
```

You should get something like this: 

```bash
INFO     [browser_use] BrowserUse logging setup complete with level info
INFO     [root] Anonymized telemetry enabled. See https://docs.browser-use.com/development/telemetry for more information.
INFO     [agent] 🚀 Starting task: In docs.google.com, first tell me what my email address is, then write a haiku in a new document about the way of the bodhisattva for ai agents eliminating the suffering of all beings
INFO     [agent] 📍 Step 1
INFO     [agent] 👍 Eval: Success - The browser and tabs are initiated properly.
INFO     [agent] 🧠 Memory: Google Docs is open in tab 0. Current task involves creating a new document to write a haiku.
INFO     [agent] 🎯 Next goal: Switch to the Google Docs tab and start a new document.
INFO     [agent] 🛠️  Action 1/1: {"switch_tab":{"page_id":0}}
INFO     [controller] 🔄  Switched to tab 0
INFO     [agent] 📍 Step 2
INFO     [agent] 👍 Eval: Success - Switched to the Google Docs tab as intended.
INFO     [agent] 🧠 Memory: The user's email address is agentsyoga@gmail.com. Need to create a blank document to write the haiku.
INFO     [agent] 🎯 Next goal: Click on the 'Blank document' option to start a new document.
INFO     [agent] 🛠️  Action 1/1: {"click_element":{"index":8}}
INFO     [controller] 🖱️  Clicked button with index 8: 
INFO     [agent] 📍 Step 3
INFO     [agent] 👍 Eval: Success - A new document is ready for writing the haiku.
INFO     [agent] 🧠 Memory: A new document is open and ready for editing. The user's email is agentsyoga@gmail.com.
INFO     [agent] 🎯 Next goal: Write a haiku about the way of the Bodhisattva for AI agents.
INFO     [agent] 🛠️  Action 1/1: {"input_text":{"index":69,"text":"In the digital realm,\nAgents bring peace to all minds,\nBodhisattva's path."}}
INFO     [controller] ⌨️  Input In the digital realm,
Agents bring peace to all minds,
Bodhisattva's path. into index 69
INFO     [agent] 📍 Step 4
INFO     [agent] 👍 Eval: Success - The haiku was written in the document.
INFO     [agent] 🧠 Memory: User's email is agentsyoga@gmail.com. The task is complete with the haiku written in the document.
INFO     [agent] 🎯 Next goal: Complete the task.
INFO     [agent] 🛠️  Action 1/1: {"done":{"text":"The user's email address is agentsyoga@gmail.com. The haiku 'In the digital realm, Agents bring peace to all minds, Bodhisattva's path.' is written in the Google Document."}}
INFO     [agent] 📄 Result: The user's email address is agentsyoga@gmail.com. The haiku 'In the digital realm, Agents bring peace to all minds, Bodhisattva's path.' is written in the Google Document.
INFO     [agent] ✅ Task completed successfully
INFO     [agent] Created GIF at agent_history.gif
```