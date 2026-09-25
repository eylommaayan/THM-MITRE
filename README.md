# THM---MITRE
ארגון **MITRE** הוא מלכ"ר (ארגון ללא כוונת רווח) המבצע מחקר ופיתוח בתחומים שונים (סייבר, בינה מלאכותית, בריאות ועוד) תחת החזון "לפתור בעיות למען עולם בטוח יותר". בחדר זה נלמדות המסגרות המובילות של MITRE להבנת התנהגות תוקפים ושיפור ההגנה: ATT&amp;CK, CAR, D3FEND ו-Engage.
<img width="1794" height="508" alt="image" src="https://github.com/user-attachments/assets/9747d9a3-0a43-4c85-9182-41c36897136c" />


# TryHackMe – MITRE Room Walkthrough & Notes

פתרון מלא, תרגום והסברים לחדר **MITRE** בפלטפורמת TryHackMe.

---

## תוכן עניינים
1. [Task 1: Introduction](#task-1-introduction)
2. [Task 2: The MITRE ATT&CK® Framework](#task-2-the-mitre-attck-framework)
3. [Task 3: ATT&CK in Operation](#task-3-attck-in-operation)
4. [Task 4: Practical Application](#task-4-practical-application)
5. [Task 5: Cyber Analytics Repository (CAR)](#task-5-cyber-analytics-repository-car)
6. [Task 6: MITRE D3FEND Framework](#task-6-mitre-d3fend-framework)
7. [Task 7: Beyond ATT&CK](#task-7-beyond-attck)
8. [Task 8: Conclusion](#task-8-conclusion)

---

## Task 1: Introduction

* **I understand the learning objectives and am ready to learn about MITRE!**  
  > *תשובה:* **Completed** (לחיצה על הכפתור)

---

## Task 2: The MITRE ATT&CK® Framework

### תמצית תיאורטית
מאגר **MITRE ATT&CK®** מסווג ומתעד טקטיקות, טכניקות ופרוצדורות (**TTPs**) של קבוצות תקיפה בעולם האמיתי:
* **Tactic (טקטיקה):** המטרה/היעד של התוקף ("הלמה" / The "Why").
* **Technique (טכניקה):** האופן שבו התוקף משיג את מטרתו ("האיך" / The "How").
* **Procedure (פרוצדורה):** היישום המעשי הספציפי שבו הוצאה הטכניקה לפועל.

### תשובות
* **What Tactic does the Phishing technique belong to in the ATT&CK Matrix?**  
  > `Initial Access`
* **Which ID is associated with the Create Account technique?**  
  > `T1136`

---

## Task 3: ATT&CK in Operation

### תמצית תיאורטית
ATT&CK מספק שפה אחידה ומזהים ייחודיים לתיאור תקיפות, ומסייע לגשר בין מודיעין איומים (CTI) לפעולות הגנה בפועל (SOC, Detection Engineering ו-Incident Response). במשימה זו מנתחים את קבוצת הריגול הסינית **Mustang Panda (G0129)**.

### תשובות
* **In which country is Mustang Panda based?**  
  > `China`
* **Which ATT&CK technique ID maps to Mustang Panda’s Reconnaissance tactics?**  
  > `T1598`
* **Which software is Mustang Panda known to use for Access Token Manipulation?**  
  > `Cobalt Strike`

---

## Task 4: Practical Application

### תמצית תיאורטית
**תרחיש:** אנליסט אבטחה בעולם התעופה (Aviation Sector) שארגונו עובר לענן, ונדרש לאסוף מודיעין על קבוצות APT רלוונטיות, לזהות טכניקות תקיפה ופערים בהגנה.

### תשובות
* **Which APT group has targeted the aviation sector and has been active since at least 2013?**  
  > `APT33`
* **Which ATT&CK sub-technique used by this group is a key area of concern for companies using Office 365?**  
  > `Cloud Accounts` *(T1078.004)*
* **According to ATT&CK, what tool is linked to the APT group and the sub-technique you identified?**  
  > `Ruler`
* **Which mitigation strategy advises removing inactive or unused accounts to reduce exposure to this sub-technique?**  
  > `User Account Management` *(M1018)*
* **What Detection Strategy ID would you implement to detect abused or compromised cloud accounts?**  
  > `DET0546`

---

## Task 5: Cyber Analytics Repository (CAR)

### תמצית תיאורטית
מאגר **CAR** מציע אנליטיקות זיהוי מוכנות המבוססות על ATT&CK. כל אנליטיקה כוללת פסאודו-קוד, שאילתות מעשיות למערכות SIEM נפוצות (כגון Splunk ו-LogPoint) ולעיתים בדיקות יחידה (Unit Tests) לבדיקת תקינות הזיהוי.

### תשובות
* **Which ATT&CK Tactic is associated with CAR-2019-07-001?**  
  > `Defense Evasion`
* **What is the Analytic Type for Access Permission Modification?**  
  > `Situational Awareness`

---

## Task 6: MITRE D3FEND Framework

### תמצית תיאורטית
בניגוד ל-ATT&CK שמתמקד באופן שבו תקיפות מתרחשות, מסגרת **D3FEND** מתמקדת בטכניקות הגנה נגדיות (Detection, Denial, Disruption) ומקשרת בין מנגנוני הגנה לארטיפקטים דיגיטליים (Digital Artifacts).

### תשובות
* **Which sub-technique of User Behavior Analysis would you use to analyze the geolocation data of user logon attempts?**  
  > `User Geolocation Logon Pattern Analysis` *(D3-UGLPA)*
* **Which digital artifact does this sub-technique rely on analyzing?**  
  > `Network Traffic`

---

## Task 7: Beyond ATT&CK

### תמצית תיאורטית
פרויקטים ומסגרות מתקדמות נוספות מבית MITRE:
* **Adversary Emulation Library:** מדריכי צעד-אחר-צעד לחיקוי תקיפות של קבוצות איום מוכרות.
* **Caldera:** כלי הדמיית תקיפות אוטומטי (Emulation tool) המבוסס על ATT&CK.
* **AADAPT:** מסגרת ייעודית לאיומים על רשתות תשלום ונכסים דיגיטליים (בלוקצ'יין, חוזים חכמים, ארנקים דיגיטליים).
* **ATLAS:** מאגר איומים ומטריצה המיועדים למערכות בינה מלאכותית (AI) ולמידת מכונה (ML).

### תשובות
* **What technique ID is associated with Scrape Blockchain Data in the AADAPT framework?**  
  > `ADT3025`
* **Which tactic does LLM Prompt Obfuscation belong to in the ATLAS framework?**  
  > `Defense Evasion`

---

## Task 8: Conclusion

### תמצית
סיכום החדר והבנת חשיבותם של מאגרי המידע והמודלים של MITRE בחיזוק מערכי האבטחה הגלובליים.

### תשובות
* **No answer needed**  
  > *תשובה:* **Completed** (לחיצה על הכפתור לסיום החדר)
