# AvianQuest: Pocket Vet AI 🦜

[![Python Version](https://img.shields.io/badge/python-3.10%20%7C%203.11%20%7C%203.12-blue?style=for-the-badge&logo=python)](https://www.python.org)
[![Flet UI Framework](https://img.shields.io/badge/Flet-v0.85.2-purple?style=for-the-badge&logo=flutter)](https://flet.dev)
[![Gemini Engine](https://img.shields.io/badge/Gemini%20AI-2.5%20Flash-orange?style=for-the-badge&logo=google-gemini)](https://ai.google.dev)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

**AvianQuest** is a modern, cross-platform interactive desktop and mobile application designed to provide specialized pre-ownership education and visual diagnostic support for exotic bird care. Powered by Google Gemini 2.5 Flash, it guides bird owners through routine consistency tracking, diagnostic courses, visual inspections, and empathetic virtual vet consultations.

---

## 🌟 Key Features

* **🩺 Pocket Vet AI:** A real-time, asynchronous streaming chat interface delivering professional, structured advice constrained strictly to avian veterinary health.
* **👁️ Avian Eye (Vision Diagnostics):** Multi-modal image scanner. Upload photos of your bird (to identify species/mutations/health indicators), cage setups (for safety audits), or droppings (for digestive health diagnostics).
* **📅 Academic Seasonal Routine:** Dynamic, gamified routine trackers customized for your bird type across all four seasons (Summer, Winter, Spring, Breeding) with a timed-completion scoring system.
* **🎓 Flight School:** A modular, milestone-unlocked learning curriculum (Diet, Trust, Genetics, Hazards, Breeding) with interactive custom quizzes tailored for Lovebirds, Budgies, Cockatiels, and Zebra Finches.
* **🏆 Performance Analytics & PDF Certificate:** A detailed mastery dashboard that grades your bird-care knowledge and automatically generates a high-quality landscape PDF Certificate of Excellence on your desktop once you reach 95% proficiency.
* **🔒 Secured Local Privacy:** Encrypted local account setups using `bcrypt` password hashing and fully contained local session/chat histories backed by SQLite.

---

## 🛠️ Built With

* **Core Language:** Python 3.10+
* **GUI Engine:** [Flet](https://flet.dev) (Modern Flutter wrapper for Python)
* **Intelligence Core:** [Google GenAI SDK](https://github.com/google/generative-ai-python) (`gemini-2.5-flash`)
* **Database Engine:** SQLite3 (Standard Python integration)
* **Security:** `bcrypt` (Cryptographic salt password hashing)
* **Document Services:** `fpdf2` (Vector PDF Certificate compiler)

---

## 📂 Project Directory Structure

```text
Avian Quest/
│
├── docs/                                 # Centralized Documentation
│   ├── AI_PROMPTS.md                     # Engineering prompts and system prompts
│   └── GitHub_Professional_Repository_Standards_v2.docx
│
├── tests/                                # Automated Test Suites
│   └── test_avianquest.py                # Database, Auth, and Edge Case testing
│
├── views/                                # Flet Application Frontend Engines
│   ├── engine_a_routine.py               # Habit scheduler and seasonal challenges
│   ├── engine_b_lessons.py               # Milestone curriculum and interactive quizzes
│   ├── engine_c_avian_eye.py             # Multi-modal camera visual scanner
│   ├── engine_d_chat.py                  # Generative streaming pocket vet consultant
│   ├── engine_e_risk.py                  # Grade tracking & PDF Certificate downloader
│   ├── engine_f_auth.py                  # Bcrypt secure sign-in / registration
│   ├── engine_g_settings.py              # Account preferences and logout controller
│   └── engine_h_onboarding.py            # Personalization questionnaire
│
├── database/                             # Database Models and Seeding Logic
│   └── db_manager.py                     # SQLite migrations and alert bank configurations
│
├── .env.example                          # Local environment variables template
├── .gitignore                            # Smart Git exclusions list
├── main.py                               # Application main entrypoint
├── pyproject.toml                        # Pytest lookup configurations
├── requirements.txt                      # Project dependencies
└── README.md                             # Repository main landing page
```

---

## 🚀 Installation & Local Setup

### 1. Clone the Repository
```bash
git clone https://github.com/Najeeb1106/webeng-project-aliahmad-najeeb.git
cd "Avian Quest"
```

### 2. Install Project Dependencies
Ensure you have Python installed, then run the pip installer:
```bash
pip install -r requirements.txt
pip install flet google-genai fpdf2
```

### 3. Configure Your Environment Keys
1. Get a free API key from [Google AI Studio](https://aistudio.google.com/).
2. Create a new file named exactly **`.env`** in the root directory.
3. Add your key inside the `.env` file like this (do not use quotes or spaces around the equals sign):
```env
GEMINI_API_KEY=your_actual_api_key_here
```

### 4. Run the Application
Execute the main script to launch the Flet desktop window:
```bash
python main.py
```

---

## 🧪 Running Automated Tests
We use `pytest` to verify database integrations, secure authentication hashing, and scoring edge-case logic. 

To run the full suite from the root folder:
```bash
pytest
```

---

## 📖 Known Constraints & Guidelines
* **Avian Scope Constraint:** The chat and vision engines will politely decline to answer prompts, diagnose images, or give recommendations unrelated to exotic birds and avian health.
* **Local Storage Only:** AvianQuest stores all user metrics, daily habits, and chat histories entirely on your local machine using SQLite. Deleting the `database/avianquest.db` file will reset all progress.

---

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.