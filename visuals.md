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

<div class="container">
<video class="container_video" controls autoplay>
    <source src="/images/avgcsr.mp4" type=video/mp4>
</video>
</div>

<br>
<hr>


## CSR Performance over time by industry
The plots below show that CSR performance of all industries enhanced over time. And some industries often outperformed the average performance of all US compaies (left figure), while the others stayed below the average (rigth figure).



### You can find the relevant codes below:
- <a href="/" Codes for cleaning and restructuring the data
- Codes for making the figures. 
