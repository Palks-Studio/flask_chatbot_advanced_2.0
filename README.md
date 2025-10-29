<p align="center">
  <img src="docs/images/Palks_Studio.png" alt="Palks Studio" width="1200">
</p>

<p align="center">
  [🇬🇧 English](README.md) | [🇫🇷 Français](README_FR.md)
</p>

<p align="center">
  <a href="https://palks.gumroad.com/" target="_blank" style="background-color:#0a5645; color:white; padding:10px 20px; border-radius:8px; text-decoration:none; font-weight:bold;">
    View all packs on Gumroad
  </a>
</p>

# Flask Chatbot – Advanced Professional Template (Version 2.0)

A complete project to create your own **conversational assistant with Flask**, ready to use:
- **locally (localhost)**
- **on shared hosting like o2switch (Passenger / cPanel)**

No external database, no hidden dependencies. You can use it as-is, modify it, or integrate it into another site / API.

---

## Structure (Public version)

```
Flask_Chatbot_Advanced_2.0/ (Version lite)
│
├── README_EN.md                   ← Main documentation (public)
├── LICENSE.txt                    ← Proprietary license (Palks Studio)
├── CUSTOMISATION.md               ← Customization guide and explanations
├── requirements.txt               ← Main Python dependencies
├── .env.example                   ← Example of API configuration
│
├── public_version/
│   ├── example_structure.txt      ← Full project structure overview (no code)
│
└── docs/
    ├── images/
    │   └── Palks_Studio.png       ← Palks Studio logo
```


*This directory structure is provided for informational purposes only.*

**⚠ Important**

This GitHub repository is only a partial preview of the project.
The `README.md` file represents only a small portion of the full documentation.

The commercial version includes:
- the complete source code (Python, HTML, JSON, scripts)
- all documentation (INSTALL.md, TECHNICAL_README.md, examples, prompts, advanced customization…)
- automatically generated files (`.env`, `data.db`, AI memory, etc.)

The full source code is available exclusively under the **commercial licensed version**.

---

## Key Features

- **Ready-to-use API:** `/chat` and `/` work immediately after installation
- **Compatible with o2switch / Passenger (shared hosting)**
- **No database required** (JSON file only)
- **Readable, commented code, easily customizable**
- **CORS enabled:** can be used with a website or front-end interface
- **Built-in logging system:** errors automatically recorded in `/logs/` folder
- **Integrated graphical interface:** access via `/ui` (live chat in browser)

---

## Automatically Generated Files

When you run the chatbot for the first time, some files are automatically created:

| File           | Purpose                                        |
|----------------|------------------------------------------------|
| `data.db`      | SQLite database that stores conversations (created automatically if `ENABLE_PERSISTENCE=true`) |
| `logs/errors.log` | Created only if a server error occurs |
| `.env`         | Must be created manually from `.env.example` if you want to enable OpenAI |

⚠ **These files are not included in the project archive.**

---

## Operating Modes

| Mode                     | Description                                                              | Requires OpenAI Key |
|--------------------------|--------------------------------------------------------------------------|----------------------|
| **Local JSON** (default) | Responses are generated from the `sample_data.json` file                 | No                   |
| **OpenAI GPT** (optional)| Uses the ChatGPT API if an API key is provided in the `.env` file        | Yes                  |

The mode is automatically selected based on whether the `OPENAI_API_KEY` variable is present in the `.env` file.
No token usage occurs if no key is provided.

---

## Error Logs

The `logs/` folder is used to automatically record Flask server errors.
- The file `logs/errors.log` is created automatically if an error occurs.
- The `logs/` folder is generated if it does not exist (no need to create it manually).
- Each error entry contains:
  - the date and time
  - the error message
  - the full traceback for easier debugging

This system works in:
- local mode
- with or without OpenAI
- production (Passenger / shared hosting)

---

**Note**
This GitHub repository showcases the structure and features of the project.
It does not include the full executable source code, prompts, or sensitive files (.env, data.db, AI memory, etc.).
The complete version is available under a commercial license.

**Full version of the project available here**
https://ko-fi.com/palksstudio  
http://palks-studio.itch.io/  
https://palks.gumroad.com/

---

## Credits & License

This template is an original creation by Palks Studio.
Resale, redistribution or public modification without permission is prohibited.
Personal and professional use is allowed.

**Palks Studio**
Creator of useful and self-contained tools: scripts, templates and ready-to-use bases.
Simplicity, clarity, efficiency.

GitHub: https://github.com/Palks-Studio  
Gumroad: https://palks.gumroad.com/  
Discord: https://discord.gg/kzrSyThyZ7  
Twitter (X): https://x.com/PalksStudio  
Itch.io: http://palks-studio.itch.io/  
Ko-Fi: https://ko-fi.com/palksstudio

---

## Signature

_Created by **Palks Studio** — Version 2.0 (Advanced Edition)_
_Compatible with Python 3.12+ / Flask 3.0+_
