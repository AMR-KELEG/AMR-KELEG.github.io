---
layout: post
inline: true
---

<div dir="rtl">
<h1 align="right"> ازاي اشتغل في مجال ال natural language processing في مصر </h1>

<h2 align="right"> مقدمة </h2>
<p align="right"> الأفكار المكتوبة هنا من واقع خبرتى البسيطة كشخص متخرج سنة 2017.
أولاً مجال ال natural language processing اختصاراً nlp بيدور حول فكرة اننا نحلل بيانات في هيئة كلام مكتوب. زمان كانت البيانات دي كتب أو مقالات صحفية. مؤخراً, بدأنا نهتم كمان ببيانات موجودة online زي tweets, websites,...
ده ساعد في أن الdata بقت أكبر لكن بردو تحليل حاجات قصيرة زي tweets (أقل من 280 حرف) مختلف عن مقال صحفي طويل.
المجال حالياً بيستخدم machine learning algorithms و deep learning models لكن ده مش معناه أن الأفكار ماقبل ال deep learning مش مستخدمة. في مجموعة من الtasks الي ظهرت وفي معظم الأحيان الشركات بتختار task معين تهتم به.</p>

<h2 align="right"> أشهر التطبيقات </h2>
<ul align="right">
<li align="right">
Text classification: الفكرة هنا أن يبقي معانا text معين في هيئة خبر أو tweet ونبقي عايزين نصنف ال text ده بشكل ما. أنواع التصنيفات بقي ممكن تبقي مختلفة فمثلاً هل الtext بيتكلم عن حاجة رياضية ولا لا أو هل الtext فيه offensive speech سواءاً كانت شتائم أو عنصرية ضد شخص معين أو مجموعة من الأشخاص.
</li>

<li align="right">
Machine Translation: والهدف هنا هو ترجمة بين لغات مختلفة (Google translate يعني)

</li>

<li align="right">
Text summarization: وده هدفه اختصار text طويل للنقط الأساسية فيه. في منه نوعين , الأول extractive بمعني أنه بيختار جمل معينة من الtext الأصلي وفيه نوع abstractive وده بيحاول يفهم المعني ويعمل generation لtext جديد يحمل المعني المختصر.

</li>

<li align="right">
News aggregation/clustering: وده هدفه تجميع الأخبار وأنه يقدر يجمع الأخبار المتعلقة ببعض في مجاميع (clusters)
</li>

<li align="right">
وفي حاجات تانية أكيد ....
</li>

</ul>

<h2 align="right"> ابدأ ازاي </h2>
<p align="right">أنا شخصياً بدأت اركز علي المجال بعد ما اتخرجت. حالياً في شوية resources حلوة سواء courses أو python packages.

ك courses ممكن تبدأوا بواحد من دول (أنا مذاكرتش كل الcourses فمش عارف مدي سهولتهم/صعوبتهم لكن لما شوفت جزء منهم كانوا كويسين).</p>
<ul align="right">
<li align="right"> <a href="https://www.coursera.org/specializations/natural-language-processing">Coursera's NLP specialization</a> وممكن تقدموا علي financial aid لكل course لوحده</li>
<li align="right"> <a href="https://www.udacity.com/course/natural-language-processing-nanodegree--nd892"> Udacity's NLP nanodegree </a>, وممكن تقدموا علي منحة ليها من <a href="http://techleaders.eg/learning-tracks/"> NTL</a>  </li>
<li align="right"> <a href="https://www.youtube.com/watch?v=cce8ntxP_XI&list=PLtmWHNX-gukKocXQOkQjuVxglSDYWsSh9">fastAI</a> وده course مركز علي python package معينة اسمها fastAI. أنا شخصياً محبتش الpackage اوي لكن هي هدفها انها تبقي سهلة الاستخدام من غير الدخول في تفاصيل الdeep learning فممكن تلاقوها حلوة خاصة فالأول</li>
</ul>

<h2 align="right"> ايه الحاجات الي محتاج ابقي عارفها علشان اقدر اشتغل بعد التخرج </h2>
<p align="right">أنا شايف محتاجين تبقوا اشتغلتوا علي مشاريع حتي لو صغيرة. المشروع ممكن يبقي حاجة زي اننا عملنا text classification. علشان يبقي الموضوع شكله حلو فيفضل المشروع يبقي موجود علي github وتكتبه عنه جملتين فالcv. الهدف من المشروع انكم تعدوا علي مراحل زي اننا بنشوف مصدر للdata وبعدين بنشوف اذا كانت annotated ولا لا وبعدين نشوف ازاي هنحول الtext الي أرقام ندخلها للmodel الي هنختاره وأخيراً ازاي بنعمل تقييم لمدي كفاءة الmodel.

اعتقد لازم تبقوا فاهمين الجزء ده علشان تبقوا علي المستوي المطلوب من الشركات. طبعاً مع المشاريع هتبقوا بتتعرفوا علي python بشكل أحسن وبتتقنوه + بتتعرفوا علي packages مفيدة في الpython.

الpackages الي أنا شخصياً بستخدمها (بتعرف عليها مع الوقت مش لازم تذاكروها الأول):</p>
<ul align="right">
<li align="right">
pandas: لطيفة جداً جداً في تغيير شكل الdata والdata cleaning.
أنا بستخدمها كأنها database تقريباً لأنها بتعمل operations كتير مفيدة.
</li>
<li align="right">
scikit-learn: ودي فيها implementation لمعظم الclassical machine learning algorithms.
هي حلوة علشان مش بنحتاج نعمل implementation لل models من الأول لكن متتعملوش معاها انها black box. يعني لو في حاجة مش واضحة ادخلوا جوة الcode أو دوروا علي tutorials بتشرح ازاي الmodel المعين بيشتغل.
فيها كمان شوية components لطيفة لل nlp زي CountVectorizers, ....
</li>

<li align="right">
pytorch: أنا بفضلها عن keras و tensorflow. لسه معملتش models كتير بايدي لكن لو عايز اعمل ده بستخدمها. هو مشهورة في انكم تعملوا deep learning models فلو الشركة بتستخدم deep learning models هتبقي متوقعة من المهندسين بتوعها يبقوا عارفين pytorch أو keras.
</li>

</ul>

<h2 align="right"> اكمل ازاي بعد ماعرفت الأساسيات </h2>
<p align="right">لو عايزين تعملوا مشاريع أكتر فممكن تخشوا مسابقات online:</p>
<ul align="right">
<li align="right"><a href="https://zindi.africa/competitions?data_type[]=NLP">Zindi</a> وده موقع زي kaggle ومهتم بافريقيا أكتر فلطيف والمنافسة فيه أقل</li>
<li align="right"><a href="http://alt.qcri.org/semeval2020/index.php?id=tasks">SemEval</a> ودي زي kaggle بس هدفها بحثي أكتر بمعني انهم كل سنة بيختاروا tasks جديدة وبتتنافسوا مع فرق بحثية من جامعات مختلفة وفي أخر المسابقة بيبقي عندكم فرصة تنشروا paper صغيرة تشرحوا فيها الsystem بتاعكم</li>
</ul>

<p align="right">لو عايزين تذاكروا أكتر فممكن تشوفوا حاجة من دول:</p>
<ul align="right">
<li align="right"><a href="https://pytorch.org/tutorials/">Pytorch's examples</a> ودي فيها tutorials لطيفة لمختلف المجالات</li>
<li align="right"><a href="https://github.com/eg-nlp-community/nlp-reading-group">Egyptian NLP community's</a> reading group وده جروب من مصريين شغالين في المجال بتاع الnlp وبيقرأوا paper كل أسبوع مع بعض</li>
<li align="right">تتعمقوا أكتر في حاجة زي Regex أو في الdeep learning architectures الجديدة زي الtransformers</li>
<li align="right">تتابعوا blogs بتاعت ناس مشهورة فالمجال زي <a href="https://ruder.io/
">Sebastian Ruder</a>, <a href="https://dair.ai/newsletter/
">Dair.AI </a>, <a href="https://allenai.org/podcasts
">AllenAI </a>, <a href="https://nlp.stanford.edu/blog/
"> Stanford </a>.</li>
</ul>

</div>
