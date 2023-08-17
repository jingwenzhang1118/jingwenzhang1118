---

layout: page
title: Data Visualization

---

<style>
.container {
    width: 70%;
    height: 400px;
    margin: 0 auto;
}
.container_img {
    width: 100%;
    height: 100%;
    object-fit: fill;
}

hr {
    background-color: whitesmoke;
    size: 1px;
    opacity: .25
}

<!-- for mp4 -->
.custom-video {
    top: 0;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    align-content: center;
    flex-wrap: wrap;
}

.custom-video__container {
    position: relative;
    top: 0;
    width: 100%;
    height: 100%;
    margin: 1em;
}

.custom-video__video {
    border-radius: 0.2em;
    cursor: pointer;
}

.custom-video__control {
    position: absolute;
    top: 43%;
    left: 46%;
    background-color: rgba(0, 0, 0, 0.5);
    border-radius: 50%;
    padding: 1em;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #ffffff;
    font-size: 1em;
    font-weight: 400;
    width: 2em;
    height: 2em;
    white-space: nowrap;
    line-height: 0;
}

video::-webkit-media-controls {
    position: relative;
    z-index: 1;
}

.fighd {
    color: #1f77b4;
}

</style>


Drawing graphs is of great importance for exploring data structure, identifying trends and clusters, detecting unusual data points and presenting results. Figures can quickly communicate a significant amount of information. It is without a doubt that **a good graph is worth a thousand words**. 

Here I display some dynamic figures I draw using Python. In particular, I will use these figures to explore the trend of CSR performance, and its association with some firm characteristics. The CSR ratings of US companies are collected from KLD database for the period from 2004 to 2018. 
<br>
<hr>


<h3 id="fighd"> CSR Performance over time </h3>

- The folllowing suggests that CSR performance of firms has improved over time. 
<br>

<div class="container">
<div class="custom-video">
      <!-- first video  -->
      <div class="custom-video__container">
        <video class="custom-video__video" width="100%" height="100%" muted>
          <source src="/images/avgcsr.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <div class="custom-video__control">▶</div>
    </div>
</div></div>



<div class="custom-video">
      <!-- first video  -->
      <div class="custom-video__container">
        <video class="custom-video__video" width="100%" height="auto" muted>
          <source src="/images/avgcsr.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <div class="custom-video__control">▶</div>
    </div>
</div>
<br>
<hr>


<h3 class="fighd"> CSR Performance over time by Industry</h3>

- The plots below show that CSR performance of all industries enhanced over time. 
- A deeper exploration shows that some industries often outperformed the average performance of all US compaies (left figure), while the others stayed below the average (rigth figure).

<div class="container">
<div class="custom-video">
      <!-- first video  -->
      <div class="custom-video__container">
        <video class="custom-video__video" width="100%" height="100%" muted>
          <source src="/images/avgcsr_ind.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <div class="custom-video__control">▶</div>
    </div>
</div></div>
<br>
<hr>


<h3 class="fighd"> CSR Performance over time by Gender</h3>

- Many literature document that females and males make decisions differently due to their differences in characteristics. 
- Here I show that firms run by female CEOs on average have better CSR performance than firms run by male CEOs. 
- However, the differences reduced over time, as the CSR performance under the operation of male CEOs kept increasing. 

<div class="container">
<div class="custom-video">
      <!-- first video  -->
      <div class="custom-video__container">
        <video class="custom-video__video" width="100%" height="100%" muted>
          <source src="/images/avgcsr_gender.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <div class="custom-video__control">▶</div>
    </div>
</div></div>
<br>
<hr>


<h3 class="fighd"> CSR Performance and Firm Size</h3> 

- Large firms are expected to have more resources to invest in CSR activities, which should lead to greater CSR performance (CSR ratings). 
- The left figure plots the linear relationship between CSR performance and firm size(measured by the logarithm of a firm's assets) each year. The scatters show part of the data used for the linear regression. As expected, there is a positive assocation between CSR and firm size. Interestingly, the association becomes greater in more recent years. 
- The right bar chart displays the coefficients of firm size by year. Clearly, the coefficients, indicative of the association between CSR and firm size, are larger in recent years. 

<div class="container">
<div class="custom-video">
      <!-- first video  -->
      <div class="custom-video__container">
        <video class="custom-video__video" width="100%" height="100%" muted>
          <source src="/images/avgcsr_ols.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <div class="custom-video__control">▶</div>
    </div>
</div></div>
<br>
<hr>


### You can find the related codes below:
- Codes for <a href="jingwenzhang1118/jingwenzhang1118.github.io/visuals_prep.ipynb" target="_blank">cleaning and restructuring the data</a>.
- Codes for <a href="jingwenzhang1118/jingwenzhang1118.github.io/visuals.ipynb" target="_blank">making the dynamic figures</a>. 


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