# Task 4
## How to use and install the R package 
Here are the instructions of using and installing the R package.
(1) Install and load these two packages.
<pre>install.packages("Rcpp")
<pre>install.packages("devtools")
library(Rcpp)
library(devtools)
</pre>
(2) Install and load the R package that we have created.
<pre>install_local("stablemarriage2", force=TRUE)
library(stablemarriage2)</pre>
(3) Create two text file to store two preference table respectively. Put them in the same folder as the jupyter notebook file.
(4) Use the function in the R package to find a stable matching for these two preference tables. For example, if the preference tables are 
<pre>A c b d a
B b a c d
C b d a c
D c a d b</pre>
and
<pre>a A B D C
b C A D B
c C B D A
d B A C D</pre>
<pre>a = rcpp_stable_marriage("table1.txt", "table2.txt")
print(a)</pre>
Applying the function on them, you will get the result.
<pre> c   b   d   a 
"D" "C" "A" "B" </pre>

## A joke
Why don't scientists trust atoms?

Because they make up everything!
