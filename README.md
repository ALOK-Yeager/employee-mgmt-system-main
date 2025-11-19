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

Populate the placeholders in `.env` with your credentials when you are ready:

- `MONGO_URI`, `MONGO_USERNAME`, `MONGO_PASSWORD` for a hosted MongoDB
- `SECRET_KEY` (Flask session / JWT signing key)
- `GROQ_API_KEY`, `TOGETHERAI_API_KEY`, `CLOUDINARY_*` as needed

## 5. Start the unified application

```bash
python unified_app.py
```

By default the app listens on `http://localhost:5000`.

### Access the app from another device on the same network

1. Leave `python unified_app.py` running; it already binds to `0.0.0.0`.
2. Find the host machine IP (for example `ipconfig` on Windows).
3. From another laptop or phone on the same Wi-Fi, open `http://<host-ip>:5000`.
4. Allow the Python process through any local firewall prompt the first time.

For secure sharing over the internet, use the guides in `ALTERNATIVE_TUNNELING.md` (Cloudflare Tunnel) or `NGROK_SETUP.md`.

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