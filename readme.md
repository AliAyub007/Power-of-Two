# Power of 2

Calculate how many power of 2 have to sum up to make the number in input.

ANSWER:

(define powers-of-two<br/>
&emsp;(lambda (x)<br/>
&emsp;&emsp;(powers-of-two-rec x 0)<br/>
&emsp;)<br/>
)<br/>

(define powers-of-two-rec<br/>
&emsp;(lambda (x pow)<br/>
&emsp;&emsp;(if (>= 0 x)<br/>
&emsp;&emsp;&emsp; (list )<br/>
&emsp;&emsp;&emsp; (if (>= x (expt 2 pow))<br/>
&emsp;&emsp;&emsp;&emsp;  (powers-of-two-rec x (+ 1 pow))<br/>
&emsp;&emsp;&emsp;&emsp;  (cons (expt 2 (- pow 1))<br/> (powers-of-two-rec (- x (expt 2 (- pow 1))) 0))<br/>
&emsp;&emsp;&emsp;&emsp;  )<br/>
&emsp;&emsp;&emsp; )<br/>
&emsp;&emsp;)<br/>
)<br/>

(powers-of-two 0); → ()<br/>
(powers-of-two 1); → (1)<br/>
(powers-of-two 26); → (16 8 2)<br/>
(powers-of-two 45); → (32 8 4 1)<br/>