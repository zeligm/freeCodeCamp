---
title: Using the Find Command
localeTitle: باستخدام الأمر بحث
---
# باستخدام الأمر بحث

يعتبر الأمر "البحث عن Linux" أداة قوية تساعدك في تحديد موقع الملفات والدلائل على الخادم الخاص بك. مع القليل من التدريب ، يمكنك بسهولة تتبع الأشياء استنادًا إلى الاسم ، أو النوع ، أو الحجم ، أو التاريخ (عند إنشائها أو تحديثها الأخير).

فكر في العثور على مساعد حريص عليك:

أنت: "أنا أبحث عن شيء ما على الخادم الخاص بي."

البحث: "يمكنني المساعدة! ما الذي يمكنك إخباري به؟"

أنت: "لقد كان ملفًا أكبر من 2 غيغابايت ، في مكان ما أسفل دليل منزلي ، وتم تحديثه في آخر 48 ساعة."

البحث: "تادا!"

البحث هو برنامج ، لذلك عليك حقا أن تقول أنه `find ~ -type f -size +2G` .

فيما يلي بعض أوامر العينة باستخدام find:

*   `find ~ -type d # Show me all the subdirectories inside my home directory`
*   `find / -type f -name 'todo.txt' # Show me files named 'todo.txt' anywhere under the root directory (ie anywhere)`

تشير المعلمة الأولى دائمًا إلى الدليل الذي سنظهر به. في الأمثلة المذكورة أعلاه ، هذه ~ (الدليل الرئيسي للمستخدم الحالي) و / (الدليل الجذري لنظام الملفات).

المعلمات الأخرى اختيارية ويمكن دمجها بأي طريقة تجدها مفيدة:

*   تتيح معلمة النوع تقييد البحث عن الملفات فقط (f) أو الدلائل فقط (d) أو الارتباطات الرمزية (l). إذا حذفت معلمة النوع ، فستبحث عن جميع هذه الأنواع.
*   تتيح لك المعلمة name تحديد ما تريد البحث عنه بالاسم ، إما باستخدام سلسلة حرفية ('filename.txt') أو باستخدام أحرف البدل ('file؟. \*').

سيظهر لك `man find` ما العديد من المعلمات ، ويستحق المراجعة. يمكن العثور على تحديد موقع الملفات بالاسم والمستخدم وتاريخ الإنشاء والحجم وأكثر من ذلك بكثير. في المرة القادمة التي تبحث فيها عن شيء ما ، يمكنك العثور عليه!