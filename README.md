Download Link: https://assignmentchef.com/product/solved-csci316-assignment2
<br>
Lisp’s comment character is “;”––this makes Lisp ignore the rest of the line, and is used like “//” in C++ or Java.  See p. 150 of Touretzky for more about comments.

<strong>IMPORTANT:  Do <u>NOT</u> use SETF except when you are answering questions which explicitly indicate that you may use them! </strong>

<ol>

 <li>(a) Can an atom be a variable?                (b) Can a number be a variable?</li>

</ol>

(c)  Can a list be a variable?                      (d) Can an atom have no value?

<ul>

 <li>Can an atom have more than one value at the same time?</li>

 <li>Can a variable have itself as a value?</li>

 <li>Can a list (A B C) be the value of two different variables?</li>

</ul>




<ol start="2">

 <li>Each of the following may be a single atom, a single list, or neither. Identify each         For the lists, also say how many elements the list has.  [You are<strong>      <em><u>not</u></em> </strong>asked to evaluate any expression––e.g., (+ 1 9) would be a <strong><em>list of 3 elements</em></strong>,      even though this list would evaluate to a numeric atom (i.e., 10).]           (a)  ATOMS                                     (b) (THIS IS AN ATOM)        (c)  )(</li>

</ol>

(d) ((A B)(C D)) 3 (3)               (e) (()())

(f) ((A B C                                          (g) (/ (+ 3 1) (- 3 1))       (h) (LIST 3)




3.[<strong>Exercise 4 on p. 37 of Wilensky</strong>]  Use SETF to assign X the value (A B C), and      then use X to produce the list (A B C A B C).




4.<strong>[Exercise 5 on p. 37 of Wilensky]  </strong>Write the expression  ”(A) using QUOTE      rather than ‘.   What is the data type of the expression ‘A ?




5.(a)  Use SETF to give Y the value (A B).  But, instead of writing ‘(A B), you must           use a Lisp function call to create the list (A B).




(b) Write code that makes the list  (D A).  However, you must get A from the                    variable Y, which has the value (A B) from part (a).

<strong> </strong>

<strong> </strong>

<ol start="6">

 <li>Define a function called SQR that returns a list of the perimeter and the area of  a square, given the length of one side.  Thus (SQR 2) should return (8 4).</li>

</ol>




Lisp Assignment 2: Page 1 of  4

<ol start="7">

 <li>Define QUADRATIC, a function with three parameters A, B and C that returns a list of the two roots of the equation <em>Ax<sup>2</sup> + Bx + C = </em>  You should use the         built-in function SQRT.  Recall that the two roots are given by:</li>

</ol>

<sup>− +</sup><em><u><sup>B B</sup></u></em><sup>2 </sup><sup>−</sup><u><sup>4<em>AC</em></sup></u>     and    <sup>− −</sup><em><u><sup>B B</sup></u></em><sup>2 </sup><sup>−</sup><u><sup>4<em>AC</em></sup></u>

2<em>A                                         </em>2<em>A</em>




8.<strong>[Exercise 1 on p. 52 of Wilensky]</strong>  Write a Lisp function that computes the area of         a circle given its radius.  Use the predefined constant PI.




<ol start="9">

 <li>Define a function called FTOC which takes as its argument a degree reading in</li>

</ol>

Fahrenheit and returns its Celsius equivalent.  (The Celsius equivalent of a                  Fahrenheit temperature is obtained by subtracting 32 and multiplying by 5/9.)




<ol start="10">

 <li>Define a function ROTATE-LEFT which takes a list as argument and returns a new list in which the former first element has become the last element.  Thus              (ROTATE-LEFT ‘(A B C D)) should return (B C D A).</li>

</ol>




11.<strong>[Exercise 4 on pp. 52 – 3 of Wilensky]</strong> A point (<em>x</em>, <em>y</em>) in the plane can be        represented as a two-element list (<em>x</em> <em>y</em>).  Write a Lisp function that takes two such        lists as arguments and returns the distance between the corresponding points.        Recall that the distance between two points (<em>x</em><sub>1</sub>, <em>y</em><sub>1</sub>) and (<em>x</em><sub>2</sub>, <em>y</em><sub>2</sub>) is given by

(<em>x</em>1−<em>x</em>2)2 +(<em>y</em>1−<em>y</em>2)2.




12.<strong>[Exercise 5 on pp. 52 – 3 of Wilensky] </strong>Define Lisp functions HEAD and TAIL       that behave just like CAR and CDR, respectively.




13.<strong>[Exercise 6 on pp. 52 – 3 of Wilensky] </strong>Define a Lisp function SWITCH that        takes as its argument a two-element list and returns a list consisting of the same       two elements, but in the opposite order.  <strong>Example</strong>: (switch ‘(A B)) =&gt; (B A).




<ol start="14">

 <li>Suppose you have just entered the following three Lisp expressions at successive Clisp &gt; prompts (with no spaces before or after * and + in 8*7 and 8+7):</li>

</ol>

(setf 8*7 5)

(defun 8+7 (x y) (+ x y))                    (defun 8*7 () 9)

If you now enter the expression    (8+7 (* 8 7) (8+7 (8*7) 8*7))       what value will be printed by Clisp?   Check your answer using Clisp.

<strong><em> </em></strong>

<strong><em> </em></strong>

<strong><em> </em></strong>

<strong><em> </em></strong>

<strong><em> </em></strong>

<strong><em> </em></strong>

<strong><em> </em></strong>

<strong><em><u>The next six questions are important</u></em></strong><strong><em>.</em></strong>  Be sure to check your answers using Clisp!




<ol start="15">

 <li><strong>[Exercise 1 on pp. 36 – 7 of Wilensky]</strong> For each of (a), (b), and (c) below,     suppose SETF has just been used to give the variable E the specified value.</li>

</ol>

(E.g., for (a) we suppose (setf e ‘(a b x d)) has just been entered at Clisp’s        &gt; prompt.)  In each case, write an expression that involves only E, car, and cdr,  <sup>      and which evaluates to the symbol </sup>X.   [<strong>Hint</strong>: For a specified value of (A X C), you         would be expected to write the expression  (car (cdr E)) because the car of the cdr of

(A X C) is X.]

(a)  <sub>  </sub>(A B X D)      (b) (A (B (X D)))  (c) (((A (B (X) D))))

16.<strong>[Exercise 2 on pp. 36 – 7 of Wilensky]</strong>  For each of the three lists in exercise 15,       write an expression that involves only quoted symbols, NIL, and calls of CONS,        and which evaluates to that list.   [<strong>Hint</strong>: For a list  (A X C), you would be expected         to write the expression  <sub> </sub>(cons ‘a (cons ‘x (cons ‘c nil))).]

<strong>Note</strong>: One way to solve such problems is to first write the list using calls of LIST, and then         rewrite the expression using appropriate calls of CONS.  (Another approach is to do a preorder         traversal of the tree-representations of the given lists––read p. 393 in Sethi for more on the         tree-representation of an S-expression.)




For questions 17 – 20, suppose E has been given a value as follows:

(    ‘((90 91 92 93 94 95 96 97 98 99) (+ 3 4 –) (9 19 29 39 49 59 69 79 89 99)))setf E   For each question, write an expression with the specified properties; your expressions may involve E, ‘A, ‘B and Lisp functions.  LIST is a good function to use.

<strong> </strong>

<strong>Example</strong>  Write an expression that <strong><em>does not involve any numbers</em></strong>, but which evaluates to the following list:

<strong>(92 (29 39 49 59 69 79 89 99 + 3 4 -))</strong>

<strong>Solution</strong>        (list (third (first E)) (append (rest (rest (third E))) (second E)))

<sub> </sub>[Or, equivalently, (list (caddr   (car E)) (append        (cddr (caddr E))   (cadr E))).] 17. Write an expression that <strong><em>does not involve any numbers</em></strong>, but which evaluates                 to the list <sub> </sub>(((90 91) 92 93 94 95 96 97 98 99) (A B 29 39 49 59 69 79 89 99)).

<ol start="18">

 <li>Write an expression that <strong><em>does not involve any numbers</em></strong>, but which evaluates        to the list ((90 A 92 93 94 95 96 97 98 99) 3  29 (4 29 39 49 59 69 79 89 99)).   19. Write an expression that <strong><em>does not involve any numbers</em></strong>, but which evaluates to             the list  <sub> </sub>((90 91 92 93 94 95 96 97 98 99 3) (+ 3 4 – 29 39 49 59 69 79 89 99)). 20. Write an expression that <strong><em>does not involve any numbers</em></strong>, but which evaluates                 to the list ((A 91 92 93 94 95 96 97 98 99) (90 (19 29) 39 49 59 69 79 89 99)).</li>

</ol>

<strong> </strong>

<strong>Working with Lisp Files </strong>




Suppose  xyz.lsp  is a file, in your current working directory, that contains one or more Lisp function definitions.  Then you can “load”  xyz.lsp  into Clisp by entering   (load “xyz.lsp”)<strong><sub>  </sub></strong>at Clisp’s &gt; prompt.  When you do this, the function definitions in xyz.lsp will be read into Clisp as if you had entered them one by one at Clisp’s prompt.  [If   (load “xyz.lsp”) produces an error, there is a syntax error in the function definitions in  xyz.lsp.]  Unless you are running Clisp as a subprocess of emacs (see below), each time you add a new lisp function definition to a file  xyz.lsp or modify an existing definition in the file, it’s a good idea to immediately save the file,  load  the saved file  into Clisp, and then test the new or modified function.  If you work this way, then whenever (load “xyz.lsp”) gives an error message it must be because of a syntax error in the new or modified function.

<strong><em><u>For problems 6 – 13,  write your function definitions in a file named </u></em></strong><strong><u>solutions.lsp</u></strong>.  On <strong>venus</strong> or <strong>euclid</strong> you should create the file in your current working directory––you could use   nano solutions.lsp   to do this.        If you are working on your PC (and have already installed Clisp on the PC), create a folder––c:316lisp, say–– on the PC to use as your working directory for Lisp. This can be done, e.g., as follows:

<ol>

 <li>Type <strong>Win-</strong>r (i.e., hold down the Windows key and type r) to open the Run dialog box.</li>

 <li>Type powershell   into the Open: textbox and press <sub>E</sub> to open a powershell window.</li>

 <li>In the powershell window, enter md c:316lisp   to create the folder c:316lisp.</li>

</ol>

All the Lisp files you create for this course (such as <strong>solutions.lsp</strong>) should be saved in this folder. After the folder has been created, do the following whenever you want to start Clisp on your PC:

<ol>

 <li>Type <strong>Win-</strong>r  to open the Run dialog box, type  powershell   into the Open: textbox, and press <sub>E</sub>.</li>

 <li>In the powershell window, enter cd c:316lisp   and enter  clisp   to start Clisp.</li>

</ol>

Then, assuming you have saved <strong>solutions.lsp</strong> in c:316lisp, you will be able to load  <strong>solutions.lsp</strong>  into Clisp by entering  (load “solutions.lsp”) at Clisp’s prompt.

You should <strong><em><u>not</u></em></strong> use  Notepad  to create <strong>solutions.lsp</strong> on a PC: It is much better to use an editor that matches parentheses for you. Some examples of such editors are listed at the bottom of this page.  I recommend you configure Windows to <strong><em><u>not</u> </em></strong>hide file name extensions (such as .lsp); this can be done as follows:

<ol>

 <li>Type <strong>Win-</strong>r (i.e., hold down the Windows key and type r) to open the Run dialog box.</li>

 <li>Type control folders into the Open: textbox and press <sub>E</sub>; this opens a folder options dialog box.</li>

 <li>Click on the View tab at the top of the Folder Options dialog box.</li>

 <li>In the “Advanced settings” window, find the “Hide extensions for known file types” checkbox. If that checkbox is unchecked, click Cancel; otherwise, <strong><em>uncheck the checkbox</em></strong> and click OK.</li>

</ol>







<strong>Emacs  is a Good Editor for Writing Lisp Code on euclid or venus </strong>




To learn to use emacs on <strong>euclid</strong>, connect to <strong>euclid</strong> using the native ssh client on a PC (in a cmd or powershell window) or a Mac (in a terminal window) and enter   emacs at the shell prompt. Then (once emacs has started up) type the two characters    <sub>F</sub>h t   to bring up a tutorial. This editor <em><u>automatically</u></em> matches parentheses––if you place the cursor at an opening parenthesis or <em>immediately after</em> a closing parenthesis, that and the matching parenthesis (if there is one) will be highlighted. Type the two characters   <sub>X</sub> Ff to move the cursor forward across one S-expression—when the cursor is at an opening parenthesis, this moves the cursor to the position that immediately follows the matching closing parenthesis. Conversely, typing   <sub>X</sub> Fb will move the cursor backward across one S-expression—when the cursor immediately follows a closing parenthesis, this moves the cursor back to the matching opening parenthesis.  When the cursor is at the start of an S-expression, typing  <sub>X</sub> Fk<strong>  </strong>will delete that S-expression (but typing   <sub>F</sub>y   will bring it back), whereas typing  <sub>X</sub> Ft will transpose it with the previous S-expression.

<strong>      </strong>You can run Clisp as a subprocess (an “inferior” process) within emacs.  To try this, start emacs on <strong>euclid</strong> by entering   emacs test.lsp<strong>  </strong>at the shell prompt.  (Any filename could be used instead of test.lsp.)    Split the emacs window into two by typing  <sub>F</sub>x 2<strong>   </strong>and then enter   <sub>X</sub> x run-lisp<strong>   </strong>to get a Clisp [1]&gt; prompt in one of the two windows.<strong>  </strong>After that you can switch back-and-forth between editing  test.lsp and using Clisp simply by typing  Fx o.<strong>  </strong>As soon as you have written a new function definition or made a change to a function definition in test.lsp, you can load that new/changed definition into Clisp by typing  X Fx<strong>  </strong>while the cursor is within or immediately to the right of the definition.  This allows you to test new/changed definitions before deciding whether to save the current edited version of  test.lsp.  In the Clisp window, you can cycle backward and forward through previously entered expressions by typing   <sub>X</sub> p and  <sub>X</sub> n.   To “unsplit” the window, type   <sub>F</sub>x 1  (after which you can switch between the editing and Clisp windows by entering  <sub>F</sub>x b).

The above instructions also work on <strong>venus</strong> if you connect to <strong>venus</strong> using the native ssh client on a PC (in a  cmd or powershell window), provided you have entered  /h<sub>ome/faculty/ykong/316setup</sub>  on  <strong>venus </strong> at some time this semester as the Lisp Assignment 1 document asked you to do.




<strong>Some Other Editors That Match Parentheses </strong>

The <sup> </sup>vim editor on <strong>venus</strong> and <strong>euclid</strong> matches parentheses automatically; also, if when vim is in command mode you type % at a parenthesis then the cursor will jump to the matching parenthesis. (Enter vimtutor on <strong>venus</strong> or <strong>euclid</strong> to bring up a tutorial that teaches beginners to use vim.)  The nano editor on <strong>venus</strong> and <strong>euclid</strong> can match parentheses, but <strong><em><u>not</u></em></strong> automatically: In nano, typing   <sub>X</sub> ]  when the cursor is at a parenthesis moves the cursor to the matching parenthesis. Free editors for PCs that support automatic parenthesis matching include:

Notepad++ <a href="https://notepad-plus-plus.org/"> </a><a href="https://notepad-plus-plus.org/"><strong>https://notepad-plus-plus.org</strong></a> <a href="https://notepad-plus-plus.org/"><strong> </strong></a><strong> </strong>

VS Code<strong>  </strong>  <a href="https://code.visualstudio.com/"><strong>https://code.visualstudio.com</strong></a> <strong> (<em><u>Don’t</u></em> use the remote-ssh extension to remotely edit files on euclid.)  </strong> Atom   <strong>  </strong>  <a href="https://atom.io/"><strong>https://atom.io</strong></a> <a href="https://atom.io/"><strong> </strong></a><strong>       </strong> jEdit  <strong>  </strong>  <a href="http://www.jedit.org/"><strong>http://www.jedit.org</strong></a> <a href="http://www.jedit.org/"><strong> </strong></a><strong> </strong>

As with emacs, the vim and nano editors are preinstalled on Macs for use in a terminal window. VS Code, Atom, and jEdit are also available for Macs.  Sublime Text <a href="https://www.sublimetext.com/">(</a><a href="https://www.sublimetext.com/"><strong>https://www.sublimetext.com</strong></a><a href="https://www.sublimetext.com/">)</a> is another good editor for PCs and Macs that automatically matches parentheses; this editor is not free, but can be evaluated for free.