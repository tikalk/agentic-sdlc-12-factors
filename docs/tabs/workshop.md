# Workshop: The Agentic SDLC in Practice


## Moving from Individual Productivity to Team Velocity.

<p dir="rtl">
סדנה מעשית למפתחים על עבודה מובנית עם כלי AI בפיתוח תוכנה. \
להקנות למפתחים מתודולוגיה סדורה (Playbook) לשימוש בכלי AI, להפוך את השימוש האישי בתהליך מובנה, מדיד וניתן לשכפול, ובכך להאיץ את ה-velocity של כל צוות הפיתוח.</p>



## <p dir="rtl">
כלים</p>




* [מצגת](https://docs.google.com/presentation/d/1x3IsreZXz8XwPSyn4zUMF41qN9Zv4XmM5e6_6ecWCzU/edit?slide=id.p#slide=id.p)
* נייר עבודה
* לוח עבודה שיתופי
* סביבת IDE עם Coding Agent (כמו Cursor או VS Code עם Copilot, וכו')
* [ה-Repository של ai-team-directive](https://github.com/tikalk/agentic-sdlc-team-ai-directives)


## <p dir="rtl">
הכנות למנחה (לפני המפגש הראשון)</p>


<p dir="rtl">
כדי להבטיח שהסדנה תתחיל בצורה חלקה ולחסוך זמן יקר על תקלות טכניות, חיוני לבצע את ההכנות הבאות:</p>




* **שליחת מייל מקדים למשתתפים (לפחות 3 ימים לפני המפגש):**
    * **נושא:** הכנה לסדנת Agentic SDLC Playbook
    * **תוכן:**
        * **דרישות קדם (Prerequisites):** יש לוודא שמותקן אצל כל משתתף IDE עם AI Assistant פעיל (למשל, Cursor, VS Code עם GitHub Copilot וכו').
        * **משימת הכנה חובה:** יש לכלול במייל את ההוראות המלאות לביצוע **"תרגיל 0: חיבור למנוע העבודה המרכזי (IDE Setup)"** ולבקש מהמשתתפים להגיע למפגש הראשון לאחר שווידאו שהחיבור הצליח (כלומר, הם מצליחים להריץ את הפקודה @team ומקבלים תגובה).
        * **הערה חשובה:** הדגישו שהשלמת משימת ההכנה תאפשר לנו להתמקד בתוכן המהותי של הסדנה.


# <p dir="rtl">
מפגש 1: יסודות ה-Agentic SDLC - מאסטרגיה ל-Mission Brief</p>



## <p dir="rtl">
במפגש הראשון נבין את ה"למה" - מדוע הצלחות אישיות עם AI לא מתורגמות להצלחה צוותית. נלמד את שינוי התפיסה הנדרש ("המפתח כ-Orchestrator"), נסקור את עקרונות המתודולוגיה, ונתרגל את השלבים הראשונים הקריטיים ביותר ב-Playbook, החל מהגדרת סביבת העבודה ועד ליצירת Mission Brief מבוסס Context.</p>



## <p dir="rtl">
מבוא</p>




* **<span style="text-decoration:underline;">הקדמה: אתגר ה-Scale</span>**
    * הצגת הבעיה המרכזית: "From Individual Gains to Team Failure".
    * למה "Vibe Coding" עם AI יוצר Tech Debt? (Inconsistent Output, Knowledge Gap, Unpredictable Velocity).
    * המטרה שלנו: לעבור מעבודה אד-הוק לתהליך מובנה שמגביר את מהירות הצוות כולו.
* **<span style="text-decoration:underline;">הצגת המתודולוגיה: The 12 Factors of Agentic SDLC</span>**
    * סקירה מהירה של ארבעת העמודים:
        1. **Strategy:** הפילוסופיה ויסודות.
        2. **Workflow:** ה-Playbook היומיומי.
        3. **Governance:** שמירה על שליטה ואיכות.
        4. **Team Capability:** מנגנון לשיפור מתמיד.
    * הדגשה שהסדנה תתמקד ביישום המעשי של ה-Workflow (ה-Playbook).
* **<span style="text-decoration:underline;">שינוי תפיסתי: The New Mental Model</span>**
    * **Factor I: Developer as Orchestrator, AI as Intern:**
        5. ה-AI הוא מתמחה מוכשר: מהיר, בעל ידע עצום, אך חסר ניסיון, טעם ארכיטקטוני והקשר עסקי.
        6. תפקיד המפתח משתדרג: מ"כותב קוד" ל"מתזמר פתרונות".
    * **Factor VI: The Great Filter:**
        7. המפתח הוא שומר הסף של האיכות. אחריות אינה ניתנת להעברה (Accountability is not transferable).
        8. ה-git merge הסופי הוא תמיד באחריות המפתח.


## <p dir="rtl">
ה-Factor I לעומק: מיומנות ה-'Orchestrator' (תזמור)</p>




* **הגדרה ומטרה**
    * **הגדרה:** "לתזמר" (Orchestrate) היא מיומנות רכה (Soft Skill) אסטרטגית. היא מתארת את היכולת להנחות, לנהל ולשלב כלים וסוכני AI כדי להגיע לתוצאה איכותית, במקום לבצע את כל המשימות בעצמך. בדומה למנצח בתזמורת, ה-"Orchestrator" לא מנגן בכל הכלים, אך הוא אחראי על ההרמוניה, הקצב והתוצר הסופי.
    * **מטרה:** המטרת שלנו היא לפרק את המושג המופשט "תזמור" לחמש מיומנויות משנה מעשיות שכל מפתח יכול ללמוד, לתרגל ולשפר באופן מודע.
* **נושא הלימוד: חמשת עמודי התווך של ה-Orchestrator \
**כדי להפוך ל-"Orchestrator" יעיל, עלינו לפתח חמש יכולות מרכזיות:
    * **חשיבה אסטרטגית ותכנון (Strategic Thinking): \
**היכולת לראות את התמונה הגדולה לפני שכותבים את הפרומפט הראשון. זה בא לידי ביטוי ביצירת **Mission Brief )** Factor III) – הגדרת המטרה העסקית, האילוצים ומדדי ההצלחה.
    * **פירוק בעיות (Problem Decomposition): \
**היכולת לקחת משימה מורכבת ולפרק אותה לתתי-משימות קטנות ומוגדרות היטב. זוהי הליבה של תהליך ה-**Triage)** Factor IV), שבו אנו מחליטים מה מתאים לעבודת "זוג" אינטראקטיבית [SYNC] ומה ניתן להאציל לסוכן אוטונומי [ASYNC].
    * **האצלה אפקטיבית (Effective Delegation): \
**זוהי האומנות של Prompt Engineering מודרני. במקום לכתוב פקודות, אנחנו מנסחים הנחיות ברורות, מספקים הקשר מלא (Context Scaffolding) ומגדירים ציפיות מדויקות, כאילו היינו מאצילים משימה למתמחה מוכשר.
    * **שיפוט ביקורתי (Critical Judgment): \
**הליבה של עקרון **The Great Filter)** Factor VI). זוהי היכולת האנושית להעריך את התוצר של ה-AI לא רק לפי נכונותו, אלא גם לפי איכותו, פשטותו, התאמתו לארכיטקטורה, וה"טעם" הצוותי.
    * **חניכה איטרטיבית (Iterative Mentorship): \
**היכולת להתייחס ל-AI כאל מתמחה שניתן ללמד. זה כולל מתן משוב מתקן, אספקת דוגמאות קוד איכותיות (Examples) כדי להדגים את הסטנדרט הרצוי, ותיקון הדרגתי של התוצרים במקום לדחות אותם על הסף.
* **תרגיל: מיפוי עצמי של מיומנויות ה-Orchestrator ([נייר עבודה](https://docs.google.com/document/d/17sKxVI1Wfw4bxo2ECwMiO_o4JUed9sUbN1Y-kUiwiN0/edit#heading=h.an8jrgx5pxu5))**
    * **הנחיה:** עבדו באופן אישי במשך 5 דקות, ולאחר מכן שתפו בזוגות.
    * **משימה:** דרגו את עצמכם בכל אחת מחמש מיומנויות המשנה (1 - מרגיש שצריך שיפור משמעותי, 5 - מרגיש חזק מאוד). לאחר מכן, רשמו פעולה אחת קונקרטית שאתם יכולים לעשות בספרינט הקרוב כדי לשפר את המיומנות שקיבלה את הדירוג הנמוך ביותר.

<table>
  <tr>
   <td>
<p dir="rtl">
מיומנות משנה</p>

   </td>
   <td><p dir="rtl">
דירוג עצמי (1-5)</p>

   </td>
   <td><p dir="rtl">
פעולה לשיפור</p>

   </td>
  </tr>
  <tr>
   <td><p dir="rtl">
1. חשיבה אסטרטגית (Mission Brief)</p>

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td><p dir="rtl">
2. פירוק בעיות (Triage)</p>

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td><p dir="rtl">
3. האצלה אפקטיבית (Prompts)</p>

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td><p dir="rtl">
4. שיפוט ביקורתי (The Filter)</p>

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td><p dir="rtl">
5. חניכה איטרטיבית (Feedback)</p>

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
</table>




    * **סבב שיתוף:** כל זוג ישתף תובנה אחת מרכזית מהתרגיל.
* **תובנות**
    * המעבר לתפקיד ה-"Orchestrator" הוא לא שינוי טכני, אלא **פיתוח של מיומנויות רכות** אסטרטגיות.
    * כל אחד מהשלבים ב-Playbook של ה-Agentic SDLC הוא למעשה **זירת אימונים** לאחת או יותר ממיומנויות אלו.
    * המודעות למיומנויות אלו מאפשרת לנו להשתפר בהן באופן מכוון, במקום לקוות שהן "פשוט יקרו".


## <p dir="rtl">
ה-Playbook: שלב 0 - הקמת סביבת העבודה (IDE Setup)</p>




* **Factor X Strategic Tooling:**
    * **הסבר:** לפני שנוכל "לתזמר" את ה-AI, עלינו לוודא שה"קוקפיט" שלנו מכוון ומוכן. שלב זה הוא הבסיס הטכני שמאפשר לכל שאר עקרונות ה-Playbook לעבוד. זהו היישום המעשי של ה-Factor אנחנו לא משתמשים בכלים אקראיים, אלא מתחברים למערכת מרכזית ומנוהלת.
* **Factor II Context Scaffolding:**
    * החיבור ל-team-ai-directives הוא שמאפשר לנו ליישם את ה-Factor בצורה יעילה, ולקבל גישה מיידית לכל הידע של הצוות (Team Context) ישירות בסביבת הפיתוח שלנו.
* **תרגיל 0: חיבור למנוע העבודה המרכזי**
    * **הנחיה:** בואו נכין את סביבת הפיתוח שלנו לעבודה.
    * **משימה:** בצעו את השלבים הבאים ב-Agentic IDE שלכם (Cursor, VSCode with Cline, וכו'):
        * בצעו https://github.com/tikalk/agentic-sdlc-team-ai-directives.git
    * **ודאו את החיבור:**
        * פתחו את חלונית ה-Chat של ה-Coding Agent ב-IDE.
        * הקלידו את הפקודה @Context ולחצו Enter.
    * **תוצר מצופה:**
        * לאחר הקלדת @team, אתם אמורים לראות רשימה של מודולים זמינים (כמו /context_modules/personas/, /context_modules/rules/) המוכיחה שהחיבור לשרת הצליח. כעת ה-IDE שלכם מוכן למשוך הקשר צוותי באופן דינמי.


## <p dir="rtl">
ה-Playbook: שלב 1 - הכנת המשימה (Mission Prep)</p>




* **Factor II: Context Scaffolding**
    * הסבר: Context הוא תלות קריטית, בדיוק כמו ספריית קוד.
    * סוגי Context:
        * **Local Context:** קבצי קוד רלוונטיים (@codebase, @files).
        * **Team Context:** סטנדרטים, ארכיטקטורה, דוגמאות קוד (@team).
        * **External Context:** תיעוד חיצוני, best practices (@web).
* **Factor III: Mission Definition**
    * הסבר: כל משימה מורכבת מתחילה ב-Mission Brief רשמי. זהו המעבר מ-"prompt" ל-"משימה".
    * מבנה ה-Mission Brief:
        * **Goal:** מטרה ברורה במשפט אחד.
        * **Constraints:** אילוצים טכניים ועסקיים.
        * **Success Criteria:** מדדי הצלחה מדידים (איך נדע שסיימנו?).
* **יצירת Mission Brief לדוגמה**
    * מטרה: להראות כיצד להשתמש ב-AI כשותף לחשיבה כדי להפוך רעיון גולמי למשימה מוגדרת היטב.
    * תהליך: המנחה ייקח דוגמה פשוטה (לדוגמה: "הוספת health-check endpoint חדש לשירות"), ויבנה עבורה Mission Brief מלא בזמן אמת, תוך שימוש בפרומפטים דומים לאלו שבתרגיל כדי להגדיר מטרה, אילוצים ומדדי הצלחה.
    * תוצר: המשתתפים יראו Mission Brief שלם וברור שנוצר בתהליך שיתופי עם ה-AI.
* **תרגיל 1: יצירת Mission Brief (נייר עבודה)**
    * **הנחיה:** 
        * התחלקו לזוגות. 
        * בחרו Feature פשוט לפיתוח (לדוגמה: "הוספת endpoint לאימות משתמש עם שם וסיסמה").
        * &lt;המנחה מוודא בחירה נכונה של Feature>
    * **משימה:** השתמשו ב-Coding Agent שלכם כדי לעזור לכם לבנות Mission Brief מלא עבור ה-Feature.
    * **טבלה בנייר העבודה:**

<table>
  <tr>
   <td>
<p dir="rtl">
<strong>חלק ב-Brief</strong></p>

   </td>
   <td><p dir="rtl">
<strong>תוכן</strong></p>

   </td>
  </tr>
  <tr>
   <td><p dir="rtl">
<strong>Goal</strong></p>

   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td><p dir="rtl">
<strong>Constraints</strong></p>

   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td><p dir="rtl">
<strong>Success Criteria</strong></p>

   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td><p dir="rtl">
<strong>Context Packet</strong></p>

   </td>
   <td><p dir="rtl">
רשימת קבצים/מסמכים רלוונטיים</p>

   </td>
  </tr>
</table>


<p dir="rtl">
<strong>ה-Prompt המומלץ לתרגיל: </strong></p>


** \
**


```
I need to create a new Mission Brief in our issue tracker for the objective: "{YOUR_OBJECTIVE}".
- Propose a one-sentence "{Goal}", measurable "{Success Criteria}" and define the key "{Constraints}".
- Using @web, research best practices for this task.
Help me choose the best components from our team's library for the Context Packet.
- Using `@team`, search `/context_modules/personas/` and suggest the most appropriate persona.
- Using `@team`, search `/context_modules/rules/` for relevant style guides and security rules.
- Using `@team`, search `/context_modules/examples/` for a high-quality example related to my objective.
```


   



    * **סבב שיתוף:** כל זוג מציג בקצרה את ה-Goal וה-Success Criteria שהגדיר.
* **תובנות מפגש 1:**
    * עבודה לא מובנית עם AI יוצרת חוב טכני ברמת הצוות.
    * התפקיד שלנו משתנה מ"מבצעים" ל"מתזמרים", והאחריות על האיכות נשארת שלנו.
    * השלב החשוב ביותר הוא הגדרת המשימה (Mission Brief). "זבל נכנס, זבל יוצא" תקף גם לעבודה עם AI.
    * Context הוא לא מידע רקע, אלא תלות קריטית שיש לנהל באופן אקטיבי.

<p dir="rtl">
<strong>סיכום מפגש 1</strong></p>




* **סבב משתתפים:**
    * מה התובנה המרכזית שלקחתם מהמפגש?
    * האם אתם מרגישים שהקונספט של Mission Brief יכול לעזור לכם בעבודה היומיומית?
* **מטלה למפגש הבא:** חשבו על משימה אמיתית מהספרינט הנוכחי שלכם ונסו לנסח עבורה Mission Brief בסיסי.


# <p dir="rtl">
מפגש 2: ה-Playbook בפעולה - תכנון, ביצוע ובדיקות</p>


<p dir="rtl">
במפגש השני נצלול לליבת ה-Playbook. נלמד איך להפוך Mission Brief לתוכנית עבודה מפורטת, נבין מתי לבחור בעבודת "זוג" עם ה-(Async) ומתי להאציל לו משימות (Async), נתרגל בדיקות מבוססות סיכון, ונסיים עם החלק החשוב ביותר: סגירת הלולאה ולכידת הידע לטובת כל הצוות.</p>



## <p dir="rtl">
רענון וחיבור למפגש 1</p>




* סיכום קצר: המפתח כ-Orchestrator, החשיבות של Context ו-Mission Brief.
* הצגת מטרת המפגש: לעבור מהגדרה לביצוע.


## <p dir="rtl">
ה-Playbook: שלב 2 - תכנון וביצוע (The Core Loop)</p>




* **Factor IV: Structured Planning**
    * הסבר: אחרי שיש לנו Brief, השלב הבא הוא לבקש מה-AI להציע תוכנית עבודה מפורטת, שלב אחר שלב.
    * המפתח סוקר, משפר ומאשר את התוכנית.
* **Factor V: Dual Execution Loops**
    * הצגת שני אופני העבודה:
        * **Synchronous Collaboration (Pair Programming):** עבודה אינטראקטיבית וצמודה עם ה-AI בתוך ה-IDE. מיועד למשימות מורכבות, עמומות או ארכיטקטוניות.
        * **Asynchronous Delegation (Automating Toil):** האצלת משימה מוגדרת היטב Autonomous coding agent שמחזיר בסוף PR. מיועד למשימות ברורות הדורשות מאמץ (לדוגמה: מימוש Feature לפי מפרט מפורט, יצירת Client API מקובץ Swagger, או הוספת שכבת תרגומים לאפליקציה).
    * **Triage:** ההחלטה באיזה אופן להשתמש היא מיומנות מפתח של ה-Orchestrator.
* **הדגמה: הפיכת Mission Brief לתוכנית עבודה**
    * מטרה: להדגים כיצד לוקחים את ה-Brief שהוגדר ומשתמשים ב-AI כדי לייצר תכנית פעולה מעשית עם חלוקה ל-SYNC/ASYNC.
    * תהליך: המנחה ייקח את ה-Mission Brief שהוכן בהדגמה הקודמת (של ה-health-check endpoint) ויזין אותו ל-AI. הוא יבקש מה-AI להציע תוכנית עבודה, יסקור אותה, יבצע תיקון קטן (כדי להדגים את עיקרון The Great Filter) ויאשר את החלוקה לשלבים Sync ו-Async.
    * תוצר: המשתתפים יראו תוכנית עבודה מפורטת ומתויגת, מוכנה לביצוע.
* **תרגיל 2: מ-Brief לתוכנית עבודה (נייר עבודה)**
    * **הנחיה:** המשיכו לעבוד בזוגות עם ה-Mission Brief שיצרתם במפגש הקודם.
    * **משימה:** השתמשו ב-Coding Agent כדי לייצר תוכנית עבודה ולתייג כל שלב כ-[SYNC] או [ASYNC].
    * **טבלה בנייר העבודה:**

<table>
  <tr>
   <td>
<p dir="rtl">
<strong>שלב בתכנית</strong></p>

   </td>
   <td><p dir="rtl">
<strong>תיאור</strong></p>

   </td>
   <td><p dir="rtl">
<strong>אופן עבודה (SYNC/ASYNC</strong></p>

   </td>
   <td><p dir="rtl">
<strong>נימוק</strong></p>

   </td>
  </tr>
  <tr>
   <td><p dir="rtl">
<strong>1</strong></p>

   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td><p dir="rtl">
<strong>2</strong></p>

   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
</table>


<p dir="rtl">
<strong>ה-Prompt המומלץ לתרגיל:</strong></p>



```
Based on my Mission Brief in issue {ISSUE-123}:
- Generate a detailed, step-by-step plan.
- Use @codebase to identify all affected files that should be part of the plan.
- For each step, suggest if it is better suited for [SYNC] or [ASYNC] execution and define the expected outcome.
```


 



    * **דיון קבוצתי:** מדוע בחרתם SYNC לשלב X ו-ASYNC לשלב Y? מהם הקריטריונים?


## <p dir="rtl">
ה-Playbook: שלב 3 - אימות ובדיקות (QA & Testing)</p>




* **Factor VIII: AI-Augmented, Risk-Based Testing**
    * הסבר: במקום לבקש "תכתוב לי טסטים", אנחנו מנחים את ה-AI לכתוב טסטים שמכסים סיכון ספציפי שזיהינו.
    * דוגמה: במקום "test the endpoint", נבקש "Write a test that asserts a 401 status when the password is wrong".
* **תרגיל 3: מ-Brief לתוכנית עבודה (נייר עבודה)**
    * **הנחיה: **בהמשך לתוכנית העבודה שיצרתם, זהו סיכון עסקי או אבטחתי אחד מרכזי (לדוגמה: "מה קורה אם משתמש לא מורשה מנסה לגשת ל-endpoint?").
    * **משימה:** כתבו פרומפט שמנחה את ה-Coding Agent שלכם לכתוב טסט ספציפי שמכסה את הסיכון הזה.
    * **[ה-Prompt המומלץ לתרגיל:](?tab=t.ut9aq1wb8f80)**


```
Generate targeted tests for @file:{path/to/your/code.py}.
- The primary goal is to validate against this risk I've identified: {DEVELOPER_IDENTIFIED_RISK}.
- As a secondary goal, ensure all {Success Criteria} from our Mission Brief in issue {ISSUE-123} are met.
- My IDE is configured with our team's standards, so all tests must adhere to the patterns and style guides defined there.

```



* **תובנות מפגש 2:**
    * הפיכת Mission Brief לתוכנית עבודה מפורטת היא השלב שבו אנו מתרגמים אסטרטגיה לטקטיקה.
    * ההחלטה מתי לעבוד ב-SYNC ומתי ב-ASYNC היא מיומנות מפתח של ה-"Orchestrator".
    * בדיקות אפקטיביות עם AI מתמקדות בבדיקת סיכונים עסקיים, לא רק בהשגת כיסוי קוד.
    * השלמנו את ליבת העבודה על המשימה. במפגש הבא נלמד איך להבטיח את איכותה הסופית ולשתף את הידע עם כל הצוות.
* **מטלה למפגש הבא:** חשבו על המשימה שניתחתם. בהתבסס על הסיכון הראשון שזיהיתם, מהו הסיכון השני בחשיבותו שהייתם רוצים לבדוק? נסחו בנקודות את הרעיון לבדיקה שלו.


# <p dir="rtl">
מפגש 3: איכות ושיפור צוותי (Leveling Up)</p>



## <p dir="rtl">
רענון וחיבור למפגש 2</p>




* **סיכום קצר:** במפגש הקודם תרגמנו Mission Brief לתוכנית עבודה מפורטת, למדנו להבחין בין עבודת SYNC ל-ASYNC, ותרגלנו יצירת בדיקות ממוקדות סיכון כדי לוודא את נכונות הפתרון.
* **הצגת מטרת המפגש:** כעת, לאחר שהמשימה "בוצעה" ברמה הטכנית, נלמד איך לסגור אותה נכון, להבטיח איכות, והכי חשוב - איך להפוך את ההצלחה שלנו למנוע צמיחה עבור כל הצוות. זהו השלב שהופך מפתחים טובים לצוותים מעולים.


## <p dir="rtl">
ה-Playbook: שלב 3 - הבטחת איכות (Quality Gates)</p>




* **Factor VII: Adaptive Quality Gates**
    * **הסבר:** האיכות נשמרת לא רק בסוף, אלא לאורך כל הדרך. המתודולוגיה דורשת סוגי בקרות איכות שונים עבור אופני העבודה השונים:
        * **Micro-Reviews:** בדיקות קטנות ומהירות שאנחנו מבצעים בזמן אמת במהלך עבודת **SYNC** אינטראקטיבית. זהו משוב מיידי ששומר על כיוון נכון.
        * **Macro-Reviews:** תהליכי סקירת קוד (Pull Request) מלאים, בדיקות CI/CD אוטומטיות וסקירה אנושית מקיפה הנדרשים עבור כל תוצר של עבודת **ASYNC**.


## <p dir="rtl">
ה-Playbook: שלב 4 - שיפור מתמיד (Leveling Up)</p>




* **Factor XI: Directives as Code**
    * **הסבר:** זהו המנגנון שהופך הצלחה אישית לנכס צוותי. אם כל הידע נשאר בראש של מפתח אחד או בהיסטוריית הצ'אט שלו, הצוות לא באמת למד כלום. הנחיות מוצלחות (prompts), תבניות עבודה ודוגמאות קוד איכותיות הן **קוד לכל דבר** ויש לנהל אותן ב-Git.
    * **הצגת מבנה ה-Repository team-ai-directives:** זהו "בנק הזיכרון" של הצוות, המכיל:
        * **Examples:** דוגמאות קוד מעולות המהוות "Gold Standard".
        * **Personas:** הגדרות אישיות ל-AI (למשל, "מומחה אבטחה").
        * **Rules:** כללים וחוקים שה-AI חייב לציית להם (למשל, "כל קוד Python חייב לכלול docstrings").
* **הדגמה: תרומת נכס חדש לצוות**
    * **מטרה:** להראות את התהליך המלא של סגירת הלולאה – הפיכת ידע אישי שנרכש במהלך משימה לנכס צוותי מנוהל גרסאות.
    * **תהליך:** בהמשך לדוגמת ה-health-check, המנחה יניח שהפיתוח הסתיים וזוהתה פונקציה יעילה או תבנית בדיקה מוצלחת. הוא ישתמש ב-AI כדי לנתח את ההצלחה ולהכין טיוטה של Pull Request שמוסיף את הנכס החדש (כ-Exemplar) למאגר ה-team-ai-directives.
    * **תוצר:** המשתתפים יראו טיוטת PR מלאה, כולל קובץ ותיאור, המדגימה איך לתרום ידע חזרה לצוות.
* **תרגיל 3: סגירת הלולאה - Leveling Up (נייר עבודה)**
    * **הנחיה:** דמיינו שסיימתם בהצלחה את המשימה. עכשיו המטרה היא לתרום את הידע חזרה לצוות.
    * **משימה:** השתמשו ב-Coding Agent כדי לנתח את תהליך העבודה, לזהות נכס ידע חדש, ולהכין טיוטה של PR שמוסיף אותו ל-Repository הצוותי.

<p dir="rtl">
<strong>ה-Prompt המומלץ לתרגיל:</strong></p>



```


The work for issue {ISSUE-123} is complete, and this chat history represents a successful workflow. Let's formalize this success for the team.
1. Analyze and Extract: Review our entire interaction and extract the single most valuable new rule or code exemplar that made this workflow effective.
2. Prepare a Pull Request: Draft a complete Pull Request to our team-ai-directives repository that adds this new asset. The draft must include:
	A clear PR Title.
	A PR Description explaining what the new asset is and why it's valuable to the team,
referencing {ISSUE-123} for context.
	The complete File Content for the new rule or exemplar, including a title, description, and code examples.
3. Update the Issue Tracker: Independently, draft a concise comment to post directly to {ISSUE-123}. This comment should be a Trace Summary of our work on the original task, including:
	The problem that was solved.
	The key decisions made.
	The final accepted code solution.
Present the full Pull Request draft and the Issue Tracker Comment in separate, clearly marked code blocks for my final review before you proceed.

```



    * **סבב שיתוף:** איזה "נכס" חדש זיהיתם? (דוגמת קוד, כלל אבטחה, וכו').
* **תובנות מפגש 3:**
    * **איכות אינה תהליך 'מידה אחת לכולם'.** עבודה אינטראקטיבית (**SYNC**) דורשת בדיקות מהירות ומתמשכות (Micro-Reviews), בעוד שעבודה אוטונומית (**ASYNC**) מחייבת תהליכים פורמליים ומקיפים (Macro-Reviews), כמו PR ובדיקות CI.
    * **הערך האמיתי לצוות נוצר כשאנחנו הופכים ידע אישי לנכס צוותי מנוהל גרסאות (Directives as Code).** אם הידע לא נשמר ושותף באופן מובנה, הצוות לא באמת למד כלום וההצלחה נשארת נקודתית.
    * **תהליך הפיתוח לא מסתיים ב-git merge.** שלב ה-Leveling Up, שבו אנו תורמים את הידע חזרה למאגר הצוותי, הוא מה שמבטיח שהארגון כולו הופך לחכם יותר ולא רק המפתח הבודד.


## <p dir="rtl">
סיכום הסדרה</p>




* **סיכום התהליך שעברנו:**
    * הבנו את הבעיה האסטרטגית ואת שינוי התפיסה הנדרש.
    * למדנו את 4 השלבים המעשיים של ה-Playbook:
        1. **Mission Prep:** הגדרת המשימה וה-Context.
        2. **Plan & Triage:** יצירת תוכנית והחלטה על אופן ביצוע.
        3. **Execute & QA:** ביצוע ואימות איכות מבוסס סיכון.
        4. **Leveling Up:** סגירת לולאת המשוב ותרומה לצוות.
* **צעדים ראשונים (Starting the Journey):**
    * **Assess:** איפה אתם היום? (Vibe Coders?)
    * **Pilot:** התחילו עם Mission Briefs בספרינט הקרוב.
    * **Create:** צרו את ה-Directive as Code הראשון שלכם - אפילו קובץ Markdown עם 5 הפרומפטים הכי טובים של הצוות.
* **סבב משתתפים:**
    * מה הכלי או הטכניקה שלמדתם בסדנה שאתם מתכוונים ליישם כבר מחר?
    * מה עדיין מרגיש לכם מאתגר בתהליך?