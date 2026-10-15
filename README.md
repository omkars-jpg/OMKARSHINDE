# Food by Soni 🍽️  (Flask + SQLite + HTML/CSS/JS)

## Run in VS Code
1. Unzip, then File > Open Folder > `food_by_soni`
2. Terminal > New Terminal, then:
   - Windows:  `python -m venv venv` then `venv\Scripts\activate`
   - Mac/Linux: `python3 -m venv venv` then `source venv/bin/activate`
3. `pip install -r requirements.txt`
4. `python app.py`
5. Open http://127.0.0.1:5000

(If PowerShell blocks activate: `Set-ExecutionPolicy -Scope Process Bypass`)

## Logins
- Admin: admin@foodbysoni.com / admin123  -> /admin
- Customer: use Sign up
- Coupons: WELCOME50, SONI20, FREEDEL

## Reset data
Stop server, delete `foodbysoni.db`, run again.


## Vercel deployment
- The Vercel entry point is `api/index.py`; configuration is in `vercel.json`.
- Import the repository root containing `app.py`, `requirements.txt`, `templates/`, `static/`, `api/`, and `vercel.json`.
- SQLite uses `/tmp` on Vercel because the deployment filesystem is read-only. Data written there is temporary and can reset; use a persistent hosted database for real customers/orders.
- Set `SECRET_KEY` as a Vercel environment variable before production use.
