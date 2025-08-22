# GIGCCL Sports Portal

This is the **GIGCCL Sports Portal**, developed as a Final Year Project.  
It is built with **Django** (Python Web Framework) and provides digital management of sports activities, including events scheduling, players/teams registration, events results and more.
---

## Project Structure
```
giccl_sports_portal/
│
├── giccl_sports_portal/      # Main Django project (settings, urls, wsgi, asgi)
│
├── sports_base/              # Sports-related app (sports, events, coaches, gallery, notification etc.)
├── Sports_Users/             # Users app (auth, profiles, dashboard, certificates, etc.)
├── static_pages/             # Static content app (base.html, home, result, teams, aboutus etc.)
│
├── media/                    # Uploaded files (profiles, certificates, schedules, logos, etc.)
├── static/                   # Static assets (images)
│
├── venv/                     # Virtual environment (not for deployment)
├── manage.py                 # Django management script
├── db.sqlite3                # SQLite database
├── requirements.txt          # Project dependencies
└── README.md
```
---

## 🛠️ Tech Stack & Tools
- **Programming & Frameworks:** Python, Django, HTML, CSS, JavaScript, Bootstrap  
- **Poppler:** PDF to Image Converter  
- **Database:** SQLite3  
- **IDE & Tools:** Visual Studio Code 

---

##  Requirements
Before setting up, ensure you have:
- **Python** (version 3.12.10 recommended)
- **Pip** (Python package installer) 
- Virtual environment (venv) setup knowledge  
- Required Python dependencies listed in `requirements.txt`  
- Modern browser (Chrome/Firefox/Edge)  

---

## ⚙️ Installation & Setup

This section includes the basic project setup and configuration for asynchronous processing with Docker and Redis.

### Basic Project Setup

Follow these steps to download and set up the GICCL Sports Portal project:

1. **Extract the Project**
    Unzip the project folder if it is in `.zip` format.

2. **Create Virtual Environment (Skip if `sp_venv` is already included)**
```bash
python -m venv sp_venv
```

3. **Move Project to Virtual Environment**
   - Copy the `GICCL_Sports_Portal` folder into the `sp_env` directory.

4. **Activate Virtual Environment**
- **Windows**:
```bash
sp_venv\Scripts\activate
```
- **Mac/Linux**:
```bash
source sp_venv/bin/activate
```

5. **Install Dependencies**
   ```bash
   cd GICCL_Sports_Portal
   pip install -r requirements.txt
   ```

6. **Install Poppler**
   - **On Windows:** download Poppler from the official GitHub release page,
   - uzip the Release-24.08.0-0
   - **Extract it** (**e.g., to C:\poppler)
   - **Add the bin folder to your System PATH:** C:\poppler\Library\bin

7. **Apply Database Migrations**
   ```bash
   python manage.py migrate
   python manage.py collectstatic
   ```

8. **Create Superuser for Admin Access**
```bash
   python manage.py createsuperuser
   ```
   Provide:
   - Email  
   - Password  
   - Password (again)  


9. **Run the Development Server**
```bash
python manage.py runserver
```

### 8️⃣ Open in Browser
Visit:
```
http://127.0.0.1:8000/
```

---

##  Admin Login
After creating the superuser in Step 8, login at:

- **URL:** http://127.0.0.1:8000/admin/
- **Email:** (the one you created)
- **Password:** (the one you set)

---

##  Notes
- Keep the `media/` folder so that uploaded images and PDFs display correctly.
- If `requirements.txt` is missing, you can generate it with:
```bash
pip freeze > requirements.txt
```

---

## Developed By
**Group 13(Morning 2021-2025)**  
BS Information Technoogy — Final Year Project  