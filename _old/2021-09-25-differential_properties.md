---
title: כמה תכונות של הנגזרת
---


<h1 style="text-align: center">כמה תכונות של הנגזרת</h1>


הדבר הטבעי לעשות אחרי שהגדרנו את הנגזרת הוא להראות חוקי גזירה כלליים:
מה עושים עם סכום, הפרש, כפל, מנה והרכבה של פונקציות. כשהייתי בשלב
הזה ב"אינפי 1"
(אותו למדתי מהספרים של הפתוחה), כל הוכחה הייתה קצת יותר מסובכת מהקודמת,
כשהשיא הגיע בהרכבת פונקציות (כלל השרשרת) ובמשפט הפונקציה ההפוכה. כאן
נעבוד בסדר שונה -- ננסח את כלל השרשרת, נוכיח בעזרתו את כל השאר, ואז
נראה את ההוכחה של כלל השרשרת.

<br>
<h2>רגע לפני שנתחיל</h2>

@@@@@@@@ לכתוב על הדיפרנציאל של $$c\cdot f(x)$$ והדיפרנציאל של
העתקות לינאריות @@@@@@@@

<br>
<h2>איך כלל השרשרת נראה</h2>

באינפי 1 כלל השרשרת הוא הכלל $$h'(x)=f'(g(x))\cdot g'(x)$$.
ליתר דיוק המשפט אומר: אם $$g$$ גזירה בנקודה $$a$$ ואם $$f$$
גזירה בנקודה $$g(a)$$, אז הפונקציה $$h(x)=f(g(x))$$ גזירה בנקודה
$$a$$ ומתקיים $$h'(a)=f'(g(a))\cdot g'(a)$$. 

ננסה רגע "לאלץ" את מושג הדיפרנציאל
לתוך המשפט: אם $$g$$ דיפרנציאבילית ב-$$a$$ ואם $$f$$ דיפרנציאבילית
ב-$$g(a)$$, אז $$h$$ דיפרנציאבילית ב-$$a$$ ומתקיים $$Dh(a)=Df(g(a))\cdot Dg(a)$$.
קצת מוזר לבטא את כפל הנגזרות בתור כפל מטריצות $$1\times1$$, אבל
תיכף נגלה שנצטרך להתרגל לזה.
&nbsp;  



אז כן, מסתבר שהדיפרנציאל של הרכבת פונקציות מתקבל ע"י
מכפלת הדיפרנציאלים. אני יכול רק לנחש מאיפה הגיעו לרעיון: אולי שמו
לב לדפוס מסוים במקרים פרטיים, אולי הרכבת פונקציות גרמה למישהו לחשוב
על הרכבת העתקות לינאריות (המקבילה של כפל מטריצות), או שסתם חשבו "איזה
כיף יהיה אם זה יתנהג ככה". בכל מקרה, בסוף הוכיחו
שזה נכון, אז בואו ננסח זאת:
&nbsp;  



תהי $$g:\mathbb{R}^{n}\rightarrow\mathbb{R}^{\boldsymbol{k}}$$
ותהי $$f:\mathbb{R}^{\boldsymbol{k}}\rightarrow\mathbb{R}^{m}$$.
אם $$g$$ דיפרנציאבילית ב-$$a$$ ו-$$f$$ דיפרנציאבילית ב-$$g(a)$$,
אז הפונקציה $$h(x)=f(g(x))\,,\,h:\mathbb{R}^{n}\rightarrow\mathbb{R}^{m}$$
מקיימת: 

$$
Dh(a)=Df\left(g(a)\right)\cdot Dg(a)
$$


&nbsp;  



ההוכחה היא די ארוכה (ובעיקר טכנית/אלגברית), אז לפני שנגיע אליה בואו
נהנה מהשימוש במשפט.

<br>
<h2>איך כלל השרשרת עוזר לנו</h2>

<strong>סכום פונקציות</strong>

העבודה שנעשה עבור סכום פונקציות תהווה "תבנית"
שאיתה נפתור גם את שאר המקרים בקלות. לכן אכתוב את חלק זה בפירוט ויסודיות,
ואני ממליץ לעבור עליו פעמיים לפני שממשיכים למקרים האחרים.


יהיו $$f,g:\mathbb{R}^{n}\rightarrow\mathbb{R}^{m}$$. נעבוד ב-3
שלבים: נביע את $$f+g$$ בתור הרכבת פונקציות, נחשב את הדיפרנציאל
של כל פונקציה בהרכבה, ואז נפעיל את כלל השרשרת.
&nbsp;  



נתחיל ביצירת ההרכבה: אזכיר שכאשר טווח הפונקציה הוא $$R^{m}$$ נוח
לחשוב על הפונקציה בתור סט של רכיבים:

$$
f=(f_{1},...,f_{m})\,,\,g=(g_{1},...,g_{m})\,,\,
$$



$$
f+g=\left((f+g)_{1},...,(f+g)_{m}\right)=\left(f_{1}+g_{1},...,f_{m}+g_{m}\right)
$$

 
&nbsp;  



נגדיר פונקציות עזר: $$p:\mathbb{R}^{2}\rightarrow\mathbb{R}\,\,,\,\,p(x)=x_{1}+x_{2}$$,
$$q_{i}:\mathbb{R}^{n}\rightarrow\mathbb{R}^{2}\,\,,\,\,q_{i}(x)=(f_{i}(x),g_{i}(x))$$
(כאן לא נגדיר $$q_{i}=(q_{i_{1}},q_{i_{2}})$$ כמו שעשינו עם $$f,g$$,
כי ב-$$q_{i}$$ כבר יש לכל רכיב שם משלו).

קחו רגע להשתכנע שמתקיים:

$$
(f+g)(x)=\left(f_{1}+g_{1},...,f_{m}+g_{m}\right)=(p(q_{1}(x)),...,p(q_{m}(x))
$$


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
תחילה נבטא את $$Dq_{i}(x)$$. לפי התחום והטווח של $$q_{i}$$ זו
תהיה מטריצה $$2\times n$$, ולפי מה שלמדנו על דיפרנציאל בפונקציות
$$\mathbb{R}^{n}\rightarrow\mathbb{R}^{m}$$נקבל: 

$$
Dq_{i}(x)\,=\,
\begin{bmatrix}
\frac{\partial f_{i}}{\partial x_{1}}(x) & \cdots & \frac{\partial f_{i}}{\partial x_{n}}(x)\\

\frac{\partial g_{i}}{\partial x_{1}}(x) & \cdots & \frac{\partial g_{i}}{\partial x_{n}}(x)\\
\end{bmatrix}

$$


&nbsp;  



נעבור להביע את $$Dp\left(q_{i}(x)\right)$$ (זכרו - פה $$q_{i}(x)$$
מסמלת נקודה ספציפית, שעבורה נבטא את הדיפרנציאל). עכשיו נוכל ממש לפרט,
כי $$p$$ מנוסחת במפורשות ולא תלויה ב-$$f$$ או $$g$$. הנגזרות
החלקיות של $$p$$ הן $$\frac{\partial p}{\partial x_{1}}(a)=1\,,\,\frac{\partial p}{\partial x_{2}}(a)=1$$,
ולכן נקבל:

$$
Dp\left(q_{i}(x)\right)\,=\,
\begin{bmatrix}
\frac{\partial p}{\partial x_{1}}\left(q_{i}(x)\right) & \frac{\partial p}{\partial x_{2}}\left(q_{i}(x)\right)
\end{bmatrix}
\,=\,
\begin{bmatrix}
1 & 1
\end{bmatrix}

$$


&nbsp;  



וסוף סוף נוכל להשתמש בכלל השרשרת: 

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


&nbsp;  
מסקנה: הדיפרנציאל של סכום פונקציות הוא סכום הדיפרנציאלים!
&nbsp;  

&nbsp;  
<strong>הפרש פונקציות</strong>


דמיינו קופי-פייסט לחלק הקודם, רק עם: $$p(x)=x_{1}-x_{2}$$, $$Dp\left(q_{i}(x)\right)\,=\,
\begin{bmatrix}
1 & -1
\end{bmatrix}
$$.
אם תעברו על החלקים האחרונים עם המטריצה החדשה, תראו שמתקיים $$D(f+g)(x)=Df(x)-Dg(x)$$.
&nbsp;  

&nbsp;  
<strong>מכפלת פונקציות</strong>


כאן נצטמצם ל-$$f,g:\mathbb{R}^{n}\rightarrow\mathbb{R}$$ (אחרת
$$f\cdot g$$ הייתה מכפלה של וקטורים, ואני לא יודע איך מגדירים את
זה). זה אומר ש--$$f(x),g(x)$$ הם מספרים ממשיים, $$D(f\cdot g)(x)$$
היא מטריצה $$1\times n$$ ושבמקום $$q_{i}$$ אפשר לרשום רק $$q$$.
&nbsp;  

&nbsp;  
עכשיו נגדיר $$p(x)=x_{1}\cdot x_{2}$$. הפעם הנגזרות החלקיות הן
$$\frac{dp}{dx_{1}}(a)=a_{2}\,\,,\,\,\frac{dp}{dx_{2}}(a)=a_{1}$$,
ולכן נקבל: 

$$
\frac{dp}{dx_{1}}(q(x))=q(x)_{2}=g(x)\,\,,\,\,\frac{dp}{dx_{2}}(q(x))=q(x)_{1}=f(x)\,\,\Longrightarrow\,\,Dp\left(q(x)\right)\,=\,
\begin{bmatrix}
g(x) & f(x)
\end{bmatrix}

$$

מכאן נמשיך הלאה:

$$
\boldsymbol{D(f\cdot g)(x)}\,=\,\cdots\,=\,
\begin{bmatrix}
g(x) & f(x)
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
g(x)\frac{\partial f_{i}}{\partial x_{1}}(x)+f(x)\frac{\partial g_{i}}{\partial x_{1}}(x) & \cdots & g(x)\frac{\partial f_{i}}{\partial x_{n}}(x)+f(x)\frac{\partial g_{i}}{\partial x_{n}}(x)
\end{bmatrix}
\,=
$$



$$
=\,g(x)
\begin{bmatrix}
\frac{\partial f_{i}}{\partial x_{1}}(x) & \cdots & \frac{\partial f_{i}}{\partial x_{n}}(x)
\end{bmatrix}
+f(x)
\begin{bmatrix}
\frac{\partial g_{i}}{\partial x_{1}}(x) & \cdots & \frac{\partial g_{i}}{\partial x_{n}}(x)
\end{bmatrix}
\,=\,\boldsymbol{g(x)\cdot Df(x)+f(x)\cdot Dg(x)}
$$

ושימו לב שבמקרה הפרטי מאינפי 1 ($$Df(x)==f'(x),Dg(x)=g'(x)$$)
באמת מקבלים את הנוסחה שמוכרת לנו
&nbsp;  



<strong>מנת פונקציות</strong>


נישאר עם $$f,g:\mathbb{R}^{n}\rightarrow\mathbb{R}$$ ונחייב גם
ש-$$g$$ לא מתאפסת בסביבה של $$x$$. יאללה לעבודה:

$$
p(x)=\frac{x_{1}}{x_{2}}\,\Longrightarrow\,\frac{dp}{dx_{1}}(x)=\frac{1}{x_{2}}\,,\,\frac{dp}{dx_{2}}(x)=\frac{-x_{1}}{x_{2}^{2}}
$$



$$
\Longrightarrow\,\frac{dp}{dx_{1}}(q(x))=\frac{1}{g(x)}\,,\,\frac{dp}{dx_{2}}(x)=\frac{-f(x)}{\left(g(x)\right)^{2}}\,\Longrightarrow\,Dp(q(x))=
\begin{bmatrix}
\frac{1}{g(x)} & \frac{-f(x)}{\left(g(x)\right)^{2}}
\end{bmatrix}

$$



$$
\,\,\,
$$



$$
\boldsymbol{D\left(\frac{f}{g}\right)(x)}\,=\,\cdots\,=\,
\begin{bmatrix}
\frac{1}{g(x)} & \frac{-f(x)}{\left(g(x)\right)^{2}}
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
\frac{1}{g(x)}\frac{\partial f_{i}}{\partial x_{1}}(x)+\frac{-f(x)}{\left(g(x)\right)^{2}}\frac{\partial g_{i}}{\partial x_{1}}(x) & \cdots & \frac{1}{g(x)}\frac{\partial f_{i}}{\partial x_{n}}(x)+\frac{-f(x)}{\left(g(x)\right)^{2}}\frac{\partial g_{i}}{\partial x_{n}}(x)
\end{bmatrix}
\,=
$$



$$
=\,\frac{1}{g(x)}
\begin{bmatrix}
\frac{\partial f_{i}}{\partial x_{1}}(x) & \cdots & \frac{\partial f_{i}}{\partial x_{n}}(x)
\end{bmatrix}
+\frac{-f(x)}{\left(g(x)\right)^{2}}
\begin{bmatrix}
\frac{\partial g_{i}}{\partial x_{1}}(x) & \cdots & \frac{\partial g_{i}}{\partial x_{n}}(x)
\end{bmatrix}
\,=
$$



$$
=\,\frac{1}{g(x)}Df(x)-\frac{f(x)}{\left(g(x)\right)^{2}}Dg(x)\,=\,\boldsymbol{\frac{g(x)\cdot Df(x)-f(x)Dg(x)}{\left(g(x)\right)^{2}}}
$$



<br>
<h2>משפט הפונקציה ההפוכה</h2>

זו התכונה האחרונה שנראה לפני ההוכחה של כלל השרשרת. @@@@@@@@@ להשלים
@@@@@@@@

<br>
<h2>איך מוכיחים את כלל השרשרת</h2>

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
\frac{f(g(a+h))-f(g(a))-ML(h)}{\left\Vert h\right\Vert }\,\,=\,\,\frac{f(g(a+h))-f(g(a))}{\left\Vert h\right\Vert }+\frac{-ML(h)}{\left\Vert h\right\Vert }\,\,\overset{(1)}{=}
$$



$$
\overset{(1)}{=}\,\,\frac{\,{\color{violet}f\left(g(a)+g(a+h)-g(a)\right)}-f\left(g(a)\right)}{\left\Vert h\right\Vert }+\frac{-ML(h)}{\left\Vert h\right\Vert }\,\,\overset{(2)}{=}
$$



$$
\overset{(2)}{=}\,\,\frac{f\left(g(a)+g(a+h)-g(a)\right)-f\left(g(a)\right)}{\left\Vert h\right\Vert }{\color{violet}+\frac{-M\left(g(a+h)-g(a)\right)}{\left\Vert h\right\Vert }}{\color{brown}{\color{violet}+M\left(\frac{g(a+h)-g(a)-L(h)}{\left\Vert h\right\Vert }\right)}}\,\,=
$$



$$
\overset{(k:=g(a+h)-g(a))}{=}\,\,\frac{f\left(g(a)+k\right)-f\left(g(a)\right)}{\left\Vert h\right\Vert }+\frac{-M(k)}{\left\Vert h\right\Vert }+M\left(\frac{g(a+h)-g(a)-L(h)}{\left\Vert h\right\Vert }\right)\,\,=
$$



$$
=\,\,{\color{teal}\frac{f\left(g(a)+k\right)-f\left(g(a)\right)-M\left(k\right)}{\left\Vert h\right\Vert }}+{\color{orange}M\left(\frac{g(a+h)-g(a)-L(h)}{\left\Vert h\right\Vert }\right)}
$$


&nbsp;  



באגף שמאל הביטוי המקורי, באגף ימין 2 חלקים -- כל חלק
מזכיר את הגדרת הדיפרנציאל (אחד עבור $$g$$ בנקודה $$a$$ והשני
עבור $$f$$ בנקודה $$g(a)$$).
&nbsp;  

&nbsp;  
רצינו להוכיח שהביטוי המקורי מתאפס כש-$$h$$ שואף ל-0.
נראה זאת באמצעות 2 החלקים באגף ימין:


(-) החלק הכתום: $$L$$ הוא הדיפרנציאל של $$g$$ ב-$$a$$, לכן
מהגדרת הדיפרנציאל הביטוי בתוך הסוגריים מתאפס כאשר $$h\rightarrow0$$.
בגלל ש-$$M$$ העתקה לינארית, הביטוי כולו שואף לאפס.


(-) החלק הירוק: מהגדרת $$k$$ (זוכרים שם בסוגריים הקטנות?) ומרציפות
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




