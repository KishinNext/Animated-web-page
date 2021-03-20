<template>

    <nav class="navbar navbar-expand-lg navbar-dark bg-transparent container" :class=" { 'navbarOpen': show }">
        <div class="logo">Ride</div>
        
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" @click.stop="toggleNavbar()">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse mr-5" id="navbarSupportedContent" :class="{ 'show': show }">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0 mt-3">
                    <li class="nav-item"><router-link  to="/"  class="nav-link active">Our Products</router-link></li>
                    <li class="nav-item"><router-link  to="/"  class="nav-link active">Our Company</router-link></li>
                    <li class="nav-item"><router-link  to="/"  class="nav-link active">Safety</router-link></li>
                    <li class="nav-item"><router-link  to="/"  class="nav-link active">Help</router-link></li>
            </ul>
        </div>
    </nav>
    
</template>

<script>
import { gsap } from 'gsap';
export default {
    mounted: function(){
        gsap.from('header',{duration:0.6, ease:"power2.out", y:-200})
        gsap.from('dropdown',{duration:0.6, ease:"power2", y:-100})
    },
    data() {
        return {
        show: false
        }
    },
    methods: {
        toggleNavbar() {
        this.show = !this.show
        }
    }
}
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');


.menu{
    top: 0;
    left: 0;
    right: 0;
    z-index: 1;
    padding: 20px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}
.logo{
    font-weight: 600;
    font-size: 2.2em;
    color: white;
    margin-top: 6px;
    cursor: pointer;
    margin-right: 80px;
}

</style>