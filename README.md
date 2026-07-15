# Hi there, I'm Arnav! 👋

I'm a software developer passionate about building practical desktop applications, engaging web platforms, and creating utility plugins. 

---

## 🚀 Projects & Platforms

### 🔌 [Brella.co.in](https://brella.co.in)
A dedicated platform where I host and distribute **custom-built plugins** I’ve designed. Everything on Brella is available to download completely **for free** to help developers and creators streamline their workflows.

### ⚽ [Footyhunt.com](https://footyhunt.com)
The ultimate matchmaking service and platform for football game enthusiasts. Whether you are looking to jump into a local match, coordinate with players, or manage teams, **Footyhunt** connects football lovers seamlessly.

---

## 🛠️ Spotlight Project: WordForge

> **Tkinter-based GUI Wordlist Builder for Authorized Security Testing**

**WordForge** is a context-aware wordlist generator designed for pentests, red-team engagements, CTFs, and defensive password auditing. It operates entirely locally, runs cross-platform (Windows & Linux), and features optional integration with local LLMs via Ollama.

### 🔒 Operational Philosophy & Ethics
* **Safe & Legal Testing:** WordForge only generates candidate strings and downloads reputable, legally-distributed public dictionaries. It **never** connects to, authenticates against, or attacks any target. 
* **Zero PII (Personally Identifiable Information):** It intentionally does not crawl for or auto-download stolen credential breach dumps. Standard public research corpora (like SecLists, RockYou) are used, with built-in parsers ensuring all username/email records are automatically filtered out.

---

### ✨ Key Features & Generation Modes

* **WiFi Wordlist:** Tailored WPA/WPA2 passphrase candidates (8–63 chars). Richly mutates the SSID (years, digits, PINs, common variations) and appends onto actual wordlists.
* **Email Wordlist:** Generates account-password candidates (6–64 chars) based on target context (names, pet, company, hobbies, dates) without building passwords directly from the email string.
* **Browse Tab:** Directly search and download legally-distributed public dictionaries (SecLists, RockYou, CrackStation). WordForge automatically checks for updates on launch.
* **Smart Hybrid Architecture:**
  * **Markov Model:** Features a built-in character-level Markov model (`localmodel.py`) trained on embedded weak-password patterns—runs entirely offline without external dependencies.
  * **Rule Engine:** Executes robust CUPP/CeWL-style token mutations (leetspeak, common prefixes, case variations).
  * **Ollama Integration (Optional):** Dynamically blend outputs from local LLMs (like Llama 3 or Mistral) running on your localhost.

---

### 📦 Installation & Setup

WordForge has zero third-party runtime dependencies and runs on Python's standard library (**Tkinter**).

#### 🪟 Windows
The fastest path is to run the prebuilt standalone executable (which bundles Python and Tkinter):
1. Grab `dist/WordForge.exe` from the repository.
2. Double-click to run!

To run or compile from source:
```powershell
# Clone and run
git clone [https://github.com/arnav42069/WordForge.git](https://github.com/arnav42069/WordForge.git)
cd WordForge
python app.py

# Build the executable yourself
pip install pyinstaller
pyinstaller --onefile --windowed --name WordForge app.py
