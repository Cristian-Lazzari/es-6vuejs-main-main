<script setup>

</script>

<template>
  <div class="pag4">
    <div class="pag4-left">
        <h2>5 YEARS</h2>
        <p>OF RESEARCH & DEVELOPMENT</p>
    </div>
    <div class="pag4-right">
        <p class="p1">CERTIFIED LAB RESULTS</p>
        <p class="p2">100% NATURAL AND ORGANIC</p>
        <p class="p3">73% MORE PROTEIN</p>
        <p class="p4">KETO DIET FRINDLY</p>
        <p class="p5">HIGHEST ANTIOXIODANT RATE</p>
        <p class="p6">100% HIGHER LEVEL OF AMINO ACID</p>
    </div>
  </div>
</template>

<style scoped lang="scss">
@use "../assets/styles/general.scss";
.pag4{
    display: flex;
    align-items: stretch;
    
}
.pag4-left, .pag4-right{
    width: 50%;
    padding: 12rem 3rem;
   
}
.pag4-left{
    background-color: #FBED3F;
    color: #999b81;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}
.pag4-left h2 {
    font-size: 100px;
}
.pag4-left p {
    font-size: 50px;
    
    text-align: center;
}
.pag4-right{
    background-color: #999b81;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    
}
.pag4-right p{
    font-size: 30px;
    width: 100%;
    text-align: center;
    color: #FFFFFF;
    
}
.p1{
    opacity: 1;
}
.p2{
    opacity: 0.95;
}
.p3{
    opacity: .7;
}
.p4{
    opacity: .6;
}
.p5{
    opacity: .5;
}
.p6{
    opacity: .4;
}
@media (max-width: 770px) {
    .pag4{
        flex-direction: column;
    }
    .pag4-left, .pag4-right{
        width: 100%;
        font-size: 30px;
    }
}
</style>
