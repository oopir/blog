---
title: תכונות הנגזרת - החלק הקל
---


<h1 style="text-align: center">תכונות הנגזרת - החלק הקל</h1>


לציין שאת ההוכחה לכלל השרשרת לקחתי מהספר $$Multivariable\,Calculus\,(George\,Cain\,\&\,James\,Herod)$$


ליצור פרק שלם על "איך בכלל הגיעו להבנה שזה כפל מטריצות?
מה הייתה האינטואיציה שהביאה אותם לחשוב על זה? איזה דוגמאות קטנות ופשוטות
הובילו לכאן?"

<br>
<h2>כלל השרשרת</h2>

<strong>הקדמה:</strong> לכתוב חלק שמזכיר ומגדיר כמו שצריך את כלל השרשרת (בפרט,
תדגיש שבביטוי $$Df(g(a))$$, $$g(a)$$ זו נקודה, בעוד שבביטוי
$$Dg(a)$$, $$a$$ זו הנקודה ו-$$g(a)$$ אינו בעל משמעות בפני
עצמו.).
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
{\color{teal}{\color{green}{\color{orange}{\color{teal}\frac{f(g(a+h))-f(g(a))-ML(h)}{\left\Vert h\right\Vert }}}}}\,\,\overset{(1)}{=}\,\,\frac{f\left(g(a)+g(a+h)-g(a)\right)-f\left(g(a)\right)-ML(h)}{\left\Vert h\right\Vert }\,\,\overset{(2)}{=}
$$



$$
\overset{(2)}{=}\,\,\frac{f\left(g(a)+g(a+h)-g(a)\right)-f\left(g(a)\right)-M\left(g(a+h)-g(a)\right)}{\left\Vert h\right\Vert }+M\left(\frac{g(a+h)-g(a)-L(h)}{\left\Vert h\right\Vert }\right)\,\,=
$$



$$
\overset{(k:=g(a+h)-g(a))}{=}\,\,{\color{purple}\frac{f\left(g(a)+k\right)-f\left(g(a)\right)-M\left(k\right)}{\left\Vert h\right\Vert }}+{\color{teal}{\color{orange}M\left(\frac{g(a+h)-g(a)-L(h)}{\left\Vert h\right\Vert }\right)}}
$$


&nbsp;  



באגף שמאל הביטוי המקורי, באגף ימין 2 חלקים -- הימני
מזכיר את $$Dg(a)$$ והשמאלי מזכיר את $$Df\left(g(a)\right)$$.
&nbsp;  

&nbsp;  
רצינו להוכיח שהביטוי המקורי מתאפס כש-$$h$$ שואף ל-0.
נראה זאת באמצעות 2 החלקים באגף ימין:


(-) החלק הצהוב: $$L$$ הוא הדיפרנציאל של $$g$$ ב-$$a$$, לכן
מהגדרת הדיפרנציאל הביטוי בתוך הסוגריים מתאפס כאשר $$h\rightarrow0$$.
בגלל ש-$$M$$ העתקה לינארית, הביטוי כולו שואף לאפס.


(-) החלק הסגול: מהגדרת $$k$$ (זוכרים שם בסוגריים הקטנות?) ומרציפות
$$g$$ סביב $$a$$ (שמתקיימת לפי הדיפרנציאביליות ב-$$a$$),
כאשר $$h\rightarrow0$$ מתקיים גם $$k\rightarrow0$$. נטפל רגע
בביטוי עצמו:

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


