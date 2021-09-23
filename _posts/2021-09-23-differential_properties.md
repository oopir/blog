---
title: תכונות הנגזרת - חלק ראשון
---


<h1 style="text-align: center">תכונות הנגזרת - חלק ראשון</h1>


הדבר הטבעי לעשות אחרי שהגדרנו את הנגזרת הוא להראות חוקי גזירה כלליים:
מה עושים עם סכום, הפרש, כפל, מנה והרכבה של פונקציות. כשהייתי בשלב
הזה ב"אינפי 1"
(אותו למדתי מהספרים של הפתוחה), כל הוכחה נראית קצת יותר מסובכת מהשניה,
כשהשיא הגיע בהרכבת פונקציות (כלל השרשרת) ובמשפט הפונקציה ההפוכה. 


כאן נעבוד בסדר שונה -- אתחיל בהוכחה של כלל השרשרת, ובעזרתו נוכיח
את השאר.


@@@@@ אם אני רוצה להראות <strong>סכום פונקציות</strong> בתור דגמה <strong>לפני</strong>
כלל השרשרת - חייבים לפחות לנסח את כלל השרשרת לפני כן. @@@@@
&nbsp;  

&nbsp;  
כדי להראות את התועלת של זה, נדבר לרגע על סכום של פונקציות $$f,g:\mathbb{R}^{n}\rightarrow\mathbb{R}^{m}$$.
בתור התחלה נביע את $$f+g$$ בתור הרכבת פונקציות:


אזכיר שכאשר טווח הפונקציה הוא $$R^{m}$$ נוח לחשוב על הפונקציה בתור
סט של רכיבים:

$$
f=(f_{1},...,f_{m})\,,\,g=(g_{1},...,g_{m})\,,\,
$$



$$
f+g=\left((f+g)_{1},...,(f+g)_{m}\right)=\left(f_{1}+g_{1},...,f_{m}+g_{m}\right)
$$

 
&nbsp;  



נגדיר פונקציות עזר. הראשונה תהיה    $$p:\mathbb{R}^{2}\rightarrow\mathbb{R}\,\,,\,\,p(x)=x_{1}+x_{2}$$.


האחרות כבר יהוו הרכבה בעצמן:    $$q_{i}:\mathbb{R}^{n}\rightarrow\mathbb{R}^{2}\,\,,\,\,q_{i}(x)=(f_{i}(x),g_{i}(x))$$


כאן לא נגדיר $$q_{i}=(q_{i_{1}},q_{i_{2}})$$ כמו שעשינו עם $$f,g$$,
כי ב-$$q_{i}$$ כבר יש לכל רכיב שם משלו.


קחו רגע להשתכנע שמתקיים:

$$
(f+g)(x)=\left(f_{1}+g_{1},...,f_{m}+g_{m}\right)=(p(q_{1}(x)),...,p(q_{m}(x))
$$


&nbsp;  

&nbsp;  
סיימנו להגדיר את ההרכבה, ועכשיו נעבור למציאת הדיפרנציאל. לפי הפוסט
הקודם מתקיים:

$$
D(f+g)(x)\,=\,
\begin{bmatrix}
- & D(f+g)_{1}(x) & -\\

 & \vdots\\

- & D(f+g)_{m}(x) & -\\
\end{bmatrix}
\,=\,
\begin{bmatrix}
- & D(p\circ q_{1})(x) & -\\

 & \vdots\\

- & D(p\circ q_{m})(x) & -\\
\end{bmatrix}

$$

אז מכאן אנחנו צריכים למצוא את הדיפרנציאל של $$D(p\circ q_{i})(x)$$
לכל $$i$$. 
&nbsp;  

&nbsp;  
תחילה נבטא את $$Dq_{i}(x)$$. לפי התחום והטווח זו תהיה מטריצה $$2\times n$$,
ומהגדרת הדיפרנציאל נקבל: 

$$
Dq_{i}(x)\,=\,
\begin{bmatrix}
\frac{\partial f_{i}}{\partial x_{1}}(x) & \cdots & \frac{\partial f_{i}}{\partial x_{n}}(x)\\

\frac{\partial g_{i}}{\partial x_{1}}(x) & \cdots & \frac{\partial g_{i}}{\partial x_{n}}(x)\\
\end{bmatrix}

$$


&nbsp;  



נעבור להביע את $$Dp\left(q_{i}(x)\right)$$. פה נוכל ממש לפרט, כי
$$p$$ מנוסחת במפורשות ולא תלויה ב-$$f$$ או $$g$$. מההגדרה:

$$
Dp\left(q_{i}(x)\right)\,=\,
\begin{bmatrix}
\frac{\partial p}{\partial x_{1}}\left(q_{i}(x)\right) & \frac{\partial p}{\partial x_{2}}\left(q_{i}(x)\right)
\end{bmatrix}

$$

נחשב את הנגזרות החלקיות של $$p$$ (למדנו בתחילת הפוסט הקודם): $$\frac{\partial p}{\partial x_{1}}(a)=1\,,\,\frac{\partial p}{\partial x_{2}}(a)=1$$.
מכך נסיק:

$$
Dp\left(q_{i}(x)\right)\,=\,
\begin{bmatrix}
1 & 1
\end{bmatrix}

$$

(לא מפתיע שהדיפרנציאל שלה זהה בכל נקודה, אבל אגע בזה אחרי שנסיים את
הדוגמה)
&nbsp;  

&nbsp;  
נחבר את הכל: 

$$
D(f+g)_{i}(x)\,=\,D\left(p\circ q_{i}\right)(x)\,=\,Dp\left(q_{i}(x)\right)\cdot Dq_{i}(x)\,=\,
\begin{bmatrix}
1 & 1
\end{bmatrix}
\cdot
\begin{bmatrix}
\frac{\partial f_{i}}{\partial x_{1}}(x) & \cdots & \frac{\partial f_{i}}{\partial x_{n}}(x)\\

\frac{\partial g_{i}}{\partial x_{1}}(x) & \cdots & \frac{\partial g_{i}}{\partial x_{n}}(x)\\
\end{bmatrix}
\,=
$$



$$
=\,
\begin{bmatrix}
\frac{\partial f_{i}}{\partial x_{1}}(x)+\frac{\partial g_{i}}{\partial x_{1}}(x) & \cdots & \frac{\partial f_{i}}{\partial x_{n}}(x)+\frac{\partial g_{i}}{\partial x_{n}}(x)
\end{bmatrix}

$$


&nbsp;  



סה"כ קיבלנו:

$$
\boldsymbol{D(f+g)(x)}\,=\,
\begin{bmatrix}
- & D(f+g)_{1}(x) & -\\

 & \vdots\\

- & D(f+g)_{m}(x) & -\\
\end{bmatrix}
\,=\,
\begin{bmatrix}
\frac{\partial f_{1}}{\partial x_{1}}(x)+\frac{\partial g_{1}}{\partial x_{1}}(x) & \cdots & \frac{\partial f_{1}}{\partial x_{n}}(x)+\frac{\partial g_{1}}{\partial x_{n}}(x)\\

\vdots & \ddots & \vdots\\

\frac{\partial f_{m}}{\partial x_{1}}(x)+\frac{\partial g_{m}}{\partial x_{1}}(x) & \cdots & \frac{\partial f_{m}}{\partial x_{n}}(x)+\frac{\partial g_{m}}{\partial x_{n}}(x)\\
\end{bmatrix}
\,=\,\boldsymbol{Df(x)+Dg(x)}
$$






<br>
<h2>כלל השרשרת</h2>

<strong>הקדמה:</strong> לכתוב חלק שמזכיר ומגדיר כמו שצריך את כלל השרשרת (בפרט,
תדגיש שבביטוי $$Df(g(a))$$, $$g(a)$$ זו נקודה, בעוד שבביטוי
$$Dg(a)$$, $$a$$ זו הנקודה ו-$$g(a)$$ אינו בעל משמעות בפני
עצמו.).


<strong>הקדמה</strong>:<strong> </strong>ליצור פרק שלם על "איך בכלל
הגיעו להבנה שזה כפל מטריצות? מה הייתה האינטואיציה שהביאה אותם לחשוב
על זה? איזה דוגמאות קטנות ופשוטות הובילו לכאן?\textquotedblright


<strong>הקדמה:</strong> לציין שאת ההוכחה לכלל השרשרת לקחתי מהספר $$Multivariable\,Calculus\,(George\,Cain\,\&\,James\,Herod)$$
&nbsp;  

&nbsp;  
בגרסה של פונקציות $$f:\mathbb{R}\rightarrow\mathbb{R}$$, הרעיון
מאחורי ההוכחה די פשוט: ע"י הכפלה וחלוקה בביטוי $$g(a+h)-g(a)$$
נקבל: 

$$
\underset{h\rightarrow0}{lim}\frac{f(g(a+h))-f(g(a))}{h}\,=\,\underset{h\rightarrow0}{lim}\frac{f(g(a+h)-f(g(a))}{g(a+h)-g(a)}\cdot\frac{g(a+h)-g(a)}{h}\,=
$$



$$
=\,\underset{h\rightarrow0}{lim}\frac{f(g(a+h)-f(g(a))}{g(a+h)-g(a)}\cdot\underset{h\rightarrow0}{lim}\frac{g(a+h)-g(a)}{h}\,=\,f'(g(a))\cdot g'(a)
$$

חשוב לציין שזו גרסה "חפיפניקית"
של ההוכחה, כי יש בה פגם מתמטי שאי אפשר להבליג עליו: אנחנו כותבים במכנה
$$g(a+h)-g(a)$$, וביטוי זה בהחלט יכול להתאפס עבור $$h$$ מסוים
( חשבו על $$g(x)=sin(x)$$ , $$h=2\pi$$). אבל גם בהוכחה הנכונה
(שמצאו בה טריק שמנצח את הבעיה) העקרון זהה.
&nbsp;  

&nbsp;  
ננסה להישען על אותו עקרון -- ניעזר באלגברה בשביל להגיע לשני ביטויים
נפרדים, כך שאחד יהיה קשור לדיפרנציאל של $$g$$ ב--$$a$$ והשני
יהיה קשור לדיפרנציאל של $$f$$ ב-$$g(a)$$.
&nbsp;  

&nbsp;  
אבל להבדיל מההוכחה הקודמת, הפעם לא נשתמש בהגדרת הנגזרת כ"קצב
שינוי" (דבר שלא אמור להפתיע אתכם). נוכיח את כלל
השרשרת ע"י הוכחת השוויון: 

$$
\underset{h\rightarrow0}{lim}\frac{f(g(a+h))-f(g(a))-ML(h)}{\left\Vert h\right\Vert }=0
$$

כאשר $$M=Df(g(a))$$, $$L=Dg(a)$$. אגב, זכרו להמשך ש-$$M,L$$
מקיימות את התכונות של העתקות לינאריות.
&nbsp;  



ועכשיו למשחקים האלגבריים:
&nbsp;  





$$
(1)\,\,g(a+h)\,=\,{\color{blue}g(a)}+g(a+h){\color{red}-g(a)}
$$


&nbsp;  


$$
-ML(h)=-M\left(L(h)\right)\,=\,{\color{purple}{\color{red}-M\left(g(a+h)-g(a)\right)}{\color{blue}\,+\,M\left(g(a+h)-g(a)\right)}}-M\left(L(h)\right)\,=
$$



$$
=\,-M\left(g(a+h)-g(a)\right)+M\left(g(a+h)-g(a)-L(h)\right)
$$



$$
\Longrightarrow\,\,\,(2)\,\,\,\frac{-ML(h)}{\left\Vert h\right\Vert }\,=\,\frac{-M\left(g(a+h)-g(a)\right)}{\left\Vert h\right\Vert }+M\left(\frac{g(a+h)-g(a)-L(h)}{\left\Vert h\right\Vert }\right)
$$


&nbsp;  



$$
\frac{f(g(a+h))-f(g(a))-ML(h)}{\left\Vert h\right\Vert }\,\,\overset{(1)}{=}\,\,\frac{\,{\color{brown}{\color{purple}{\color{cyan}{\color{violet}f\left(g(a)+g(a+h)-g(a)\right)}}}}-f\left(g(a)\right)-ML(h)}{\left\Vert h\right\Vert }\,\,\overset{(2)}{=}
$$



$$
\overset{(2)}{=}\,\,\frac{f\left(g(a)+g(a+h)-g(a)\right)-f\left(g(a)\right){\color{brown}{\color{violet}-M\left(g(a+h)-g(a)\right)}}}{\left\Vert h\right\Vert }{\color{brown}{\color{violet}+M\left(\frac{g(a+h)-g(a)-L(h)}{\left\Vert h\right\Vert }\right)}}\,\,=
$$



$$
\overset{(k:=g(a+h)-g(a))}{=}\,\,{\color{purple}{\color{teal}\frac{f\left(g(a)+k\right)-f\left(g(a)\right)-M\left(k\right)}{\left\Vert h\right\Vert }}}+{\color{teal}{\color{orange}M\left(\frac{g(a+h)-g(a)-L(h)}{\left\Vert h\right\Vert }\right)}}
$$


&nbsp;  



באגף שמאל הביטוי המקורי, באגף ימין 2 חלקים -- הימני
מזכיר את $$Dg(a)$$ והשמאלי מזכיר את $$Df\left(g(a)\right)$$.
&nbsp;  

&nbsp;  
רצינו להוכיח שהביטוי המקורי מתאפס כש-$$h$$ שואף ל-0.
נראה זאת באמצעות 2 החלקים באגף ימין:


(-) החלק הירוק: $$L$$ הוא הדיפרנציאל של $$g$$ ב-$$a$$, לכן
מהגדרת הדיפרנציאל הביטוי בתוך הסוגריים מתאפס כאשר $$h\rightarrow0$$.
בגלל ש-$$M$$ העתקה לינארית, הביטוי כולו שואף לאפס.


(-) החלק הסגול: מהגדרת $$k$$ (זוכרים שם בסוגריים הקטנות?) ומרציפות
$$g$$ סביב $$a$$ (שמתקיימת לפי הדיפרנציאביליות ב-$$a$$),
אם $$h\rightarrow0$$ אז גם $$k\rightarrow0$$. נטפל רגע בביטוי
עצמו:

$$
\underset{h\rightarrow0}{lim}\frac{f\left(g(a)+k\right)-f\left(g(a)\right)-M(k)}{\left\Vert h\right\Vert }\,\,=\,\,\underset{h\rightarrow0}{lim}\frac{f\left(g(a)+k\right)-f\left(g(a)\right)-M(k)}{\left\Vert k\right\Vert }\cdot\frac{1}{\left\Vert h\right\Vert }\left\Vert k\right\Vert \,\,=\,\,
$$



$$
=\,\,\underset{h\rightarrow0}{lim}\frac{f\left(g(a)+k\right)-f\left(g(a)\right)-M(k)}{\left\Vert k\right\Vert }\cdot\left\Vert \frac{k}{||h||}\right\Vert \,\,=\,\,\underset{h\rightarrow0}{lim}\frac{f\left(g(a)+k\right)-f\left(g(a)\right)-M(k)}{\left\Vert k\right\Vert }\cdot\underset{h\rightarrow0}{lim}\left\Vert \frac{g(a+h)-g(a)}{\left\Vert h\right\Vert }\right\Vert 
$$


&nbsp;  



הגורם השמאלי שואף ל-0 מהגדרת הדיפרנציאל $$M=Df(g(a))$$).
נותר להראות שהגורם הימני חסום, ובזה נסיים:

$$
\underset{h\rightarrow0}{lim}\left\Vert \frac{g(a+h)-g(a)}{\left\Vert h\right\Vert }\right\Vert \,\,\overset{\text{המרונה תופיצר}}{=}\,\,\left\Vert \underset{h\rightarrow0}{lim}\frac{g(a+h)-g(a)}{\left\Vert h\right\Vert }\right\Vert \,\,\overset{\text{לאיצנרפיד תרדגה}}{=}\,\,\left\Vert \underset{h\rightarrow0}{lim}\frac{L(h)+o(\left\Vert h\right\Vert )}{\left\Vert h\right\Vert }\right\Vert \,\,=
$$



$$
=\,\,\left\Vert \underset{h\rightarrow0}{lim}\frac{L(h)}{\left\Vert h\right\Vert }+\underset{h\rightarrow0}{lim}\frac{o(\left\Vert h\right\Vert )}{\left\Vert h\right\Vert }\right\Vert \,\,=\,\,\left\Vert \underset{h\rightarrow0}{lim}L\left(\frac{h}{\left\Vert h\right\Vert }\right)+\underset{h\rightarrow0}{lim}\frac{o(\left\Vert h\right\Vert )}{\left\Vert h\right\Vert }\right\Vert \,\,=\,\,\left\Vert \underset{h\rightarrow0}{lim}L\left(\frac{h}{\left\Vert h\right\Vert }\right)+0\right\Vert 
$$

@@@@@@@@@@@ בעיה - איך מצדיקים שהביטוי הזה חסום? איך מתעסקים עם הגבול
שנותר שם? @@@@@@@@@@@@@@
&nbsp;  

&nbsp;  
נתקעתי - איך מוכיחים באופן פורמלי שהביטוי הימני חסום??? בגלל הנורמה
במונה אי אפשר להגיד "זו הנגזרת"
וזהו

$$
\underset{h\rightarrow0}{lim}\frac{f(a+h)-f(a)-T(h)}{||h||}=0\,\,\Longrightarrow\,\,f(a+h)-f(a)=T(h)+o(||h||)\,\,\Longrightarrow\,\,f(a+h)-f(a)\,||=||\,T(h)+o(||h||)\,||
$$


&nbsp;  

&nbsp;  

&nbsp;  

