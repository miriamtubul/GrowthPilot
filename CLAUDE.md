# GrowthPilot — הנחיות לעבודה

## כלל בסיסי
אם התבקשתי לבצע משימה ואין לי את המלל או הנתונים הדרושים — **לעולם לא לפעול אוטומטית**.
תמיד לפנות למשתמשת ולבקש שתספק את החומר החסר.

## הפרויקט
- קובץ יחיד: `index.html` — הכל בפנים (CSS + HTML + JS)
- שפה: עברית, RTL (`dir="rtl"`, `lang="he"`)
- פלטפורמת העלאה: GitHub Pages (repo: GrowthPilot, branch: main)

## עיצוב
- צבע ראשי (מרים): `#135bec`
- צבע משני (רז): `#7c3aed`
- פונטים: Syne (כותרות) + DM Sans (גוף)
- סגנון: glassmorphism navbar, blob animations, כרטיסים עם shadow

## מבנה הדף
1. Navbar — יתרונות | שירותים | מי אנחנו
2. Hero
3. יתרונות (value-props)
4. שירותים (services)
5. מי אנחנו (team) — 2 כרטיסים
6. פרופיל מרים (`#miriam-profile`) — מוסתר כברירת מחדל
7. פרופיל רז (`#raz-profile`) — מוסתר כברירת מחדל
8. Footer

## אנשי קשר
- מרים טבול: 052-646-9288 | mariatar@gmail.com
- רז שמריה: 054-652-2650 | Razshmaria@gmail.com

## קבצים בתיקייה
- `raz/driveschool-app.jpeg` — תמונת אפליקציה DriveSchool
- `raz/raz-recommendation.pdf` — מכתב המלצה רז
- יש להעלות את כל התיקייה (git push מעלה הכל אוטומטית)

## טפסים וחיבור לידים
- טופס מרים: `name="miriam-leads"` — Google Sheets בלבד (Netlify Forms לא פעיל ב-GitHub Pages)
- טופס רז: `name="raz-leads"` — Google Sheets בלבד
- `MIRIAM_SHEET` — URL של Apps Script מרים (בקוד JS)
- `RAZ_SHEET` — URL של Apps Script רז: `https://script.google.com/macros/s/AKfycbzJ1JjJ5JZ0dtPyJuJe2Z0hJ2WnDPdHO4PkJgC1PuMG0CG3HMjQ6H-FW9moxPntaUob/exec`
- Apps Script צריך לקבל `e.parameter` (לא JSON) — `params.name`, `params.phone`, `params.email`, `params.business`, `params.message`

## פרופיל מרים — מבנה נוכחי
- Hero: שם + תיאור (מומחית לאוטומציות ופתרונות AI)
- פרויקטים נבחרים: 3 כרטיסי שורה (תמונה שמאל + תוכן ימין) — כמו רז
  1. דף נחיתה חכם + רשתות חברתיות/ביט/פייבוקס
  2. דף נחיתה + דשבורד נתונים
  3. דף נחיתה + אוטומציות גוגל
- טופס יצירת קשר

## פרופיל רז — מבנה נוכחי
- Hero: שם + תיאור
- מכתב המלצה (Cx-Plus) + כפתור PDF
- פרויקטים: DriveSchool + מערכת QAQC (כרטיסי שורה)
- Highlights: 3 כרטיסים (flex column)
- טופס יצירת קשר

## כלל CSS חשוב — מובייל
- inline styles **לא נדרסים** ע"י @media CSS
- לשינוי שיעבוד בנייד: לשנות ה-inline style ישירות ב-HTML
- פתרון מוכח: `display:flex;flex-direction:column` ב-inline style במקום grid

## עדכון לגיטהאב
```bash
git add .
git commit -m "תיאור השינוי"
git push
```
GitHub Pages מתעדכן אוטומטית תוך ~30 שניות.
