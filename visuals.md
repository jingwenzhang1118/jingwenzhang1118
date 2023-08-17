---

layout: page
title: Data Visualization

---

<link rel="stylesheet" href="/assets/css/res.css">


Drawing graphs is of great importance for exploring data structure, identifying trends and clusters, detecting unusual data points and presenting results. Figures can quickly communicate a significant amount of information. It is without a doubt that **a good graph is worth a thousand words**. 

Here I display some dynamic figures I draw using Python. In particular, I will use these figures to explore the trend of CSR performance, and its association with some firm characteristics. The CSR ratings of US companies are collected from KLD database for the period from 2004 to 2018. 
<br>
<hr>


<h3 class="fighd">CSR Performance over time by Gender</h3>

- The folllowing suggests that CSR performance of firms has improved over time. 

<div class="custom-video">
      <div class="custom-video__container">
        <video class="custom-video__video" weight="auto" height="100%" muted autoplay>
          <source src="/images/avgcsr.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <div class="custom-video__control">▶</div>
    </div>
</div>
<hr>


<h3 class="fighd">CSR Performance over time by Industry</h3>

- The plots below show that CSR performance of all industries enhanced over time. 
- A deeper exploration shows that some industries often outperformed the average performance of all US compaies (left figure), while the others stayed below the average (rigth figure).

<div class="custom-video">
      <div class="custom-video__container">
        <video class="custom-video__video" width="auto" height="100%" muted autoplay>
          <source src="/images/avgcsr_ind.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <div class="custom-video__control">▶</div>
    </div>
</div>
<br>
<hr>


<h3 class="fighd">CSR Performance over time by Gender</h3>

- Many literature document that females and males make decisions differently due to their differences in characteristics. 
- Here I show that firms run by female CEOs on average have better CSR performance than firms run by male CEOs. 
- However, the differences reduced over time, as the CSR performance under the operation of male CEOs kept increasing. 

<div class="custom-video">
      <div class="custom-video__container">
        <video class="custom-video__video" width="auto" height="100%" muted autoplay>
          <source src="/images/avgcsr_gender.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <div class="custom-video__control">▶</div>
    </div>
</div>
<hr>


<h3 class="fighd">CSR Performance and Firm Size</h3> 

- Large firms are expected to have more resources to invest in CSR activities, which should lead to greater CSR performance (CSR ratings). 
- The left figure plots the linear relationship between CSR performance and firm size(measured by the logarithm of a firm's assets) each year. The scatters show part of the data used for the linear regression. As expected, there is a positive assocation between CSR and firm size. Interestingly, the association becomes greater in more recent years. 
- The right bar chart displays the coefficients of firm size by year. Clearly, the coefficients, indicative of the association between CSR and firm size, are larger in recent years. 

<div class="custom-video">
      <div class="custom-video__container">
        <video class="custom-video__video" width="auto" height="100%" muted autoplay>
          <source src="/images/avgcsr_ols.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <div class="custom-video__control">▶</div>
    </div>
</div>
<br>
<hr>


<h3 class="fighd">You can find the related codes below:</h3>

- Codes for <a href="https://github.com/jingwenzhang1118/jingwenzhang1118.github.io/blob/656d780e02a5618939aa4888a4b34e3ed38b275c/visuals_prep.ipynb" target="_blank">cleaning and restructuring the data</a>.
- Codes for <a href="https://github.com/jingwenzhang1118/jingwenzhang1118.github.io/blob/656d780e02a5618939aa4888a4b34e3ed38b275c/visuals.ipynb" target="_blank">making the dynamic figures</a>. 


<script src="/assets/css/videoscript.js"></script>


