
# Git

### في البداية سنقوم بشرح أهم الأوامر في الـ git:

> git init

قبل كتابة الأمر git init لا يقوم الـ git بمراقبة المشروع وبعد كتابة الأمر سيقوم الـ git بتسجيل أي إضافة على الملفات أو التعديل عليها.

> echo 'mssg' > file.txt

يقوم بإنشاء ملف وكتابة رسالة بداخله بنفس الأمر.

> git status

يقوم بإظهار حالة المشروع.

> git nano file.txt 

سيقوم بفتح الملف file، والسماح بالكتابة فيه.

> touch file.txt

يقوم بإنشاء ملف، وفي المثال أعلاه سيقوم بإنشاء ملف اسمه file من نوع script.

> git add file.txt

يقوم بمراقبة الملف file من قبل الـ git تجهيزًا لإضافته إلى قاعدة البيانات.

> git commit -m "mssg"

وهنا, يقوم بحفظ الملفات المضافة من قبل الـ git إلى قاعدة البيانات.

> git restore file.txt

يقوم بحفظ التغييرات التي تم اجراؤها دون إضافتها لقاعدة البيانات.

> git diff

يقوم بعرض الفروقات بين الملفات.

> git commit --amend -m "mssg"

يقوم بالتعديل على رسالة آخر commit أو آخر حزمة عمليات مضافة لقاعدة البيانات.

> git log

يقوم بعرض تاريخ المشروع.

> git log --oneline

يقوم بعرض تاريخ المشروع مختصرًا في سطر واحد.

****
### الـ branches أو فروع الـ git:

والآن سنتعرف على مفهوم الـ branch:

عندما نرغب بإضافة تغييرات أو مميزات جديدة للمشروع، والتي تسمح لي بإضافتها هذه التغييرات في النسخة الفرعية أولًا لاختبارها قبل إضافتها للمشروع الأساسي.

#### إنشاء الـbranch:

> git branch **branchName**

#### الانتقال إلى الـ branch:

> git checkout **branchName**

كما يمكننا إنشاء branch جديدة والانتقال إليها في نفس السطر كالتالي:

>git checkout -b **branchName**
#### عرض كل الـ branches في المشروع:

> git branch

#### حذف الـ branch:

عند طباعتنا لهذا الأمر يجب أن يكون المؤشر أو مكان تواجدنا في مكان غير المجلد المُراد حذفه، وصيغة الأمر كالتالي:

> git branch -d **branchName**


***
### الدمج في الـ git:

والآن سنتعرف على  كيفية دمج التغييرات أو الـ features الفرعية التي قمنا بإجرائها واختبارها، ومن ثم إضافتها إلى ملف العمل الأساسي.
ولنقوم بالدمج في الـ git، تنقسم طرق الدمج إلى نوعين:

* fast forward merge.
* three way merge.

##### طريقة Fast Forward Merge:

وهي الطريقة السريعة والمباشرة للدمج، ويمكن تطبيقها عندما يكون هناك طريق خطي مُباشر بين ملف العمل الأساسي والفرعي، فيمكننا تحريك المؤشر من مجلد العمل الأساسي إلى الفرعي، دون الحاجة إلى عملية دمج إضافية.
 
##### طريقة Three Way Merge:

وعلى عكس الـ fast forward merge، لا تتم عملية الدمج هنا بشكل خطي،
***

### مفهوم الـ Rebase:

في الـ git، تنقسم طرق ربط الملفات إلى: الـ merge أو الدمج، والـ rebase.
في الـ rebase يقوم الأمر على عملية إعادة كتابة الـ commits السابقة من أفرع مختلفة لتجميعها في انسخة النهائية من الـ commit.

#### الأوامر الأساسية في الـ rebase:

لنفترض أن لدينا مجلد العمل الأساسي ولنقم بتسميته على سبيل المثال "Master"، ومجلد العمل الفرعي ولنقم بتسميته " Feature"،
وقد قمنا مسبقًا بإضافة تعديلات مختلفة على كلًا منهما وإضافتها لقاعدة البيانات،
والآن سنقوم بعمل rebase: 
سنقوم بكتابة الأوامر بشكلين مختلفين نظرًا لموقعنا في المجلد العمل، في الكود الأول لنفترض بأننا  في الفرع أو الـ Feature وسنقوم بعمل rebase له مع مجلد العمل الأساسي أو الـ Master:

> git rebase **Master**

وفي الأمر التالي، سنقوم باختصار العملية بدل الذهاب إلى الـ Feature للقيام بعملية الـ rebase، يمكننا كتابة الأمر كالتالي:

> git rebase **Master** **Feature**

#### التراجع عن الـ rebase:

في حالة وجود conflict أو تعارض في عملية الـ rebase يمكننا التراجع عن العملية بالأمر التالي:

> git rebase --abort


#### خصائص إضافية:

وفي حال رغبنا بحل الـ conflict أو التعارض بين النسختين دون التراجع عن عملية الـ rebase، فيقدم لنا الـ git طريقتين:
* Skip
* Continue

**طريقة skip:**

هنا سنتجاهل أحد النسختين ونقوم باعتماد الأخرى.

> git rebase --skip

**طريقة continue:**

هنا، سندمج النسختين مع بعضهما البعض.


