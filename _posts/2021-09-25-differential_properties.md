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
ואני ממליץ לעבור עליו <strong>פעמיים</strong> לפני שממשיכים למקרים האחרים.
אני ממליץ גם לרשום בצד את ההגדרה של כל פונקציית עזר שניצור, כי חלק
מהמעברים מבלבלים.


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
מסמלת נקודה, לא פונקציה). עכשיו נוכל ממש לפרט, כי $$p$$ מנוסחת
במפורשות ולא תלויה ב-$$f/g$$. הנגזרות החלקיות של $$p$$ הן $$\frac{\partial p}{\partial x_{1}}(a)=1\,,\,\frac{\partial p}{\partial x_{2}}(a)=1$$,
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
מסקנה: הדיפרנציאל של סכום פונקציות הוא סכום הדיפרנציאלים! אם עד לפה
הבנתם, נמשיך הלאה.
&nbsp;  

&nbsp;  
<strong>הפרש פונקציות</strong>


דמיינו קופי-פייסט לחלק הקודם, רק עם: $$p(x)=x_{1}-x_{2}$$, $$Dp\left(q_{i}(x)\right)\,=\,
\begin{bmatrix}
1 & -1
\end{bmatrix}
$$.
אם תעברו על החלקים האחרונים עם המטריצה החדשה, תראו שמתקיים $$D(f-g)(x)=Df(x)-Dg(x)$$.
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

נראה את הנדרש ע"י ההגדרה הבאה של הנגזרת:

$$
f(g(x+h))-f(g(x))\,=\,\left(Df(g(x))\circ Dg(x)\right)\cdot h+o(h)
$$

($$f$$ דיפרנציאבילית בנקודה $$g(x)$$, לכן עבור $$h$$ קטן
מספיק היא אכן מוגדרת ב--$$g(x+h)$$. ניזכר ש--$$g(x+h)$$ מוגדר
כי $$g$$ גזירה ב--$$x$$ ומכך רציפה ב--$$x$$).


הדיפרנציאביליות של $$f$$ ב--$$g(x)$$ אומרת: 

$$
f(g(x)+k)-f(g(x))\,=\,Df(g(x))\cdot k+o(k)
$$

אם היינו בוחרים את $$k$$ כך שיתקיים $$g(x)+k=g(x+h)$$ (ומכך
$$k=g(x+h)-g(x)$$), היינו מקבלים:

$$
f(g(x+h))-f(g(x))\,=\,Df(g(x))\cdot(g(x+h)-g(x))+o(g(x+h)-g(x))=\cdots
$$

ניעזר בהגדרת הדיפרנציאל שוב (הפעם עם הגזירות של $$g$$ ב--$$x$$)
ונקבל:

$$
\cdots\,=\,Df(g(x))\cdot(Dg(x)\cdot h+o(h))+o(Dg(x)\cdot h+o(h))
$$

נשים לב ש--$$Df(g(x))$$ היא העתקה לינארית, ולכן מלינאריות אפשר
"לפתוח סוגריים":

$$
\cdots\,=\,Df(g(x))\cdot(Dg(x)\cdot h)+Df(g(x))\cdot o(h)+o(Dg(x)\cdot h+o(h))\,=
$$



$$
=\,(Df(g(x))\circ Dg(x))\cdot h+Df(g(x))\cdot o(h)+o(Dg(x)\cdot h+o(h))
$$

שימו לב: הגורם הראשון הוא מה שאנחנו טוענים להיות הנגזרת של $$f\circ g$$.
אם נוכיח ש--2 הגורמים האחרים מתאפסים כש--$$h\rightarrow0$$,
זה יוכיח את הנדרש.


שני הגורמים מכילים הפעלה של העתקה לינארית על וקטור שקשור ב--$$h$$.
נרצה להראות שההפעלה תשאף ל--0 כאשר $$h\rightarrow0$$.
נשים לב שלכל העתקה לינארית מתקיים:

$$
\left\Vert T(h)\right\Vert \,=\,\left\Vert T\left(\sum_{i=1}^{n}h_{i}e_{i}\right)\right\Vert \,=\,\left\Vert \sum_{i=1}^{n}h_{i}T(e_{i})\right\Vert \,=\,\sum_{i=1}^{n}\left\Vert h_{i}T(e_{i})\right\Vert \,=
$$



$$
=\,\sum_{i=1}^{n}\left|h_{i}\right|\left\Vert T(e_{i})\right\Vert \,\overset{(*)}{\leq}\,\sum_{i=1}^{n}\left\Vert h\right\Vert \left\Vert T(e_{i})\right\Vert \,=\,\left(\sum_{i=1}^{n}\left\Vert T(e_{i})\right\Vert \right)\left\Vert h\right\Vert \,=\,C\cdot\left\Vert h\right\Vert \,\overset{h\rightarrow0}{\longrightarrow}\,0
$$



$$
(*)\,\,\,\left|h_{i}\right|=\sqrt{h_{i}^{2}}\leq\sqrt{h_{1}^{2}+\cdots+h_{n}^{2}}=\left\Vert h\right\Vert 
$$

כאשר $$C$$ הוא קבוע כלשהו שתלוי ב--$$T$$. מתכונות הנורמה ומרציפות
הנורמה, הביטוי $$\left\Vert T(h)\right\Vert \overset{h\rightarrow0}{\longrightarrow}0$$
גורר $$T(h)\overset{h\rightarrow0}{\longrightarrow}0$$, לכן כאשר
$$h\rightarrow0$$ נוכל להסיק $$T(h)\overset{h\rightarrow0}{\longrightarrow}0$$.


מבלי להיכנס לדקויות ולהגדרה הפורמלית של $$o(\,*\,)$$, אפשר להשתכנע
ששני הגורמים מקודם מתאפסים כנדרש.



