java c
CS210 Fall   2024:   PS5A
Virtual Memory 
1.    (12 points)    Let   us   have   a   system   with   12-bit   virtual   addresses,   11-bit   physical   addresses,   and   a   page   of size   512 bytes.
(a)    (2 points)    How   many   bytes   of   data   can   virtual   memory   support?    
(b)    (2 points)    How   many   bytes   of   data   can   physical   memory   support?    
(c)    (2 points)    How   many   bits   is   the   offset   address?   
(d)    (2 points)    How   many   virtual   pages   are   there?   
(e)    (2 points)    How   many   physical   pages   are   there?   
(f)    (2 points)    How   many   entries   will   the   page   table   have?   
2.    (8 points)    Using   the      system   with   the   specifications   described   in   Question   1   and   the   following   table Translate   the   virtual   addresses   into   their   corresponding   physical   addresses   (in   hex).       Write    PAGE   FAULT, if needed.
(a)    (2 points)    Virtual   Address:   0xC00   (b)    (2 points)    Virtual   Address:   0x7A4   (c)    (2 points)    Virtual   Address:   0x49C   
(d)    (2 points)    Virtual   Address:   0xA00   Using   the   same   system   from   question   1, we   are   going   to   execute   3 instructions   sequentially.   The   original page table is given below.   Update the   page   table   to   have   the   correct   information   after   each   instruction   executes   (questions   3, 4,   5).Keep   the   following   in   mind:   Is   a   page   fault   needed?; Which   page   doI   evict?   (Note: in   the   LRU   column,   1 represents the most recently used page).   Make sure to update the   LRU   column   on   every   access;   Do   I   need   to   write   to   the   disk?]

3.      (8 points)      mov         [0x0f4],    rax
(a)    (2 points)    Page   Fault   needed?   
(b)    (2 points)    If   so, which   virtual   page   was   evicted?   
(c)    (2 points)    Which   physical   page   was   overwritten   by   the   page   fault?   
(d)    (2 points)    Was   a   write   to   the   disk   needed?   
Index 
R 
D 
PPN 
LRU 
0 




1 




2 




3 




4 




5 




6 




7 




4.      (8 points)      mov         [0x9a4],    rax
(a)    (2 points)    Page   Fault   needed?   
(b)    (2 points)    If   so, which   virtual   page   was   evicted?   
(c)    (2 points)    Which   physical   page   was   overwritten   by   the   page   fault?   
(d)    (2 points)    Was   a   write   to   the   disk   needed?   
Index 
R 
D 
PPN 
LRU 
0 




1 




2 




3 




4 




5 




6 




7 




5.      (8 points)      mov         [0xc44],    rax
(a)    (2 points)    Page   Fault   needed?   
(b)    (2 points)    If   so, which   virtual   page   was   evicted?   
(c)    (2 points)    Which   phys代 写CS210 Fall 2024: PS5AMatlab
代做程序编程语言ical   page   was   overwritten   by   the   page   fault?   
(d)    (2 points)    Was   a   write   to   the   disk   needed?   
Index 
R 
D 
PPN 
LRU 
0 




1 




2 




3 




4 




5 




6 




7 




Caching 
6.    We   have   the   following   2-way   set-associative   cache   containing   8 sets,with   a   block   size   of   2 64-bit   words.   The cache uses a LRU replacement strategy.   At a particular point   during   execution,   a   snapshot is   taken   of the   cache   contents,   which   are   shown   below.    All   values   are   in   hex;   assume   that   any   hex   digits   not   shown   are   0.
The   cache   uses   bits   from   the   64-bit   byte   address   produced   by   the   CPU   to   select   appropriate   set   (L),   and   input   to   the   tag   comparisons   (T)   and   to   select   the   appropriate   word   from   the   data   block   (B).   For   correct   and   optimal   performance   what   are   the   appropriate   portions   of   the   address   to   use   forL, T, and   B?   Express   your   answer   in   the   form. “A[N:M]” for   N   and   M   in   the   range   0 to   63, or   write “CAN’T   TELL”   .
(a)    (1 point)    Address   bits   to   use   for   B:   
(b)    (1 point)    Address   bits   to   use   for   L:   
(c)    (1 point)    Address   bits   to   use   for   T:   For   the   following   addresses,   if   the   contents   of   the   specified   location   appear   in   the   cache,   give   the   location’s   64-bit   contents   in   hex   (determined   by   using   the   appropriate   value   from   the   cache).      If the   contents   of   the   specified   location   are   NOT   in   the   cache, write   “MISS”   .
(a)    (1 point)    Contents   of   the   location   0x128   (in   hex):    
(b)    (1 point)    Contents   of   the   location   0xDB0   (in   hex):   
(c)    (1 point)    Contents   of   the   location   0x3BF70 (in   hex):   
Pipelining 
7.    (10 points)    Consider   the   following   combinational   logic   circuit   constructed   from      6   modules.      In   the diagram below,   each   combinational   component   is   marked   with   its propagation   delay   in   seconds;   con-   tamination delays are zero for each   component.

(a)    (2 points)    What   is   the   latency   of   this   combinational   circuit?   
(b)    (2 points)    What   is   the   throughput   of   this   combinational   circuit?    
(c)    (2 points)    Draw   the   smallest   number   of   ideal   (zero   delay,   zero   setup/hold   time)   pipeline   registers on   the   circuit   diagram below   so   as   to   maximize   its   throughput.    Remember to place   a register   on   the output.

(d)    (2 points)    What   is   the   latency   of   the   pipelined   circuit?   
(e)    (2 points)    What   is   the   throughput   of   the   pipelined   circuit?    





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
