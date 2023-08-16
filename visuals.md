---

layout: page
title: Data Visualization

---

<style>
.container {
    width: 70%;
    height: 300px;
    margin: 0 auto;
}
.container_img {
    width: 100%;
    height: 100%;
    object-fit: fill;
}

.container_video {
    width: 100%;
    height: 100%;
    object-fit: fill;
}

hr {
    background-color: whitesmoke;
    size: 1px;
    opacity: .25
}

.custom-video {
    position: relative;
    top: 0;
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    align-content: center;
    flex-wrap: wrap;
    background-color: #00808097;
}

.custom-video__container {
    position: relative;
    top: 0;
    width: 32vw;
    height: auto;
    margin: 1em;
    font-family: 'Oswald', sans-serif;
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
    width: 3em;
    height: 3em;
    white-space: nowrap;
    line-height: 0;
}

video::-webkit-media-controls {
    position: relative;
    z-index: 1;
}

</style>


Drawing graphs is of great importnat for exploring data structure, identifying trends and clusters, detecting unusual data points and presenting results. Figures can quickly communicate a significant amount of information. It is without a doubt that *a good graph is worth a thousand words*. 

Here I display some figures I draw using Python. In particular, I will use these figures to explore the trend of CSR performance, and its association with some firm characteristics. The CSR ratings of US companies are collected from KLD database for the period from 2004 to 2018. 

## CSR Performance over time
The folllowing suggests that CSR performance of firms has improved over time. 

<div class="container">
<img class="container_img" src="/images/avgcsr.gif">
</div>

<div class="container">
<img class="container_img" src="/images/avgcsr_all.gif">
</div>

<video controls autoplay>
    <source src="/images/avgcsr.mp4" type="video/mp4">
</video>

<div class="custom-video">
      <!-- first video  -->
      <div class="custom-video__container">
        <video class="custom-video__video" width="100%" height="auto" muted>
          <source src="/images/avgcsr.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <div class="custom-video__control">▶</div>
      </div>

<br>
<hr>


## CSR Performance over time by industry
The plots below show that CSR performance of all industries enhanced over time. And some industries often outperformed the average performance of all US compaies (left figure), while the others stayed below the average (rigth figure).



### You can find the relevant codes below:
- <a href="/" >Codes for cleaning and restructuring the data</a>
- <a href=Codes for making the figures. 


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