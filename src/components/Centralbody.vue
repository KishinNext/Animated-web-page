<template>
  <section class="hero container">
      <div class="hero-content">
          <h1>Get in the driver's seat and <span>get paid</span></h1> 
          <p>Drive on the largest network of active riders</p>

          <button class="singup-btn">Sing Up To Drive</button>
          <button class="talk-btn">Talk To Us</button>
      </div>

      <div class="illustration">
        <Image/>
      </div>

  </section>
</template>

<script>
import Image from './Image'
import { gsap } from 'gsap';
export default {
    components:{
        Image
    },
    mounted: function(){
        gsap.from('.hero-content',{ duration: 1.5, ease: "bounce.out", y: -40, opacity:0, delay:0.5 })
        gsap.from('.singup-btn',{ duration: 1.5, ease: "bounce.out", y: -40, opacity:0, delay:0.7 })
        gsap.from('.talk-btn',{ duration: 1.5, ease: "bounce.out", y: -40, opacity:0, delay:0.7 })
        gsap.from('.illustration',{ duration: 1.5, ease: "power2.out", opacity:0, delay:1 })

        // let tl = gsap.timeline({delay:0.2})

        // tl.from('.hero-content',{ duration: 1.5, ease: "bounce.out", y: -40, opacity:0})
        // tl.from('.singup-btn',{ duration: 1.5, ease: "bounce.out", y: -40, opacity:0 })
        // tl.from('.talk-btn',{ duration: 1.5, ease: "bounce.out", y: -40, opacity:0})
        // tl.from('.illustration',{ duration: 1.5, ease: "power2.out", opacity:0})

    }
}
</script>

<style>
    @media (max-width: 1375px){
        .hero{
            flex-direction: row;
        }
        .illustration{
            margin-left: 20%;
        }
    }
    @media (max-width: 1200px){
        .hero{
            flex-direction: column-reverse;
        }
        .illustration{
            margin-left: 0%;
        }
    }
    section.hero{
        display: flex;
        align-items: center;
        justify-content: space-evenly;
        flex-wrap: wrap;
        margin: 0 auto;
        width: 100%;
    }
    section.hero h1{
        font-family: inherit;
        color:  white;
        font-size: 2.6em;
        margin-bottom: 1em;
        line-height: 1.2em;
    }
    section.hero h1 span{
        color: #FFD500;

    }
    section.hero p{
        font-size: 1em;
        color: white;
        margin-bottom: 2em;
    }
    button{
        padding: 20px 10px;
        margin-right: 10px;
        font-family: inherit;
        border: 1px solid white;
        font-size: 1em;
        background-color: none;
    }
    .singup-btn{
        background-color: white;
        color: #180037;
        cursor: pointer;
    }
    .talk-btn{
        background-color:  #180037;
        color: #ffffff;   
        cursor: pointer;
    }

    .hero-content{
        max-width: 300px;

    }

    .illustration{

        height: 50%;
        width: 50%;
        padding: 0;
        margin-bottom: 10%;
    }
    .illustration svg{
        
        width: 100%;
        height: 100%;
        padding: 0;
        margin: 0;
    }

</style>