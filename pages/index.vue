<template>
 <div class="container">
 <Hero />
 <LargeCardDisplay 
 v-for="cardInfo in largeCardInfo"
 :key="cardInfo.id"
 :cardsSection="cardInfo"
 />
 </div>
</template>

<script>
import {largeCardSections} from "@/assets/data.js"
import LargeCardDisplayVue from "../components/LargeCardDisplay.vue";
export default {
  data() {
    return {
      largeCardInfo : largeCardSections
      
    }
  },
    
}
</script>
