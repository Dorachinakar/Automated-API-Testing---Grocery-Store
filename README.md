# Automated-API-Testing---Grocery-Store

# 🛒 Grocery Store API – Automated Testing with Postman

פרויקט זה הוא חלק מקורס בדיקות אוטומטיות ובודק את ה-API של חנות מכולת פשוטה שנבנתה לצורכי תרגול.  
הבדיקות נכתבו באמצעות Postman והן כוללות תרחישים נפוצים כמו התחברות, קבלת מוצרים, הוספה לעגלה ורכישה.

## 🚀 תכולת הפרויקט

- `grocery-store-tests.postman_collection.json` – קובץ הקולקשן של Postman
- `grocery-store-env.postman_environment.json` – קובץ סביבה עם משתנים כמו טוקנים, baseURL וכו'
- `README.md` – תיעוד הפרויקט

## 🧪 תרחישי בדיקה לדוגמה

- התחברות משתמש
- קבלת רשימת מוצרים
- הוספת מוצר לעגלה
- צפייה בעגלה
- ביצוע רכישה
- ניהול טוקן גישה
- בדיקות שגיאה (Unauthorized, Not Found וכו')

## 📦 הרצה עם Newman

כדי להריץ את הבדיקות מחוץ ל־Postman (ב-CI/CD למשל), אפשר להשתמש ב־Newman – הכלי של Postman לשורת הפקודה.

### התקנת Newman

```bash
npm install -g newman
הרצת הקולקשן
ללא סביבה:

bash
Copy
Edit
newman run grocery-store-tests.postman_collection.json
עם קובץ סביבה:

bash
Copy
Edit
newman run grocery-store-tests.postman_collection.json -e grocery-store-env.postman_environment.json
הפקת דוח HTML
bash
Copy
Edit
newman run grocery-store-tests.postman_collection.json \
  -e grocery-store-env.postman_environment.json \
  -r cli,html --reporter-html-export report.html
📂 איך להשתמש בפרויקט
פתח את Postman

יבא (Import) את הקולקשן והסביבה

ערוך את משתני הסביבה במידת הצורך

הרץ את הבדיקות מתוך Postman או דרך שורת הפקודה עם Newman

🧠 השראה
ה-API נלקח מתוך הפרויקט של Valentin Despa, כחלק מתרגול מעשי בקורס בדיקות API.

✍️ נכתב על ידי
דור אחינקר – תלמיד QA אוטומציה
