
### **Galaxy pipeline for the identification of non-canonical ORFs and their potential biological function**

Cristobal Gallardo Alba

2023.07.06

---

### Index of contents

- <span class="fragment highlight-current-red">1. Introduction</span>
- 2. Galaxy workflow
- 3. Preliminary results

---

<span class="menu-title" style="display: none">Introduction</span>

<div style="text-align:left; font-size:40px"><br>

### 1. Introduction

- <span class="fragment highlight-current-red">1.1. What do we mean by *non-canonical ORFs*?</span>

- 1.2. Why study non-canonical ORFs?

- 1.3. Why have not been yet characterized?

- 1.4. How identify non-canonical ORFs?

</div>

------

<span class="menu-title" style="display: none"> What do we mean by non-canonical ORFs?</span>

#### What do we mean by *non-canonical ORFs*?

<div class="r-stack">
<span class="fragment fade-out" data-fragment-index="0">


<img src="img/expression_distribution.png" alt="drawing" width="600"/>
<p  style="font-size:20px">Mean Ribo-Seq expression and Ribo-Seq expression standard deviation (SD). </p>
<p style="font-size:14px;">Source: Erady, Chaitanya, et al. "Pan-cancer analysis of transcripts encoding novel open-reading frames (nORFs) and their potential biological functions." NPJ Genomic Medicine 6.1 (2021): 4.</p>

</span>
<span class="fragment current-visible" data-fragment-index="0">

<img src="img/dark_proteome.png" alt="drawing" width="1000"/>

</span>
</div>


Note:
nORFs are uncharacterized and unnanotated open-reading frames with functional relevance.


------

<div style="text-align:left; font-size:40px"><br>

### 1. Introduction

- 1.1. What do we mean by *non-canonical ORFs*?

- <span class="fragment highlight-current-red">1.2. Why study non-canonical ORFs?</span>

- 1.3. Why have not been yet characterized?

- 1.4. How identify non-canonical ORFs?

</div>

------

<span class="menu-title" style="display: none">Why study non-canonical ORFs?</span>

<span  style="text-align:left">

### Why study non-canonical ORFs?

</span>

<div class="r-stack">
<span class="fragment fade-out" data-fragment-index="0">


<div style="text-align:left; font-size:35px">

- Potentially novel <b>prognostic and diagnostic markers</b>

- The vast majority <b>have not been investigated</b>

- Particulary attractive as <b>allosteric celullar regulators</b>

</div>

</span>
<span class="fragment current-visible" data-fragment-index="0">

<img src="img/non-canonical_nature.png" alt="drawing" width="800"/>

</span>
</div>

------

<div style="text-align:left; font-size:40px"><br>

### 1. Introduction

- 1.1. What do we mean by *non-canonical ORFs*?

- 1.2. Why study non-canonical ORFs?

- <span class="fragment highlight-current-red">1.3. Why have not been yet characterized?</span>

- 1.4. How identify non-canonical ORFs?

</div>

------

<span class="menu-title" style="display: none">Why have not been characterized?</span>

<span  style="text-align:left">

### Why have not been characterized?

<br>

</span>

<div style="text-align:left; font-size:30px">

- <span class="fragment highlight-current-red" style="font-size:30px">Arbitrary thresholds on ORF lengths</span>
    - <span class="fragment highlight-current-red" style="font-size:30px">Peptides smaller than 100 aminoacids are usually discarted</span>

- Frequently annotated as non-coding RNAs

- Propensity for structural disorder
    -  Discarted as intrinsically disordered proteins (IDPs)

</div>


------

<span class="menu-title" style="display: none">Why study small peptides?</span>

### Why study small peptides?

<div class="r-stack">
<span class="fragment fade-out" data-fragment-index="0">
<img src="img/small_peptides.png" alt="drawing"/>
</span>
<span class="fragment" data-fragment-index="0">
<img src="img/small_peptides_examples.png" alt="drawing"  width="600"/>
<p  style="font-size:20px">Example: In eukaryotes, small proteins upregulate proteases and chaperones and downregulate protein synthesis when cells encounter ER stress. </p>
<p style="font-size:14px">Source: Steinberg, R., & Koch, H. G. (2021). The largely unexplored biology of small proteins in pro- and eukaryotes. The FEBS journal, 288(24), 7002-7024.</p>
</span>
</div>

------

<span  style="text-align:left">

### Why have not been characterized?

<br>

</span>

<div style="text-align:left; font-size:30px">

- Arbitrary thresholds on ORF lengths
    - Peptides smaller than 100 aminoacids are usually discarted

- <span class="fragment highlight-current-red" style="font-size:30px">Frequently annotated as non-coding RNAs</span>

- Propensity for structural disorder
    -  Discarted as intrinsically disordered proteins (IDPs)

</div>

------

<span class="menu-title" style="display: none">Annotated as non-coding RNAs?</span>

#### Annotated as non-coding RNAs?

<div class="r-stack">
<span class="fragment fade-out" data-fragment-index="0">
<img src="img/question.jpg" alt="drawing" width="800"/>
</span>
<span class="fragment current-visible" data-fragment-index="0">
<img src="img/small_non_coding.png" alt="drawing" width="900"/>
</span>
</span>
<span class="fragment">
<img src="img/spencer_datase.png" alt="drawing" width="1000"/>
</span>


------

<span  style="text-align:left">

### Why have not been characterized?

<br>

</span>

<div style="text-align:left; font-size:30px">

- Arbitrary thresholds on ORF lengths
    - Peptides smaller than 100 aminoacids are usually discarted

- Frequently annotated as non-coding RNAs

- <span class="fragment highlight-current-red" style="font-size:30px">Propensity for structural disorder</span>
    -  <span class="fragment highlight-current-red" style="font-size:30px">Discarted as intrinsically disordered proteins (IDPs)</span> 

</div>

------

<span class="menu-title" style="display: none">Why study intrinsically disordered proteins (IDP)?</span>


#### Why study intrinsically disordered proteins (IDP)?

<div class="r-stack">
<span class="fragment fade-out" data-fragment-index="0">
<img src="img/disordered_regions.png" alt="drawing" width="600"/>
<p style="font-size:14px;">Source: Babu, M. M., Kriwacki, R. W., & Pappu, R. V. (2012). Versatility from protein disorder. Science, 337(6101), 1460-1461.</p>
</span>
<span class="fragment current-visible" data-fragment-index="0">
<b>Disorder-Function Paradigm</b>
<img src="img/disorder_article.png" alt="drawing" width="1000"/>
</span>
</span>
<span class="fragment current-visible" data-fragment-index="1">
<img src="img/intrinsically_disordered.png" alt="drawing" width="700"/>
</span>
<span class="fragment current-visible" data-fragment-index="2">
<img src="img/disorder_protein.jpg" alt="drawing" width="1000"/>
<p style="font-size:14px;">Source: Chakrabarti, P., & Chakravarty, D. (2022). Intrinsically disordered proteins/regions and insight into their biomolecular interactions. Biophysical Chemistry, 283, 106769.</p>
</span>

------

<div style="text-align:left; font-size:40px"><br>

### 1. Introduction

- 1.1. What do we mean by *non-canonical ORFs*?

- 1.2. Why study non-canonical ORFs?

- 1.3. Why have not been yet characterized?

- <span class="fragment highlight-current-red">1.4. How identify non-canonical ORFs?</span>

</div>

------

<span class="menu-title" style="display: none">How identify non-canonical ORFs?</span>

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
<img src="img/isoform_switching.jpg" alt="drawing" width="600"/>
</span>
</div>

---

### Index of contents

- 1. Introduction
- <span class="fragment highlight-current-red">2. Galaxy workflow</span>
- 3. Preliminary results

------

<span class="menu-title" style="display: none">Galaxy Workflow</span>

#### Galaxy Workflow

<div class="r-stack">
<span class="fragment fade-out" data-fragment-index="0">
<img src="img/galaxy_training.png" alt="drawing" width="700"/>
<p  style="font-size:20px">Full detailed explanation in the <a href="https://gxy.io/GTN:T00345">Genome-wide alternative splicing analysis</a> Galaxy training. </p>
</span>
<span class="fragment current-visible" data-fragment-index="0">
<img src="img/full_workflow.png" alt="drawing" width="1000"/>
<p  style="font-size:20px">Full detailed explanation in the <a href="https://gxy.io/GTN:T00345">Genome-wide alternative splicing analysis</a> Galaxy training. </p>
</span>
</span>
<span class="fragment current-visible" data-fragment-index="1">
<img src="img/simple_workflow.png" alt="drawing" width="700"/>
<p  style="font-size:20px">Full detailed explanation in the <a href="https://gxy.io/GTN:T00345">Genome-wide alternative splicing analysis</a> Galaxy training. </p>
</span>
<span class="fragment current-visible" data-fragment-index="2">

### Initial QC assessment

<img src="img/initial_QC.png" alt="drawing" width="600"/>
<p style="font-size:14px;">Identify potential artifacts that may impact the interpretation of downstream analysis.</p>
</span>
<span class="fragment current-visible" data-fragment-index="3">

#### Mapping and identication of novel splicing sites with RNASTAR

<img src="img/STAR_pipeline.png" alt="drawing" width="900"/>
<p style="font-size:14px;">Two-pass alignment enables sequence reads to span novel splice junctions by fewer nucleotides, conferring greater read depth and providing significantly more accurate quantification of novel splice junctions.</p>
</span>
<span class="fragment current-visible" data-fragment-index="5">

#### Post-mapping QC assessment with RSeQC

<img src="img/rseqc_junction_saturation_plot.png" alt="drawing" width="800"/>
<p style="font-size:18px;"> RSeQC is a toolkit for generating RNA-seq-specific quality control metrics. The figure corresponds to RSeQC junction saturation of known (A) and novel (B) splicing sites.</p>
</span>
<span class="fragment current-visible" data-fragment-index="6">

#### Reference-based transcriptome assembly and quantification with StringTie

<img src="img/stringtie_pipeline.png" alt="drawing" width="1000"/>
<p style="font-size:14px;">StringTie is a fast and highly efficient assembler of RNA-seq alignments into potential transcripts.</p>
</span>
<span class="fragment current-visible" data-fragment-index="7">

#### Post-assembly QC assessment with rnaQUAST

<img src="img/rnaQUAST_cumulative_isoform.png" alt="drawing" width="500"/>
<p style="font-size:14px;">rnaQUAST, which will provide us diverse completeness/correctness statistics very useful in order to identify and address potential errors or gaps in the assembly process. The figure is a rnaQUAST cummulative isoform plot.</p>
</span>
<span class="fragment current-visible" data-fragment-index="8">

#### Isoform switching and functional analysis with IsoformSwitchAnalyzeR

<img src="img/isoformswitch_pipeline.png" alt="drawing" width="1000"/>
<p style="font-size:14px;">IsoformSwitchAnalyzieR performs the differential isoform usage analysis by using DEXSeq.</p>
</span>
<span class="fragment current-visible" data-fragment-index="9">

#### Isoform switching and functional analysis with IsoformSwitchAnalyzeR

<img src="img/consequences_plot.png" alt="drawing" width="500"/>
<p style="font-size:14px;">To analyze large-scale patterns in predicted IS consequences, IsoformSwitchAnalyzeR computes all isoform switching events resulting in a gain/loss of a specific consequence (e.g. protein domain gain/loss).</p>
</span>

---

### Index of contents

- 1. Introduction
- 2. Galaxy workflow
- <span class="fragment highlight-current-red">3. Preliminary results</span>

------

<span class="menu-title" style="display: none">Preliminary results</span>


#### Preliminary results

<div class="r-stack">
<span class="fragment fade-out" data-fragment-index="0">
<img src="img/FBXO4.png" alt="drawing" width="700"/>
<p style="font-size:14px;">The complete analysis can be found in this <a href="https://usegalaxy.eu/u/gallardoalba/h/genome-wide-splicing-history">Galaxy history</a>.</p>
</span>
<span class="fragment" data-fragment-index="0">
<img src="img/fbxo4_information.png" alt="drawing" width="700"/>
<p style="font-size:14px;">The complete analysis can be found in this <a href="https://usegalaxy.eu/u/gallardoalba/h/genome-wide-splicing-history">Galaxy history</a>.</p>
</span>
</div>

---

<img src="img/closing_image.png" alt="drawing" width="700"/>

Thanks for you attention!
