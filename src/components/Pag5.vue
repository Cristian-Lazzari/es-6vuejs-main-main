<script>
export default {
  data() {
    return {
     sidebar1: 0,
     sidebar2: 0,
     sidebar3: 0,
    }
  },
  methods: {
    barside() {
      if (this.sidebar1) {
        this.sidebar1 = 0
      } else {
        this.sidebar1 = 1
      }
      console.log(this.sidebar1)
    }
}
}
</script>

<template>
  <div class="pag5">
    <div class="container">
        <div class="title-pag5"><h2>3 METABOLIC BOOSTERS</h2></div>
        <div class="container-bar">
            <div class="bar1">
                <div class="top-bar1">
                    <h3>AMINO ACIDS</h3>
                    <span @click="generalbar(this.sidebar1)" :class="sidebar1 ? 'sidebar1open' :'sidebar1close'"  ><i class="bi bi-plus"></i></span>
                </div>
                <div class="bottom-bar1">
                    <div  :class="sidebar1 ? 'sidecontent1open' :'sidecontent1close'">
                        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eligendi quibusdam quod debitis maxime. Tempore iusto dolorem odit eum. Natus labore ab blanditiis reprehenderit debitis voluptatum accusamus facere impedit dolor quod.
                    </div> 
                </div>
            </div>
            <div class="bar2">
                <div class="top-bar2">
                    <h3>AMINO ACIDS</h3>
                    <span @click="generalbar(this.sidebar2)" :class="sidebar2 ? 'sidebar1open' :'sidebar1close'"  ><i class="bi bi-plus"></i></span>
                </div>
                <div class="bottom-bar2">
                    <div  :class="sidebar2 ? 'sidecontent1open' :'sidecontent1close'">
                        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eligendi quibusdam quod debitis maxime. Tempore iusto dolorem odit eum. Natus labore ab blanditiis reprehenderit debitis voluptatum accusamus facere impedit dolor quod.
                    </div> 
                </div>
            </div>
            <div class="bar3">
                <div class="top-bar3">
                    <h3>AMINO ACIDS</h3>
                    <span @click="generalbar(this.sidebar3)" :class="sidebar3 ? 'sidebar1open' :'sidebar1close'"  ><i class="bi bi-plus"></i></span>
                </div>
                <div class="bottom-bar3">
                    <div  :class="sidebar1 ? 'sidecontent1open' :'sidecontent1close'">
                        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eligendi quibusdam quod debitis maxime. Tempore iusto dolorem odit eum. Natus labore ab blanditiis reprehenderit debitis voluptatum accusamus facere impedit dolor quod.
                    </div> 
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@use "../assets/styles/general.scss";
.pag5{
    background-color:#1a1a17 ;
    padding-top: 100px;
}
.container{
    padding: 0px 100px;
}
.title-pag5{
    display: flex;
    align-items: center;
    padding-bottom: 100px;
}
.title-pag5 h2{
    font-size: 70px;
    color: #FFFFFF;
}
.bar1, .bar2, .bar3{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    font-size: 30px;
    color: #FFFFFF;
    border-top: 1px solid white;
    padding: 20px 0px;
}
.bar1 i, .bar2 i, .bar3 i{
    font-size: 80px;
}
.bar2{
    opacity: .5;
}
.bar3{
    opacity: .3;
    border-bottom: 1px solid white;
    padding-bottom: 100px;
}
.sidebar1open{
    transform: rotateZ(45deg);
}
.sidecontent1open {
    padding: 3rem 0rem;
    display: block;
}
.sidecontent1close{
    display: none;
}
.top-bar1,.top-bar2,.top-bar3{
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.bottom-bar1{
//display: none;
}
@media (max-width: 770px) {
    .container{
        padding: 0px 20px;
    }
    .title-pag5 h2{
        font-size: 50px;
    }
    .bar1 i, .bar2 i, .bar3 i{
    font-size: 60px;
    .bar1 h3, .bar2 h3, .bar3 h3{
        font-size: 30px;
    }
    }
    .bar2{
        flex-wrap: wrap;
    }
    


    
}
    

</style>
