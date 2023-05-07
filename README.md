Download Link: https://assignmentchef.com/product/solved-operating-system-homework-4
<br>
<h1>Part I</h1>

<ol>

 <li>A computer has four page frames. The time of loading, time of last access, and the <em>R </em>and <em>M </em>bits for each page are as shown below (the times are in clock ticks):</li>

</ol>

<table width="250">

 <tbody>

  <tr>

   <td width="50">Page</td>

   <td width="56">Loaded</td>

   <td width="96">Last Reference</td>

   <td width="48"><em>R M</em></td>

  </tr>

  <tr>

   <td width="50">0</td>

   <td width="56">126</td>

   <td width="96">279</td>

   <td width="48">0        0</td>

  </tr>

  <tr>

   <td width="50">1</td>

   <td width="56">230</td>

   <td width="96">260</td>

   <td width="48">1        0</td>

  </tr>

  <tr>

   <td width="50">2</td>

   <td width="56">120</td>

   <td width="96">272</td>

   <td width="48">1        1</td>

  </tr>

  <tr>

   <td width="50">3</td>

   <td width="56">160</td>

   <td width="96">280</td>

   <td width="48">1        1</td>

  </tr>

 </tbody>

</table>

<ul>

 <li>Which page will NRU replace?</li>

 <li>Which page will FIFO replace?</li>

 <li>Which page will LRU replace?</li>

 <li>Which page will second chance replace?</li>

</ul>

<ol start="2">

 <li>A small computer has 8 page frames, each containing a page. The page frames contain virtual pages <em>A</em>, <em>C</em>, <em>G</em>, <em>H</em>, <em>B</em>, <em>L</em>, <em>N</em>, and <em>D </em>in that order. Their respective load times were 18, 23, 5, 7, 32, 19, 3, and 8. Their reference bits are 1, 0, 1, 1, 0, 1, 1, and 0 and their modified bits are 1, 1, 1, 0, 0, 0, 1, and 1, respectively. Which page will the second chance page replacement algorithm replace?</li>

 <li>What is the difference between a physical address and a virtual address?</li>

 <li>Are there <em>any </em>circumstances in which clock and second chance choose different pages to replace? If so, what are they?</li>

 <li>A small computer has four page frames. At the first clock tick, the R bits are 0111 (page 0 is 0, the rest are 1). At subsequent clock ticks, the values are 1011, 1010, 1101, 0010, 1010, 1100, and 0001. If the aging algorithm is used with an 8-bit counter, give the values of the four counters after the last ticks.</li>

</ol>

<h1>Part II</h1>

This part requires that you write a memory manager in C. In other words, instead of wrappers as shown below

<ul>

 <li>#include &lt;stdlib.h&gt;</li>

 <li>#include “mm.h”</li>

</ul>

3

<ul>

 <li>void *mymalloc(size_t size)</li>

 <li>{</li>

 <li>return malloc(size);</li>

 <li>}</li>

</ul>

8

<ul>

 <li>void myfree(void *ptr)</li>

 <li>{</li>

 <li>free(ptr);</li>

 <li>}</li>

</ul>

13

<ul>

 <li>void *myrealloc(void *ptr, size_t size)</li>

 <li>{</li>

 <li>return realloc(ptr, size);</li>

 <li>}</li>

</ul>

18

<ul>

 <li>void *mycalloc(size_t nmemb, size_t size)</li>

 <li>{</li>

 <li>return calloc(nmemb, size);</li>

 <li>}</li>

</ul>

you are writing your own memory management functions, as follows:

1 #include “mm.h”

2

<ul>

 <li>void *mymalloc(size_t size)</li>

 <li>{</li>

 <li><em>// your own code</em></li>

 <li>}</li>

</ul>

7

<ul>

 <li>void myfree(void *ptr)</li>

 <li>{</li>

 <li><em>// your own code</em></li>

 <li>}</li>

</ul>

12

<ul>

 <li>void *myrealloc(void *ptr, size_t size)</li>

 <li>{</li>

 <li><em>// your own code</em></li>

 <li>}</li>

</ul>

17

<ul>

 <li>void *mycalloc(size_t nmemb, size_t size)</li>

 <li>{</li>

 <li><em>// your own code</em></li>

 <li>}</li>

</ul>

Note that mm.h is as given below.

1 #ifndef __MY_MM_H_INCLUDED__ 2 #define __MY_MM_H_INCLUDED__

3

4 #include &lt;stddef.h&gt;

5

<ul>

 <li>void *mymalloc(size_t size);</li>

 <li>void myfree(void *ptr);</li>

 <li>void *myrealloc(void *ptr, size_t size);</li>

 <li>void *mycalloc(size_t nmemb, size_t size);</li>

</ul>

10

11 #endif

For an example, please see pp. 185–189 of <em>The C Programming Language, Second Edition </em>by Kernighan and Ritchie, Prentice Hall, 1988.