
### **Galaxy pipeline for the identification of non-canonical ORFs and their potential biological function**

Cristobal Gallardo Alba

2023.07.06

---

### Index of contents

- Introduction
- Galaxy pipeline description
- Conclusion

---

<span class="menu-title" style="display: none">Introduction</span>

#### Introduction

#### What do we mean by *non-canonical ORFs*?

<img src="img/dark_proteome.png" alt="drawing" width="800"/>

Note:
nORFs are uncharacterized and unnanotated open-reading frames with functional relevance.

------

<span class="menu-title" style="display: none">Introduction</span>

#### Introduction

<p style="font-size:25px;">Mean Ribo-Seq expression and Ribo-Seq expression standard deviation (SD)</p>

<img src="img/expression_distribution.png" alt="drawing" width="600"/>
<p style="font-size:14px;"> Source: Erady, Chaitanya, et al. "Pan-cancer analysis of transcripts encoding novel open-reading frames (nORFs) and their potential biological functions." NPJ Genomic Medicine 6.1 (2021): 4.</p>

Note:
Canonical ORFs are depicted as blue dots and novel ORFs are depicted by orange dots. The black line shows the median expression SD of canonical ORFs. Not all nORFs have noisy expression values, many have similar SD vs. mean expression values as that of canonical ORFs (cORFs).

------

<span class="menu-title" style="display: none">Introduction</span>

#### Introduction

### Why study non-canonical ORFs?

<div class="r-stack">
<span class="fragment fade-out" data-fragment-index="0">

<div style="text-align:left; font-size:30px">

- Potentially novel prognostic and diagnostic markers
- The vast majority of non-canonical peptides have not been investigated
- Particulary attractive as allosteric celullar regulators

</div>

</span>
<span class="fragment current-visible" data-fragment-index="0">

<img src="img/non-canonical_nature.png" alt="drawing" width="1000"/>

</span>
</div>

------

#### Introduction

### Why have not been yet characterized?


<div style="text-align:left; font-size:30px">

- <span class="fragment highlight-current-red" style="font-size:30px">Arbitrary thresholds on ORF lengths</span>
- <span class="fragment highlight-current-red" style="font-size:30px">Annotated as noncoding RNAs or pseudogenes</span>
- <span class="fragment highlight-current-red" style="font-size:30px">Propensity for structural disorder</span>

</div>

------

#### Introduction

#### Why study intrinsically disordered proteins (IDP)?

<div class="r-stack">
<span class="fragment fade-out" data-fragment-index="0">
<img src="img/intrinsically_disordered.png" alt="drawing" width="600"/>
</span>
<span class="fragment current-visible" data-fragment-index="0">
<img src="img/disorder_protein.jpg" alt="drawing" width="1000"/>
</span>
</span>
<span class="fragment">
<span class="fragment" data-fragment-index="0">
Allostery mediated by IDPs ensures robust and efficient signal integration through <span class="fragment highlight-current-red"><b>mechanisms that would be extremely unfavorable or even impossible for globular protein interaction partners</b></span>.
<p><br><small><small>Berlow, R. B., Dyson, H. J., & Wright, P. E. (2018). Expanding the paradigm: intrinsically disordered proteins and allosteric regulation. Journal of molecular biology, 430(16), 2309-2320.</small></small></p></span>
</div>

------

<span class="menu-title" style="display: none">Introduction</span>

#### Introduction

### How identify non-canonical ORFs?


<div class="r-stack">
<span class="fragment fade-out" data-fragment-index="0">
<img src="img/scientist.jpg" alt="drawing" width="500"/>
</span>
<span class="fragment current-visible" data-fragment-index="0">
<img src="img/isoform_switching.png" alt="drawing" width="900"/>
</span>
</span>
<span class="fragment">
<img src="img/intro_results.png" alt="drawing" width="700"/>
</span>
</div>

---

### Galaxy pipeline decription


---

Thanks for you attention!
