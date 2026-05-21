# פרויקט 4 - ניתוח נתונים ב-`Power BI`

## Project 4 - Analyze Data with Power BI

---

### פרטי הפרויקט / Project Info

- **קורס / Course:** John Bryce / Matrix - Data Analyst
- **שם הפרויקט / Project Name:** Coffee Shop Sales Performance Analytics
- **מקור הנתונים / Dataset Source:** Maven Analytics – Coffee Shop Sales
- **קובץ ראשי / Main File:** `Coffee_Shop_Sales_FINAL_v2.pbix`

---

## סקירה כללית / Quick Overview

בפרויקט הזה אני ניתחתי את ביצועי המכירות של רשת בתי קפה הפועלת בשלושה סניפים בעיר ניו יורק (Astoria, Hell's Kitchen, Lower Manhattan) במחצית הראשונה של שנת 2023. עבדתי עם מערך הנתונים הציבורי של Maven Analytics, שמכיל **149,116 טרנזקציות** בהיקף כולל של **$698,812** הכנסות. ניקיתי, מידלתי וטיפלתי בנתונים ב-`Power Query` לפני שטענתי אותם לדאשבורד אינטראקטיבי שעיצבתי בעצמי. הדאשבורד שבניתי מורכב מחמישה דפים, ואני מציע בו פילוחים לפי קטגוריות מוצר, סניפים וזמן, יחד עם תחזית מכירות, `Drill Through` ו-`Bookmarks` שמובילים את המשתמש לתובנות עסקיות מעשיות. המטרה שלי הייתה לזהות אילו מוצרים, שעות וסניפים מניעים את הצמיחה ולספק המלצות מנומקות לקבלת החלטות.

---

## כיצד לפתוח את הפרויקט / How to Open

1. הורידו את התיקייה במלואה למחשב מקומי (אל תפתחו ישירות מענן – חלק מהנתיבים יחסיים).
2. פתחו את הקובץ `Coffee_Shop_Sales_FINAL_v2.pbix` באמצעות `Power BI Desktop` בגרסה **May 2024** ומעלה.
3. ה-`Theme` שעיצבתי (`CoffeeHouse_Linen_Theme.json`) כבר מוטמע בקובץ – אין צורך לטעון מחדש.
4. במידה ונפתחת הודעת רענון – לחצו על **Apply Changes**; הנתונים הגולמיים נמצאים בתת-התיקייה `Data/`.
5. לצפייה מהירה ללא `Power BI Desktop` – פתחו את הקובץ `Coffee_Shop_Performance_Analytics_FINAL_REPORT.pdf` שייצאתי.

---

## מה יש בתיקייה / What's Inside the Folder

| קובץ / File | תיאור / Description |
|---|---|
| `Coffee_Shop_Sales_FINAL_v2.pbix` | קובץ ה-`Power BI` הראשי שבניתי להגשה (הגרסה הסופית). |
| `Coffee_Shop_Performance_Analytics_FINAL_REPORT.pdf` | ייצוא PDF של כל חמשת דפי הדאשבורד שלי לצפייה מהירה. |
| `01_DOC1_הסבר_מקדים.md` | **DOC1** – הסבר מקדים שכתבתי על הפרויקט, מטרות ושאלות מחקר. |
| `02_DOC2_תיאור_תהליך.md` | **DOC2** – תיאור מלא של תהליך העבודה שלי, מ-ETL ועד עיצוב. |
| `00_איך_לצפות_בפרויקט.md` | מדריך תצוגה למשתמש (סדר מומלץ לקריאת הדפים). |
| `03_מדריך_שלב_שלב_PowerBI.md` | תיעוד בנייה שלב-אחר-שלב של הדאשבורד שיצרתי. |
| `04_DAX_מדדים_מוכנים.md` | מילון מדדי `DAX` שכתבתי במודל. |
| `05_עיצוב_5_דוחות.md` | מסמך עיצוב שהכנתי לכל אחד מ-5 הדפים. |
| `06_סגירת_דרישות_והשלמת_הגשה.md` | מסמך בדיקה שערכתי מול דרישות הקורס. |
| `Data/Coffee Shop Sales.xlsx` | מערך הנתונים הגולמי (Maven Coffee Shop Sales). |
| `CoffeeHouse_Linen_Theme.json` | קובץ `Theme` שעיצבתי בנושא קפה. |
| `Templates/`, `Previews/`, `Dashboard_Redesign/` | תיקיות עבודה ותצוגות מקדימות מתהליך העיצוב שלי. |

---

## סיור בדפי הדאשבורד / Dashboard Pages Tour

### דף 1 – Cover (כריכה)
דף פתיחה ויזואלי שעיצבתי, הכולל לוגו, כותרת הפרויקט, פרטי הקורס, וטבלת תוכן עניינים אינטראקטיבית. הוספתי ניווט בין הדפים באמצעות לחצנים מותאמים אישית (Buttons) שקישרתי ל-`Bookmarks`. בנוסף שילבתי תקציר KPI מהיר: הכנסה כוללת, מספר טרנזקציות וטווח התאריכים שניתחתי.

### דף 2 – Sales Summary (סקירת מכירות)
הדף הזה מציג את התמונה הכוללת של ביצועי הרשת. בניתי בו **KPI Cards** מרכזיים, גרף עמודות של הכנסות לפי חודש עם `Trend Line` שהוספתי, פילוח לפי `Product Category`, ותחזית 30 יום קדימה שיצרתי באמצעות `Analytics Pane`. תכננתי את הדף הזה כך שישמש את ההנהלה לראייה אסטרטגית של ביצועי החצי-שנה.

### דף 3 – Product Performance (ביצועי מוצרים)
בדף הזה אני מציג ניתוח מעמיק של 80+ מוצרים ב-9 קטגוריות. בניתי **Treemap** של קטגוריות, **Bar Chart** של Top 10 מוצרים מכניסים, ומטריצה היררכית עם `Drill Down` מ-Category → Type → Detail שהגדרתי. הוספתי גם ויזואל `Decomposition Tree` כדי לאפשר חקירה דינמית של מקורות ההכנסה.

### דף 4 – Stores Performance (ביצועי סניפים)
בדף הזה אני משווה בין שלושת הסניפים: Astoria, Hell's Kitchen ו-Lower Manhattan. כללתי **Map Visual** עם בועות פרופורציונליות לפי הכנסה, מטריצת השוואה לכל KPI, ו-**Small Multiples** שעוזרים לזהות דפוסים ייחודיים לכל סניף. הגדרתי תכונת `Drill Through` שמאפשרת ללחוץ על סניף ולעבור לדף מפורט שלו.

### דף 5 – Time & Insights (זמן ותובנות)
דף שבו אני חוקר את דפוסי השעות והימים. בניתי **Heatmap** של מכירות לפי שעה ביום ויום בשבוע, גרף קווי של מגמת המכירות היומית, וקלפי תובנה (Insight Cards) שכתבתי, שמסכמים ממצאים מפתח: שעות שיא, ימים חזקים, וזיהוי שעות שקטות עם פוטנציאל לקידום מכירות.

---

## מספרים מרכזיים לאימות / Key Numbers (Grader Verification)

| מדד / Metric | ערך / Value |
|---|---|
| **Total Revenue** | $698,812 |
| **Total Transactions** | 149,116 |
| **Total Quantity Sold** | 214,470 units |
| **Average Transaction Value** | ~$4.69 |
| **Number of Stores** | 3 (Astoria, Hell's Kitchen, Lower Manhattan) |
| **Number of Product Categories** | 9 |
| **Number of Unique Products** | 80 |
| **Date Range** | 01/01/2023 – 30/06/2023 (181 days) |
| **Top Category by Revenue** | Coffee |
| **Top Performing Store** | Hell's Kitchen |

---

## טכניקות שהוצגו בפרויקט / Techniques Demonstrated

- **`Power Query` (M Language)** – ניקיתי נתונים, יצרתי עמודות מותאמות, מיזגתי והוספתי שאילתות וטיפלתי בערכי NULL.
- **Data Modeling** – בניתי `Star Schema` עם טבלת עובדות וטבלאות ממדים (Date, Product, Store).
- **`DAX` Measures** – כתבתי למעלה מ-25 מדדים מותאמים, כולל שימוש ב-`CALCULATE`, `FILTER`, `SUMX`, `DIVIDE`.
- **Time Intelligence** – השתמשתי בפונקציות `DATEADD`, `SAMEPERIODLASTYEAR`, `TOTALYTD` ועוד.
- **Forecast** – הוספתי תחזית 30 יום על גרף קווי באמצעות `Analytics Pane`.
- **`Drill Through` Pages** – הגדרתי מעבר מנקודת נתונים לדף מפורט.
- **`Bookmarks` + Selection Pane** – יצרתי ניווט אינטראקטיבי וסיפור נתונים (Data Storytelling).
- **Custom Visuals** – שילבתי ויזואלים מותאמים מ-`AppSource` (Decomposition Tree, Small Multiples).
- **Conditional Formatting** – הגדרתי צבעוניות דינמית בטבלאות ומטריצות.
- **Custom Theme** – עיצבתי `Theme` מאוחד בנושא קפה (`CoffeeHouse_Linen_Theme.json`).
- **Tooltips Pages** – יצרתי Tooltips מותאמים אישית להעמקת המידע ב-hover.
- **`What-If` Parameters** – הוספתי פרמטרים שמאפשרים למשתמש לבדוק תרחישים.

---

## תודות / Acknowledgments

- **Maven Analytics** – על מערך הנתונים הציבורי האיכותי ששימש את הפרויקט שלי (Maven Coffee Shop Sales Dataset).
- **John Bryce / Matrix** – על מסגרת הקורס, התרגול והליווי המקצועי לאורך הדרך.

---

*נוצר במאי 2026 / Created in May 2026*
