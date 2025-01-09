java c
Optimization   and   Algorithms 
November   17,   2022 
Exam: Part A
1. Positioning   without   covering   a   set.    Consider   the   set
S   =   {x =   (x1   , . . . ,   xn)   ∈ Rn   :      - 1   ≤ xi      ≤ 1,    for      1   ≤ i   ≤ n} .
(In   dimension   n =   2,   the   set   S   looks   like   a   ﬁlled   square.)
We   want   to   position   a   ball
B(c)   =   {x   ∈ Rn   :      Ⅱx - cⅡ2    ≤   r}
such   that   the   center   c   of   the   ball   is   as   close   as   possible   to   a   given   point   d   ∈   Rn   and   such   that   the   ball   does   not   cover   the   set      S      (that   is,   we   do   not   want   to   have   S   ≤ B(c)).   The   radius   r   > 0   of the   ball   is   given   and   cannot   be   changed.
For   future   reference,   let   V   C Rn    be   the   set   of   vectors   of   size   n   whose   components   are   either   1   or   -1.   For   example,   in   dimension   n = 2,   we   have


Note that,   for   n = 2,   the   set   V   is the   set   of vertices   of   the   square   S.    (For   general   n,   the   set   V   has   2n      elements.)
Consider   the   following   optimization   problems.

One   of these   optimization   is   suitable   for   the   given   context.
Which   one?
Write your answer (A, B, C, D, E, or F) in the box at the top of page 1
Hint:   think   about   this   problem   in   dimension   n = 2.
2. Unconstrained   optimization.    Consider   the   optimization   problem

where

The   point

is   a   global   minimizer   of   (7)   for   one   of the   following   choices   of   d:

Which   one?
Write your answer (A, B, C, D, E, or F) in the box at the top of page 1
3. Least-squares.    Let   A   ∈ Rm×n      and   b   ∈ Rm      be   given,   with   n   being   an   even   number,   and   consider   the   following   optimization   problems:

where rev   : Rn   → Rn   is the map that returns the input written in reverse   order   (that   is,   written   from   the   last   component   to   the   ﬁrst   component).    Examples   (for   n   = 4):

where   sort   : Rn    → Rn    is   the   map   that   returns   the   input   sorted   in   ascending   order.   Examples   (for   n = 4):

where      circ   : Rn    → Rn    is   the    map   that    returns   the   input   circulated   by   one   component    (that   is,      the   ﬁrst   component   of   the   input      x   becomes   the   second   component   of the   output,   the   second   component   of   x   becomes   the   third   com-   ponent of the output,   and so   on,   and the   last   component   of   x   becomes   the   ﬁrst   component   of the   output).   Examples   (for   n = 4):

where      cent   : Rn      → Rn    is    the   map   that   shifts   the   input   so   that   it   becomes   centered   at   the   origin;      more   precisely,      given   the   input      x,   the   map   subtracts   from   x the   average   of the   components   of x.    Examples   (for   n = 4):

where   trim   : Rn      → Rn    is   the   map   that   trims   one   component   at   the   beginning   and   at   the   end   of   the   input;      that   is,      given   the   input      x,   the   map   zeroes   the   ﬁrst   and   last   components of x, while keeping   the   other   components   of x   intact.   Examples   (for   n =   4):

where   swap   : Rn   → Rn    is   the   map   that   swaps   each   consecutive   pair   of compo-   nents   of   x   (that   is, given   x   =   (x1   ,   x2   , . . . ,   xn), it   swaps   x1      with   x2   ,   thenx3    with x4   ,   and   so   on,   until   xn-1      with   xn).   Examples   (for   n = 4):
                
One   of the   above   problems   is not a   least-squares   problem.   Which   one?
Write your answer (A, B, C, D, E, or F代 写Optimization and Algorithms 2022 Exam
代做程序编程语言) in the box at the top of page 1
4. Newton   algorithm.      Consider the Newton algorithm with the generic update equation   given   by
x   k+1   = x   k   + Qkdk   ,                                                                                                                                                (8)
where   Qk    denotes   the   stepsize.
Suppose   that   the   Newton   algorithm   is   applied   to   the   function   f   : R2   → R,
f   (a,   b)   =   (2a - b)2   + b2,
and   suppose   that   the   current   iterate   is

One   of the   following   vectors   is   then   the   vector   dk    in   (8).

Which   one?
Write your answer (A, B, C, D, E, or F) in the box at the top of page 1
Exam: Part B
1. Convex   problem.    Show   that   the   following   problem   is   convex,

where   the   vectors   ak         ∈ Rn       (for      1    ≤   k    ≤   K)    and   c   ∈ Rn.       The      numbers    bk         (for 1   ≤ k   ≤ K),   λ > 0,   r   >   0,   and   P   >   0   are   also   given.
The   function   φ   : R → R is   deﬁned   as

The   function   ψ   : R → R is   deﬁned   as

2. Equivalent   problems?         Bob   wants   to   compute   a   point   in   the   hyperplane   H(s,   r)   =   {x ∈ Rn   :   sT   x   = r   }   that   is   closest   to   given   points   pk ∈ Rn   ,   for      1 ≤ k ≤ K,   in   the mean   squared-distance   sense.    That   is,   Bob   wants   to   ﬁnd   a   global   minimizer   of the   problem

Alice   claims   that   this   problem   is   equivalent   to   compute   a   point   in   the   hyperplane   H(s,   r) that is closest to the   center-of-mass   of the   points pk,   for   1   ≤ k   ≤ K.    That is,   Alice   claims that the   global   minimizers   of   (2)   are the   same   as the   global   minimizers   of

Is      Alice      correct      or   wrong?       If   you    think    Alice      is      wrong,    then      provide      a      counter-   example:   that   is,   provide   an   hyperplane   H(s,   r)   and   points p1   , . . . ,   pK      such that the   global minimizers of   (2)   and   (3)   are not the   same.    If you think   Alice   is   correct,   then   prove   that   the   global   minimizers   of      (2)   and      (3)   are   the   same      (for   any   hyperplane   H(s,   r)   and   points   p1   , . . .   ,   pK   ).
3. Distance   between   two   parallel   hyperplanes.    Consider   two   parallel   hyperplanes   in Rn   given   by
H1   =   {x ∈ Rn   :   sT   x   =   r1   } ,    and   H2    =   {x ∈ Rn   :   sT   x   =   r2   } ,
where   s is a nonzero vector in Rn   ,   andr1    andr2    are two distinct   numbers   (r1  r2   ).   We   wish   to   ﬁnd   the   distance   between   these   two   hyperplanes.   That   is,   denoting   this   distance   by   d (H1,   H2   ),   we   wish   to   compute
d (H1,   H2   )   =   inf {Ⅱx1    - x2 Ⅱ2    :   x1    ∈ H1,   x2    ∈ H2} .                                                                      (4)
Give   a   closed-form   expression   for   the   distance   d (H1,   H2   )   in   terms   of   s,   r1   ,   and   r2   .   Hint:   use   KKT   conditions   on   the   problem   (4).4. Dead-zone   quadratic penalty.   The dead-zone quadratic penalty function with bandwidth B   > 0   is   the   function   φ   : Rn   → R deﬁned   asφB (x)   =   (ⅡxⅡ2   - B) .   Let   H(s,   r)   be   a   given   hyperplaneH(s,   r) ={x ∈ Rn   :   sT   x   =   r   }   ,with   s   ∈ Rn      and   r   ∈ R.Give   a   closed-form   expression   for   a   global   minimizer   of the   problemwhere      c      ∈ Rn         and      B      >    0    are      given.          Assume      that      c      is      not      in      the      hyperplane (c   ∈/ H(s,   r))   and   that   s   is   a   nonzero   vector   (s ≠   0).

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
