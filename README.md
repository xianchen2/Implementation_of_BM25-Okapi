
# Implementation of BM25 Okapi
Python implementation of the [BM25](https://en.wikipedia.org/wiki/Okapi_BM25) for file retrieval

Given a query Q, containing keywords ```q1,...,qn```, BM25 score of a document is 

<a href="https://www.codecogs.com/eqnedit.php?latex={\text{score}}(D,Q)=\sum&space;_{i=1}^{n}{\text{IDF}}(q_{i})\cdot&space;{\frac&space;{f(q_{i},D)\cdot&space;(k_{1}&plus;1)}{f(q_{i},D)&plus;k_{1}\cdot&space;\left(1-b&plus;b\cdot&space;{\frac&space;{|D|}{\text{avgdl}}}\right)}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?{\text{score}}(D,Q)=\sum&space;_{i=1}^{n}{\text{IDF}}(q_{i})\cdot&space;{\frac&space;{f(q_{i},D)\cdot&space;(k_{1}&plus;1)}{f(q_{i},D)&plus;k_{1}\cdot&space;\left(1-b&plus;b\cdot&space;{\frac&space;{|D|}{\text{avgdl}}}\right)}}" title="{\text{score}}(D,Q)=\sum _{i=1}^{n}{\text{IDF}}(q_{i})\cdot {\frac {f(q_{i},D)\cdot (k_{1}+1)}{f(q_{i},D)+k_{1}\cdot \left(1-b+b\cdot {\frac {|D|}{\text{avgdl}}}\right)}}" /></a>

where the inverse document frequency weight of the query term ```qi``` is computed as:   <a href="https://www.codecogs.com/gif.latex?\\text{IDF}(q_i)&space;=&space;\log&space;\frac{N&space;-&space;n(q_i)&space;&plus;&space;0.5}{n(q_i)&space;&plus;&space;0.5}," target="_blank"><img src="https://latex.codecogs.com/gif.latex?\text{IDF}(q_i)&space;=&space;\log&space;\frac{N&space;-&space;n(q_i)&space;&plus;&space;0.5}{n(q_i)&space;&plus;&space;0.5}," title="\text{IDF}(q_i) = \log \frac{N - n(q_i) + 0.5}{n(q_i) + 0.5}," /></a>
