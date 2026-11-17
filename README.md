# israeli-legal-skills

Two Agent Skills for Claude, written in Hebrew, for civil litigation work in Israel:

- **takanot-2018**: the practical rules of Israel's Civil Procedure Regulations, 2018. Document structure and page limits, filing deadlines, counting of days and court recesses, and sanctions, with the full text of the regulations bundled as reference.
- **human-hebrew-writing**: rules for Hebrew writing that does not read as AI-generated text.

The skills and the rest of this page are in Hebrew. Not legal advice.

---

# סקילים ל-Claude לעבודה משפטית בעברית

שני סקילים (Agent Skills) לעורכי דין שעובדים עם Claude בעברית, בליטיגציה אזרחית בישראל.

| סקיל | מה הוא עושה |
|---|---|
| [`takanot-2018`](skills/takanot-2018/) | הכללים המעשיים של תקנות סדר הדין האזרחי, התשע"ט-2018: מבנה והיקף של כל סוג מסמך, מועדים, מניין ימים ופגרות, וסנקציות. כולל את הנוסח המלא, טבלת מועדים, רשימות בדיקה לפי סוג מסמך ורשימה של שאלות פרשנות פתוחות. |
| [`human-hebrew-writing`](skills/human-hebrew-writing/) | כללים לכתיבה בעברית שלא נשמעת כמו AI: מילים ומבנים שמסגירים טקסט של מודל, כללי פיסוק ועיצוב, ובדיקה לפני מסירה. |

הסקילים לא תלויים זה בזה, ואפשר להתקין רק אחד מהם.

## התקנה

ב-Claude Code מוסיפים את המאגר כחנות תוספים ומתקינים את הסקיל הרצוי:

```
/plugin marketplace add yotamohayon632-lgtm/israeli-legal-skills
/plugin install takanot-2018@israeli-legal-skills
/plugin install human-hebrew-writing@israeli-legal-skills
```

אפשר גם להעתיק ידנית את תיקיית הסקיל לתיקיית הסקילים האישית, או לתיקיית הסקילים של פרויקט מסוים:

```bash
git clone https://github.com/yotamohayon632-lgtm/israeli-legal-skills.git
cp -r israeli-legal-skills/skills/takanot-2018 ~/.claude/skills/
cp -r israeli-legal-skills/skills/human-hebrew-writing ~/.claude/skills/
```

לפרויקט מסוים: אותו דבר, אל `.claude/skills/` שבתיקיית הפרויקט.

ב-claude.ai דוחסים את תיקיית הסקיל לקובץ zip ומעלים אותו במסך ההגדרות של הסקילים.

## מה חשוב לדעת על takanot-2018

- **זה לא ייעוץ משפטי.** האחריות למועד ולמסמך שמוגש היא של עורך הדין שחתום עליו.
- **הנוסח אינו רשמי.** מקורו בנוסח המשולב שבוויקיטקסט, ובראש כל קובץ בתיקיית `references` מופיעים הקישור, מספר הגרסה והתאריך. ציטוט שנכנס למסמך לבית המשפט נבדק מול רשומות או מול מאגר משפטי.
- **התקנות מתוקנות מעת לעת.** הנוסח המלא נכון ל-9.10.2026. לפני שסומכים על מועד או על היקף, כדאי לבדוק בקישור אם יש גרסה חדשה יותר.
- **הטבלאות הן עיבוד.** טבלת המועדים, רשימות הבדיקה ושאלות הפרשנות נבנו מתוך הנוסח המלא ואינן חלק ממנו. במקרה של סתירה, לשון התקנות קובעת.
- **החלטה בתיק גוברת.** מועד שבית המשפט קבע בתיק גובר על הטבלה.
- הסקיל הוא ידע ולא סגנון. הוא לא קובע איך מנסחים כתב טענות.

## מה חשוב לדעת על human-hebrew-writing

הסקיל נכתב מתוך עבודה משפטית, ולכן רוב הדוגמאות בו משפטיות, אבל רוב הכללים מתאימים לכל טקסט בעברית. כלל, מדריך סגנון או פורמט קבוע של המשתמש גוברים על מה שכתוב בו.

## מקורות

- נוסח התקנות, תקנות הפגרות והוראות מנהל בתי המשפט: [ויקיטקסט](https://he.wikisource.org), נוסחים משולבים שמתעדכנים מרשומות.
- סימני כתיבה של מודלים: המדריך "Signs of AI writing" של WikiProject AI Cleanup בוויקיפדיה האנגלית.

## רישיון

הסקילים והטבלאות מתפרסמים ברישיון [MIT](LICENSE). על נוסח התקנות עצמו אין זכות יוצרים (סעיף 6 לחוק זכות יוצרים, התשס"ח-2007).

## תיקונים והצעות

מצאתם טעות במועד, בהפניה לתקנה או בכלל? פתחו issue עם מספר התקנה והנוסח הנכון.
