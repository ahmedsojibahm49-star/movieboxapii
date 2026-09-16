# 🚀 MovieBox API — Deploy Guide (Bangla te)

Eta ekta **FastAPI (Python)** app. Live korer 3 ta sohoj bhav:

## Option A — Railway (recommended)
1. Railway.app e GitHub login → **New Project → Deploy from GitHub repo** → ei repo ta select.
2. `railway.json` already ache — Railway auto-build + run korbe.
3. Deploy por URL pabi (`https://xxxx.up.railway.app`) → browser e `.../home` dile JSON asleo thik ache ✅

## Option B — Render
1. Render.com → **New → Web Service** → ei repo.
2. Build: `pip install -r requirements.txt`
3. Start: `uvicorn main:app --host 0.0.0.0 --port $PORT`
4. Deploy → URL.

## Option C — Vercel
1. vercel.com → **Add New → Project** → ei repo → Framework: **Other** → Deploy.
2. `vercel.json` already ache (Python serverless config).
3. ⚠️ Free plan e serverless time limit ache — `/home` cold start e slow hote pare. Kone na hole Railway/Render use koro.

## Local e cholano
```
pip install -r requirements.txt
uvicorn main:app --host 0.0.0.0 --port 8000
# check: http://localhost:8000/home  (JSON asleo thik)
```

## Website er sathe connect
Website (streambox) project e ekta env variable deya:
```
MOVIEBOX_API_URL=<ei api er live URL>
```
- Local e: `streambox/.env.local` file e
- Vercel website e: dashboard → Environment Variables e

Tara **koy kichu code change lagbe NA**.
