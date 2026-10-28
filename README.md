# Smart Diet

**A project concept for photo-assisted calorie tracking with Jordanian and Arabic cuisine.**

![Smart Diet presentation cover](assets/cover.jpg)

Smart Diet explores how a mobile-friendly application could recognize local dishes from meal photos and help users keep a daily food and calorie log. The presentation describes user profiles, food recognition, calorie tracking, daily reports, and suggestions when a user's stated daily target is exceeded.

> **Project status:** The provided Drive folder contains a 14-page project presentation only. It does not include application source code, a trained model, a food dataset, or a nutrition database. This repository preserves and documents the available project material; it does not claim that the proposed app or recognition model is currently runnable or validated.

## Project flow described in the presentation

1. A user enters profile details such as age, height, weight, gender, and activity level.
2. The user photographs a meal.
3. A proposed image-recognition model identifies the dish.
4. The app looks up food information and records the meal in a daily log.
5. A dashboard summarizes intake and presents the project's proposed recommendations.

The presentation highlights dishes such as mansaf, shawarma, maqluba, kabsa, molokhia, and kunafa, alongside everyday foods and salads.

## Technologies mentioned

The presentation names **Ultralytics YOLO**, **SQLite**, and **Streamlit** as the proposed stack. The source code and model weights were not included in the shared folder, so their implementation and performance cannot be verified from the available files.

## Project previews

| Application flow | Interface concept |
| --- | --- |
| ![Application flow slide](assets/app-flow.jpg) | ![Interface concept slide](assets/app-interface-concept.jpg) |

## Repository contents

- [`docs/Smart_Diet_Project_Presentation.pdf`](docs/Smart_Diet_Project_Presentation.pdf) — the original 14-page presentation shared on Google Drive.
- `assets/` — selected, reduced-size slide previews for this README.

## Credits

Names listed in the presentation: **Omar Salem**, **Mohammed Abufurha**, **Hamzeh Haloub**, and **Dr. Ahmad Al-Smadi**.

## Notes before real-world use

Calorie estimates depend on accurate dish recognition, portion size, and validated nutrition data. The equations and recommendations shown in the presentation should be reviewed by a qualified nutrition professional before implementation. Smart Diet is an educational project concept, not medical or nutrition advice.

---

## ملخص بالعربية

**Smart Diet** فكرة تطبيق لمساعدة المستخدم على تتبّع الطعام والسعرات في المأكولات الأردنية والعربية باستخدام صور الوجبات. يشرح العرض تصورًا للتطبيق، ويذكر YOLO وSQLite وStreamlit ضمن التقنيات المقترحة.

المجلد المشارك يحتوي على **عرض تقديمي فقط**؛ لا يحتوي كود التطبيق أو أوزان نموذج مدرّب أو قاعدة بيانات غذائية. لذلك هذا المستودع يوثّق المواد المتاحة ولا يدّعي أن التطبيق جاهز للتشغيل. كما يجب مراجعة حسابات السعرات والتوصيات مع مختص تغذية قبل استخدامها فعليًا.
