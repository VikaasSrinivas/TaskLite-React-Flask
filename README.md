# TaskLite — React + Flask + SQLite

## Requirements
Python 3.10+ and Node.js/npm. MongoDB is not needed.

## Backend (VS Code terminal 1)
```powershell
cd backend
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python app.py
```
If activation is blocked:
```powershell
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe app.py
```
Backend runs at http://127.0.0.1:5000

## Frontend (VS Code terminal 2, from project root)
```powershell
cd frontend
npm install
npm run dev
```
Open the URL shown by Vite, usually http://localhost:5173.

Features: add tasks, mark complete/incomplete, delete tasks. SQLite database is created automatically at `backend/tasks.db`.

Architecture: React UI -> Flask REST API -> SQLite database. This is not technically MERN; Python replaces Express/Node backend and SQLite replaces MongoDB.
