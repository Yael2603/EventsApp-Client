# EventsApp-Client — אתר "SHOW הפקות"

צד הלקוח (React) של מערכת ניהול האירועים. השרת (ASP.NET Core Web API) נמצא בריפו נפרד:
https://github.com/Yael2603/EventsApplication

## טכנולוגיות
React, Vite, React Router, Axios. ממשק בעברית (RTL).

## הרצה מקומית
```bash
npm install
npm run dev
```
האתר זמין ב-http://localhost:5173.
כתובת ה-API נקבעת בקובץ `.env.development` במשתנה `VITE_API_URL` (ברירת מחדל: `http://localhost:8080`). אחרי שינוי בקובץ יש להפעיל מחדש את `npm run dev`.

## בנייה ופריסה
```bash
npm run build
```
התוצר נוצר בתיקיית `dist`. הפריסה ב-Render כ-Static Site:
- Build Command: `npm install && npm run build`
- Publish Directory: `dist`
- משתנה סביבה: `VITE_API_URL` = כתובת ה-API

בשרת יש להגדיר את כתובת האתר ב-`Cors__AllowedOrigins__0`.

## מבנה
- `src/api` — קריאות לשרת (Axios, טוקן JWT בכותרת, CorrelationId לכל בקשה)
- `src/auth` — התחברות והגנה על דפים לפי תפקיד
- `src/pages` — דפי לקוח, ספק ומנהל
- `src/components` — רכיבי ממשק משותפים

## כתובת באינטרנט
https://eventsapp-client.onrender.com
