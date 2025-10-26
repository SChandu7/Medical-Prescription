

# 💊 Medical Prescription & Disease Information System

A smart **medical information system** built to provide **disease details, care instructions, and prescription guidance** based on user input.  
This project allows users to enter their symptoms or disease prompts and receive structured, concise, and accurate information, along with **recommended prescriptions and care tables**.

---

## 🚀 Features

- 🩺 **Symptom-based Disease Detection** — Users input symptoms or disease prompts.  
- 📋 **Structured Output** — Disease description, causes, symptoms, and care instructions.  
- 💊 **Prescription Guidance** — Suggested medications or remedies for the disease.  
- 🗂️ **Tables & Charts** — Clear, organized tables showing treatment plans and dosage.  
- 🧠 **Intelligent Prompt Handling** — Optimized prompts for concise, accurate results.  
- 🌐 **Frontend-ready** — API can be integrated with mobile apps or web dashboards.  

---

## 🧩 Tech Stack

| Component | Technology |
|-----------|------------|
| **Backend** | Python / Flask or Django (depending on implementation) |
| **Database** | SQLite / MySQL (storing diseases and prescriptions) |
| **AI / NLP** | Prompt-based AI (can be GPT / custom model) |
| **Frontend** | Flutter / Web UI (optional) |
| **API** | REST API for integration with apps |

---

## 🧠 Workflow

1. User enters **symptoms or disease prompt**.  
2. Backend processes the input using **AI/NLP models**.  
3. Disease is identified and **relevant information** is fetched from the database.  
4. Output includes:
   - Disease **description**  
   - **Causes** and **risk factors**  
   - **Symptoms table**  
   - **Care instructions and precautions**  
   - Suggested **prescriptions / medicines**  
5. Structured data is sent to frontend or displayed in **tables/charts**.  

---

## 🔧 Setup Instructions (Backend)

### 1️⃣ Clone Repository
```bash
git clone https://github.com/<your-username>/medical-prescription-system.git
cd medical-prescription-system
```
## 2️⃣ Create Virtual Environment
bash
```
python -m venv env
source env/bin/activate    # Windows: env\Scripts\activate
```
## 3️⃣ Install Dependencies
bash
```
pip install -r requirements.txt
```
## 4️⃣ Configure Database
- SQLite: Default for quick setup.
- MySQL: Update settings.py or config.py with DB credentials.
  
Example settings.py for MySQL:

python
```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'medical_db',
        'USER': 'root',
        'PASSWORD': 'password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```
## 5️⃣ Migrate Models
bash
```
python manage.py makemigrations
python manage.py migrate
```
## 📄 Models & Database Structure
Disease Model
Field	Type	Description
id	Integer	Primary Key
name	CharField	Disease Name
description	TextField	Disease Description
causes	TextField	Causes of Disease
symptoms	TextField / JSON	Symptoms list
precautions	TextField	Care instructions
medications	TextField / JSON	Suggested medications

Prescription Model
Field	Type	Description
id	Integer	Primary Key
disease	ForeignKey	Linked Disease
medicine	CharField	Name of Medicine
dosage	CharField	Recommended Dosage
duration	CharField	Duration of Treatment
notes	TextField	Additional Notes

## 🌐 API Endpoints
Method	Endpoint	Description
POST	/api/disease/	Submit symptoms / prompt and get disease info
GET	/api/disease/<id>/	Retrieve specific disease details
GET	/api/diseases/	List all diseases
POST	/api/prescription/	Add prescription for a disease
GET	/api/prescription/<id>/	Get prescription details

## 🧰 Usage Example
Request:

bash
```
POST /api/disease/
{
  "symptoms": "fever, cough, fatigue"
}
Response:

json
Copy code
{
  "disease": "Influenza",
  "description": "Influenza is a viral infection affecting the respiratory system...",
  "causes": "Influenza virus (A, B, C)",
  "symptoms": ["Fever", "Cough", "Fatigue", "Headache"],
  "precautions": "Rest, hydration, avoid contact with others",
  "medications": [
    {"medicine": "Oseltamivir", "dosage": "75mg twice daily", "duration": "5 days"},
    {"medicine": "Paracetamol", "dosage": "500mg as needed", "duration": "3-5 days"}
  ]
}
```


## 📸 Screenshots

<img width="1246" height="688" alt="image" src="https://github.com/user-attachments/assets/06e69dc6-2e76-452b-996d-18de419f220f" />


---

## 💡 Benefits
- ✅ Quick access to accurate disease information
- ✅ Clear prescription guidance
- ✅ Structured tables and charts for care instructions
- ✅ Easy integration with mobile apps, web dashboards, or AI systems
- ✅ Reduces manual searching for medical info

- 🧭 Use Cases
- 🏥 Healthcare assistants and patient guidance
- 📚 Medical education & learning
- 📱 Mobile health apps integration
- 💻 Telemedicine platforms
- ⚙️ Future Improvements


-🔹 Integration with AI chat assistants for real-time Q&A
- 🔹 Multilingual support for symptoms & prescriptions
- 🔹 Add image-based symptom recognition
- 🔹 Advanced recommendation engine for treatment & preventive care
---

## 🧑‍💻 Developer Info

Author: S. Chandu

Project Type: AI-assisted medical info system

Backend: Django/Flask REST API

Database: MySQL / SQLite

Frontend: Flutter / Web UI (optional)

---

## 🏆 License
This project is licensed under the MIT License — free to use, modify, and distribute.
