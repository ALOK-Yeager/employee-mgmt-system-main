# Employee Management System (Unified Local Version)

Single Flask application that serves the login, dashboards, analytics, and AI assistant from one codebase. Follow these steps on any machine to run it exactly as in the repository.

## Prerequisites

- Python 3.10+ (3.13 tested)
- Git
- (Optional) `virtualenv`

## 1. Clone the repository

```bash
git clone https://github.com/ALOK-Yeager/employee-mgmt-system-main.git
cd employee-mgmt-system-main
```

## 2. Create a virtual environment (recommended)

```bash
python -m venv .venv
.venv\Scripts\activate        # Windows
# source .venv/bin/activate    # macOS / Linux
```

## 3. Install backend requirements

```bash
pip install -r requirements.txt
```

## 4. Configure environment variables

```bash
copy .env.example .env          # Windows
# cp .env.example .env          # macOS / Linux
```

The default values let the app run with mock data. Update the keys in `.env` later if you want live integrations (MongoDB, Groq, Cloudinary, etc.).

## 5. Start the unified application

```bash
python unified_app.py
```

By default the app listens on `http://localhost:5000`.

## 6. Log in with demo accounts

| Role | Username | Password |
|------|----------|----------|
| CEO / Admin | `admin` | `admin123` |
| Zone Education Officer | `zeo1` | `zeo123` |
| School Admin | `school1` | `school123` |
| Staff | `staff1` | `staff123` |

Successful login redirects to the unified dashboard where you can access analytics, employee records, transfers, login logs, and the AI assistant widget.

## Optional tooling

- `scripts/setup-env.js`: generates `.env` interactively (Node.js required).
- `ALTERNATIVE_TUNNELING.md`: instructions for exposing localhost via Cloudflare Tunnel/Ngrok for demos.

That’s it—clone, install, copy `.env`, run `unified_app.py`, and share the provided demo credentials.