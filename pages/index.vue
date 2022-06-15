<template>
 <div class="container">
 <Nav />
 <Hero />
 <LargeCardDisplay 
 v-for="cardInfo in largeCardInfo"
 :key="cardInfo.id"
 :cardsSection="cardInfo"
 />
 <SmallCardDisplay
 v-for="cardInfo in smallCardInfo"
 :key="cardInfo.id"
 :cardsSection="cardInfo"
 
  />
 </div>
</template>

<script>
import {largeCardSections, smallCardSections} from "@/assets/data.js"
import LargeCardDisplayVue from "../components/LargeCardDisplay.vue";
import SmallCardDisplayVue from "../components/SmallCardDisplay.vue";
export default {
    data() {
        return {
            largeCardInfo: largeCardSections,
            smallCardInfo:smallCardSections
        };
    },
    components: { SmallCardDisplayVue }
}
</script>
