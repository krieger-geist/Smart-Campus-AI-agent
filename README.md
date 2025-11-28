SmartCampusAI Agent is a hackathon-built smart campus assistant that connects a web UI and Telegram bot to an n8n workflow to answer student and visitor queries about the college in real time.
Below is a ready-to-use README.md you can paste into your GitHub repo and then customize with your name, partner name, screenshots, and exact tech stack details.

SmartCampusAI Agent

SmartCampusAI Agent is an AI-powered campus assistant that helps students, parents, and visitors get instant answers about your college, such as fees, courses, admissions, events, and more.
It uses an n8n workflow connected to a custom web interface and a Telegram bot so users can chat with the assistant from browsers or mobile devices, using both text and voice.

Features

•	Answer common campus queries (fees, admissions, courses, events, contact info, etc.).
•	Unified experience across web UI and Telegram bot, powered by the same n8n workflow.
•	Voice input support in the browser using Web Speech APIs, with text responses shown in a chat-style interface.
•	Easy to extend with new intents, FAQs, or integrations inside n8n without changing frontend code.
•	Suitable for hackathons, college helpdesks, and as a base for more advanced smart campus solutions.
Architecture

•	Frontend: A web-based chat UI (HTML/CSS/JavaScript) that sends user messages to n8n via an HTTP/Webhook endpoint.
•	Automation layer: n8n workflow that receives messages, calls an LLM or rule-based logic, and returns structured responses.
•	Messaging: Telegram bot connected to the same n8n workflow so students can chat directly from Telegram.
•	Optional: Voice recognition in the browser and voice responses in Telegram using n8n’s audio/AI integrations.
Tech Stack

•	n8n for workflow automation and AI agent orchestration.
•	Telegram Bot API for messaging interface with students and parents.
•	Web frontend using HTML, CSS, and JavaScript for the SmartCampusAI chat page.
•	Any LLM or NLP backend supported by n8n (e.g., OpenAI, local models) for natural-language replies.
Getting Started

1.	Clone this repository
•	git clone https://github.com/your-username/smartcampusai-agent.git
•	cd smartcampusai-agent
2.	Set up n8n
•	Install or start n8n (cloud, Docker, or local).
•	Import the provided workflow JSON from the workflows/ folder into n8n.
•	Configure credentials for your LLM provider and any external APIs used in the workflow.
3.	Configure Telegram bot (optional but recommended)
•	Create a bot using BotFather and get the bot token.
•	In n8n, add a Telegram Trigger node and set up the webhook or use a helper workflow to register the webhook URL.
•	Update the .env or n8n credentials with your TELEGRAM_BOT_TOKEN and webhook URL.
4.	Configure the web UI
•	Open the frontend/index.html file and set the API / webhook URL (the n8n Webhook node endpoint) in the JavaScript configuration.
•	Serve the frontend with any static server (e.g., Live Server, simple Node/Express static hosting, or GitHub Pages pointing to the built files).
5.	Run the project
•	Start n8n and make sure the SmartCampusAI workflow is active.
•	Open the web UI in your browser or start chatting with the Telegram bot to test the assistant.

Usage
•	Ask questions like:
•	“What are the admission fees for BCA?”
•	“Where is the admin office located?”
•	“What are today’s important events?”
•	The assistant routes the query through n8n, generates a response using the AI agent or FAQ logic, and sends back a message to web and Telegram clients.
You can customize prompts, add new nodes, or connect to real college data sources (Google Sheets, databases, LMS, etc.) directly in n8n.

Project Status and Future Work
•	Current status: Hackathon prototype of a campus assistant with working web and Telegram integrations.
•	Planned improvements:
•	Integration with real college APIs or databases for live data.
•	Better conversation memory, multi-language support, and 3D/robot avatar or facial expression understanding in future versions.

Folder Structure
•	/frontend – Web UI (HTML/CSS/JS) for SmartCampusAI chat.
•	/workflows – Exported n8n workflows for Telegram and web integration.
•	/docs – Architecture diagrams, screenshots, and additional documentation.

Contributing

Contributions, issues, and feature requests are welcome.
You can fork the repo, create a feature branch, and submit a pull request describing your changes.

Special Thanks 

We thank all contributors and collaborators who made this project possible. Special recognition to Manas and Sakir for their invaluable roles in designing, developing, and deploying the agent, ensuring it meets the dynamic needs of a smart campus ecosystem.

Together, we aim to inspire further innovations in campus automation and AI applications to support the future of education.



