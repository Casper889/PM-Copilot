🧠 PM Copilot Build Tracker (Casper)
📌 Goal
Create a local AI-powered assistant that:
* Runs daily
* Gathers Bloomberg data and news for coverage tickers
* Summarizes relevant developments
* Identifies opportunities
* Outputs a digest via Markdown/email/dashboard

✅ STEP 1: Setup Bloomberg Access
Task	Details	Status
Install Bloomberg Terminal	Must run locally on your PC	☐
Install Bloomberg API SDK	From Bloomberg's software download page	☐
Install Python packages	pip install pdblp pandas	☐
Test data pull	Use bdp and bdh for tickers	☐
Save snapshot template	Decide which fields (e.g., PX_LAST, PE_RATIO, BETA)	☐

✅ STEP 2: Create Ticker Universe
Task	Details	Status
Create YAML or CSV	Ticker, Name, Sector, Internal Notes	☐
Store in repo/data directory	e.g., data/watchlist.yaml	☐
Add priority/risk flag	(e.g., “core position”, “monitor”, “avoid”)	☐

✅ STEP 3: News & IR Scraping
Task	Details	Status
Choose sources	Yahoo Finance, IR pages, Google News RSS	☐
Build scraper (requests/bs4)	Store 3–5 latest headlines per ticker	☐
Include article URLs and timestamps	For reference in summary	☐
Store results in JSON format	e.g., data/news/AAPL.json	☐

✅ STEP 4: Macro / Thematic Scraping
Task	Details	Status
Identify macro news feeds	FT, Reuters, or scraped sources	☐
Extract themes per day	Use LLM to classify topics (e.g., “China demand”, “Rates”)	☐
Save relevant stories	Connect to sectors/stocks later	☐

✅ STEP 5: LLM Integration
Task	Details	Status
Choose model	OpenAI GPT-4 (API) or local GPT (Ollama)	☐
Set up API key or local runtime	Keep secure	☐
Create summarization prompt	For single articles and multiple articles	☐
Create opportunity prompt	E.g., “Is this bullish or bearish for any coverage stock?”	☐

✅ STEP 6: Opportunity Detection
Task	Details	Status
Compare valuation/momentum	vs historical or peers (using pdblp)	☐
Use GPT to explain anomaly	“Why did XYZ’s P/E drop 12%?”	☐
Generate mini-theses	e.g., “This may present a contrarian opportunity due to…”	☐

✅ STEP 7: Generate Digest Report
Task	Details	Status
Design output format	Markdown with tables, summaries, links	☐
Add ESG alert flags	From scraping or Sustainalytics	☐
Generate chart (optional)	Use matplotlib for price/multiple chart	☐
Convert to PDF or email	Use WeasyPrint or SMTP	☐

✅ STEP 8: Automation
Task	Details	Status
Set up scheduler	cron (Mac/Linux) or Task Scheduler (Windows)	☐
Daily run at 7 AM	Bloomberg + news + LLM + output	☐
Save logs/errors	Create logs/ directory	☐
Email results	Optional: daily email to yourself	☐

🛠 Optional Enhancements
Feature	Details	Status
Slack or Telegram bot	Ask it “what’s moving today?”	☐
Dashboard UI	Streamlit or Flask frontend	☐
GPT fine-tuning	With your pitch tone and ESG policy	☐
Daily macro radar	News sentiment summarizer with sector relevance	☐
