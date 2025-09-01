# AI-Agent2
Absolutely! Here's a more concise version under 250 characters:  An AI agent is a system that senses its environment, processes data, and acts to achieve goals. It uses AI methods like learning and decision-making, enabling applications like chatbots, robots, and virtual assistants.

Browser Use Web UI
GitHub stars Discord Documentation WarmShao

This project builds upon the foundation of the browser-use, which is designed to make websites accessible for AI agents.

We would like to officially thank WarmShao for his contribution to this project.

WebUI: is built on Gradio and supports most of browser-use functionalities. This UI is designed to be user-friendly and enables easy interaction with the browser agent.

Expanded LLM Support: We've integrated support for various Large Language Models (LLMs), including: Google, OpenAI, Azure OpenAI, Anthropic, DeepSeek, Ollama etc. And we plan to add support for even more models in the future.

Custom Browser Support: You can use your own browser with our tool, eliminating the need to re-login to sites or deal with other authentication challenges. This feature also supports high-definition screen recording.

Persistent Browser Sessions: You can choose to keep the browser window open between AI tasks, allowing you to see the complete history and state of AI interactions.


 bu-webui-demo.mp4 
Installation Guide
Option 1: Local Installation
Read the quickstart guide or follow the steps below to get started.

Step 1: Clone the Repository
git clone https://github.com/browser-use/web-ui.git
cd web-ui
Step 2: Set Up Python Environment
We recommend using uv for managing the Python environment.

Using uv (recommended):

uv venv --python 3.11
Activate the virtual environment:

Windows (Command Prompt):
.venv\Scripts\activate
Windows (PowerShell):
.\.venv\Scripts\Activate.ps1
macOS/Linux:
source .venv/bin/activate
Step 3: Install Dependencies
Install Python packages:

uv pip install -r requirements.txt
Install Browsers in playwright.

playwright install --with-deps
Or you can install specific browsers by running:

playwright install chromium --with-deps
Step 4: Configure Environment
Create a copy of the example environment file:
Windows (Command Prompt):
copy .env.example .env
macOS/Linux/Windows (PowerShell):
cp .env.example .env
Open .env in your preferred text editor and add your API keys and other settings
Step 5: Enjoy the web-ui
Run the WebUI:
python webui.py --ip 127.0.0.1 --port 7788
Access the WebUI: Open your web browser and navigate to http://127.0.0.1:7788.
Using Your Own Browser(Optional):
Set BROWSER_PATH to the executable path of your browser and BROWSER_USER_DATA to the user data directory of your browser. Leave BROWSER_USER_DATA empty if you want to use local user data.
Windows
 BROWSER_PATH="C:\Program Files\Google\Chrome\Application\chrome.exe"
 BROWSER_USER_DATA="C:\Users\YourUsername\AppData\Local\Google\Chrome\User Data"
Note: Replace YourUsername with your actual Windows username for Windows systems.

Mac
 BROWSER_PATH="/Applications/Google Chrome.app/Contents/MacOS/Google Chrome"
 BROWSER_USER_DATA="/Users/YourUsername/Library/Application Support/Google/Chrome"
Close all Chrome windows
Open the WebUI in a non-Chrome browser, such as Firefox or Edge. This is important because the persistent browser context will use the Chrome data when running the agent.
Check the "Use Own Browser" option within the Browser Settings.
Option 2: Docker Installation
Prerequisites
Docker and Docker Compose installed
Docker Desktop (For Windows/macOS)
Docker Engine and Docker Compose (For Linux)
Step 1: Clone the Repository
git clone https://github.com/browser-use/web-ui.git
cd web-ui
Step 2: Configure Environment
Create a copy of the example environment file:
Windows (Command Prompt):
copy .env.example .env
macOS/Linux/Windows (PowerShell):
cp .env.example .env
Open .env in your preferred text editor and add your API keys and other settings
Step 3: Docker Build and Run
docker compose up --build
For ARM64 systems (e.g., Apple Silicon Macs), please run follow command:

TARGETPLATFORM=linux/arm64 docker compose up --build
Step 4: Enjoy the web-ui and vnc
Web-UI: Open http://localhost:7788 in your browser
VNC Viewer (for watching browser interactions): Open http://localhost:6080/vnc.html
Default VNC password: "youvncpassword"
Can be changed by setting VNC_PASSWORD in your .env file
Changelog
 2025/01/26: Thanks to @vvincent1234. Now browser-use-webui can combine with DeepSeek-r1 to engage in deep thinking!
 2025/01/10: Thanks to @casistack. Now we have Docker Setup option and also Support keep browser open between tasks.Video tutorial demo.
 2025/01/06: Thanks to @richard-devbot. A New and Well-Designed WebUI is released. Video tutorial demo.
