#HSLIDE
### Politecnico di Milano
#### 30.01.2017

#HSLIDE
### VLDB 2016's two paper report
#### Lodi Luca

#HSLIDE
## Selected papers

#VSLIDE
** Effective Indexing for Approximate Constrained Shortest Path Queries on Large Road Networks **

#VSLIDE
** DOCS: Domain-Aware Crowdsourcing System **

#VSLIDE
[Effective Indexing for Approximate Constrained Shortest Path Queries on Large Road Networks - .pdf](http://www.vldb.org/pvldb/vol10/p61-wang.pdf)


#VSLIDE
[DOCS: Domain-Aware Crowdsourcing System - .pdf](http://www.vldb.org/pvldb/vol10/p361-zheng.pdf)

#HSLIDE
### Effective Indexing for Approximate Constrained Shortest Path Queries on Large Road Networks

#HSLIDE
# Who ?

#VSLIDE
- Sibo Wang
  (Nanyang Technological University)
- Xiaokui Xiao
  (Nanyang Technological University)
- Yin Yang
  (Hamad Bin Khalifa University)
- Wenqing Lin
  (Qatar Computing Research Institute)

#HSLIDE
# What ?

#VSLIDE
## CSP query
[**C**onstrainted **S**hortest **P**ath]<br>

Find path between two nodes that:
- satify a **constraint on cost**
- **minimize length** of path

#VSLIDE
## CSP is NP-HARD

#VSLIDE
## Approximate CSP (&Alpha;-CSP)
existing methods are still **prohibitively expensive** on **large Roads Network** (RN).

#VSLIDE
fail to utilize the **special properties of road networks**

#VSLIDE
process queries **without indices** / few existing indices consume **large amounts of memory** in comparison to the limited benefit

#VSLIDE
## COLA
the **first practical solution** for approximate CSP processing on **large road networks**

#VSLIDE
![idea](idea.jpg)
<br>
 **road network can be effectively partitioned**

#VSLIDE
![idea](idea.jpg)
<br>
there exists a **relatively small set of landmark vertices**
that commonly **appear in CSP results**

#VSLIDE
![idea](idea.jpg)
<br>
Accordingly **indexes the vertices** lying on **partition boundaries**

#VSLIDE
![idea](idea.jpg)
<br>
on-the-fly algorithm called **α-Dijk for path computation within a partition**, which **effectively prunes paths** based on landmarks


#VSLIDE
![results](fantozzi.jpg)
<br>
On **continent-sized road networks**, COLA answers an approximate CSP query in sub-second time, existing methods can take hours.

#VSLIDE
![results](fantozzi.jpg)
<br>
**Without an index**, the **α-Dijk algorithm** in COLA still **outperforms**
previous solutions by **more than an order of magnitude**.

#HSLIDE
# Why ?

#VSLIDE
## How to deal with multiple criteria on SP ?

#VSLIDE
![results](gmap.jpg)
<br>

#VSLIDE
## Show multiple path, let the user choose
(Not so efficient)

#VSLIDE
![results](toll1.jpg)
<br>

#VSLIDE
![results](toll2.jpg)
<br>

#VSLIDE
![results](toll3.jpg)
<br>

#VSLIDE
![results](ny_left.jpg)
<br>

#VSLIDE
![idea](idea.jpg)
<br>
Use **CSP to efficiently solve two-criteria** SP. <br>
(still **challenging**)

#VSLIDE
Railroads applications
<br>
![results](rail.jpg)


#VSLIDE
![results](tank.jpg)
<br>
Military applications

#HSLIDE
# State of art

#VSLIDE
![results](wrong.png)
### Aim to solve general 	&Alpha;-CSP
(no exploitation of graph properties)

#VSLIDE
![results](wrong.png)
### None or poor use of indexing
(Few existing indexes are **thought for exact CSP**, thus **memory intensive** without any practical result)


#HSLIDE
# How ?
### (Quo modo ?)

#HSLIDE
# How ?
### (Quibus auxiliis ?)

#HSLIDE
# How much ?
#VSLIDE


#HSLIDE
