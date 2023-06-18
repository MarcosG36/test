
<template>
    <div id="eventgallerie">
    <!--     <Swiper
           :slides-per-view="3"
           :space-between="50"
          
  >
         <SwiperSlide  v-for="n in {users}" :key='n'>
        
                <img src="{{ n.url }}" >
                
        </SwiperSlide>
     <div>
                <h1>{{imagesGallery[1].url}}</h1>
            </div>
    
  </Swiper> -->
   
   <img v-if="result" src="{{imagesGallery[1].url}}" alt="">
   <img src="https://unsplash.com/photos/DwTZwZYi9Ww" alt="">
    </div>


</template>





<script>

import axios from 'axios'
/* import SwiperCore from 'swiper' */
/* import { Swiper, SwiperSlide } from 'swiper/vue';/*  */ 
/* import "swiper/swiper.scss" */

export default {
    name: 'eventGallery',
    /* components: {
      Swiper,
      SwiperSlide,
    }, */
    data(){
        return{
            imagesGallery:null,
            result:null
        }
    },
    created(){
            console.log('mi perro')
            axios.get('http://localhost:8080/v2/list?page=2&limit=100')
            .then(res=>{
                 this.imagesGallery=res.data
                 console.log(res.data)
                 console.log(res.data[1].url)
                 this.result=true
            })
            .catch(e => console.log(e))  },
    
            
        }
    
        
   
   
          
  
        
    


    

</script>0

