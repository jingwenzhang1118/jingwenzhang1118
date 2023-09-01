---

layout: page
title: Data Visualization

---

<link rel="stylesheet" href="/assets/css/res.css">


Graphs improve the effectiveness of reporting. No wonder that **a good graph is worth a thousand words**. 

I created dynamic figures using Python to show the **trend of CSR (Corporate Social Responsibility) performance of US companies**, and **its association with some firm characteristics**. The CSR ratings of US companies are collected from KLD database for the period from 2004 to 2018. 
<br>
<hr>


<h3 class="fighd" id="#f1">CSR Performance over time</h3>

- The folllowing figure suggests that **CSR performance of firms has improved over time**. 

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


<h3 class="fighd" id="#f2">CSR Performance over time by Industry</h3>

- **Some industries** often **outperformed** the average performance of all the US compaies (**left figure**), while the **other industries** mostly **performed below the average** (**rigth figure**)

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


<h3 class="fighd" id="#f3">CSR Performance over time by CEO's Gender</h3>

- **Firms operated by Female CEOs on average had better CSR performance** than firms run by male CEOs. 
- However, **the difference decreased over time**, as the CSR performance of firms with male CEOs kept increasing. 

<div class="custom-video">
      <div class="custom-video__container">
        <video class="custom-video__video" width="100%" height="auto" muted autoplay>
          <source src="/images/avgcsr_gender.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <div class="custom-video__control">▶</div>
    </div>
</div>
<hr>


<h3 class="fighd" id="#f4">CSR Performance and Firm Size</h3> 

- The left figure shows **a positive assocation between CSR and firm size** each year. 
- Interestingly, **the association between CSR performance and firm size becomes greater in more recent years**, as the slope of the line increases over time.
- The right bar chart displays the coefficients and confirms that **the association between CSR performance and firm size is larger in recent years**. 

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


<h3 class="fighd">You can find the Python codes below:</h3>

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



