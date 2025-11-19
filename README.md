# Employee Management System - Original Working Version

## 🚀 Quick Start (Original Local Setup)

This system has 3 components that work together:

### 1️⃣ **Frontend (Next.js)** - Main UI
```bash
cd employee-mgmt-system-main/frontend
npm install
npm run dev
```
**Access:** http://localhost:3000

### 2️⃣ **Backend (Flask API)** - Employee Management API
```bash
cd employee-mgmt-system-main/backend
pip install -r requirements.txt
python app.py
```
**Access:** http://localhost:5000

### 3️⃣ **Chatbot Service (Optional)** - AI Chatbot
```bash
cd employee-mgmt-system-main/backend
python chatbot_service.py
```
**Access:** http://localhost:5001

### 4️⃣ **WhatsApp Bot (Optional)** - WhatsApp Integration
```bash
cd employee-mgmt-system-main
pip install -r whatsapp_requirements.txt
python twilio_whatsapp.py
```
**Access:** http://localhost:8000
**Webhook:** http://localhost:8000/whatsapp

---

## 🎯 **What Each Component Does**

| Component | Port | Purpose |
|-----------|------|---------|
| **Frontend (Next.js)** | 3000 | Full UI with login, dashboard, chatbot widget |
| **Backend API** | 5000 | Employee management, authentication, transfers |
| **Chatbot Service** | 5001 | AI-powered chatbot responses |
| **WhatsApp Bot** | 8000 | WhatsApp integration via Twilio |

---

## ✅ **Start Everything**

### **Windows:**
```bash
# Terminal 1 - Frontend
cd employee-mgmt-system-main\frontend
npm run dev

# Terminal 2 - Backend
cd employee-mgmt-system-main\backend
python app.py

# Terminal 3 - Chatbot (Optional)
cd employee-mgmt-system-main\backend
python chatbot_service.py

# Terminal 4 - WhatsApp Bot (Optional)
cd employee-mgmt-system-main
python twilio_whatsapp.py
```

### **Mac/Linux:**
```bash
# Terminal 1 - Frontend
cd employee-mgmt-system-main/frontend
npm run dev

# Terminal 2 - Backend
cd employee-mgmt-system-main/backend
python app.py

# Terminal 3 - Chatbot (Optional)
cd employee-mgmt-system-main/backend
python chatbot_service.py

# Terminal 4 - WhatsApp Bot (Optional)
cd employee-mgmt-system-main
python twilio_whatsapp.py
```

---

## 🔐 **Login Credentials**

**Admin Account:**
- Username: `admin`
- Password: `admin123`

**Employee Accounts:**
- Username: `john.doe` | Password: `password123`
- Username: `jane.smith` | Password: `password456`

---

## 📱 **WhatsApp Integration**

See [WHATSAPP_SETUP_GUIDE.md](WHATSAPP_SETUP_GUIDE.md) for complete setup instructions.

**Quick Setup:**
1. Deploy the WhatsApp bot to a hosting provider
2. Configure Twilio webhook with your deployed URL
3. Connect teacher's phone to Twilio sandbox
4. Start chatting with the bot

---

## 🚀 **Deployment**

See [DEPLOYMENT.md](DEPLOYMENT.md) for production deployment instructions.

**Quick Deploy Options:**
- Render.com (recommended)
- Railway.app
- Heroku
- DigitalOcean

---

## 📞 **Support**

For issues or questions:
- Check troubleshooting guides in documentation
- Review logs in your IDE or hosting dashboard
- Consult DEPLOYMENT.md for deployment issues