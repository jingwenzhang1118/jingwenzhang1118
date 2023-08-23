---

layout: page
title: Data Visualization

---

<link rel="stylesheet" href="/assets/css/res.css">


Drawing graphs is of great importance for exploring data structure, identifying trends and clusters, detecting unusual data points and presenting results. Figures can quickly communicate a significant amount of information. It is without a doubt that **a good graph is worth a thousand words**. 

Here I display some dynamic figures I draw using Python. In particular, I use these figures to explore the **trend of CSR performance of US companies**, and **its association with some firm characteristics**. The CSR ratings of US companies are collected from KLD database for the period from 2004 to 2018. 
<br>
<hr>


<h3 class="fighd">CSR Performance over time</h3>

- The folllowing figure suggests that CSR performance of firms has improved over time. 

<div class="custom-video">
      <div class="custom-video__container">
        <video class="custom-video__video" weight="auto" height="90%" muted autoplay>
          <source src="/images/avgcsr.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <div class="custom-video__control">▶</div>
    </div>
</div>
<hr>


<h3 class="fighd">CSR Performance over time by Industry</h3>

- The plots below show that CSR performance of all industries enhanced over time. 
- A deeper exploration shows that some industries often outperformed the average performance of all the US compaies (left figure), while the other industries mostly performed below the average (rigth figure). The grey area represents the average CSR performance of all the US companies. 

<div class="custom-video">
      <div class="custom-video__container">
        <video class="custom-video__video" width="100%" height="auto" muted autoplay>
          <source src="/images/avgcsr_ind.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <div class="custom-video__control">▶</div>
    </div>
</div>
<br>
<hr>


<h3 class="fighd">CSR Performance over time by Gender</h3>

- Many literature document that females and males make decisions differently due to their differences in characteristics. Some papers suggest that females are likely more socially responsible. 
- Here I show that firms run by female CEOs on average have better CSR performance than firms run by male CEOs. 
- However, the differences reduced over time, as the CSR performance of firms with male CEOs kept increasing. 

<div class="custom-video">
      <div class="custom-video__container">
        <video class="custom-video__video" width="auto" height="90%" muted autoplay>
          <source src="/images/avgcsr_gender.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <div class="custom-video__control">▶</div>
    </div>
</div>
<hr>


<h3 class="fighd">CSR Performance and Firm Size</h3> 

- Large firms are expected to have more resources to invest in CSR activities, which should lead to greater CSR performance (CSR ratings). 
- The left figure plots the linear relationship between CSR performance and firm size each year, in which firm size is measured by the logarithm of firms' total assets. For clarity, the scatter plot only shows part of the data used for each linear regression. 
- As shown in the left figure, there is a positive assocation between CSR and firm size. Interestingly, the slope of the line increases over years, meaning that the association between CSR performance and size becomes greater in more recent years. 
- The right bar chart displays the coefficients of firm size by year. Clearly, the coefficients, indicative of the association between CSR and firm size, are larger in recent years. 


<div class="custom-video">
      <div class="custom-video__container">
        <video class="custom-video__video" width="100%" height="auto" muted autoplay>
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



<script>
    // Adding functinality to video play and pause button
    const video = document.getElementsByClassName("custom-video__video");
    let i;
    for (i = 0; i < video.length; i++) {
    video[i].addEventListener("click", function () {
        const controls = this.nextElementSibling;
        if (controls.innerHTML === "▶") {
        controls.innerHTML = "| |";
        this.play();
        } else {
        controls.innerHTML = "▶";
        this.pause();
        }
    });
    video[i].addEventListener("mouseout", function () {
        const controls = this.nextElementSibling;
        if (!this.paused) {
        controls.style.display = "none";
        }
    });
    video[i].addEventListener("mouseover", function () {
        const controls = this.nextElementSibling;
        controls.style.display = "flex";
    });
    video[i].addEventListener(
        "ended",
        function () {
        const controls = this.nextElementSibling;
        controls.style.display = "flex";
        controls.innerHTML = "▶";
        },
        false
    );
    }
</script>



