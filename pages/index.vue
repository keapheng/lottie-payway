<template>
            <lottie :options="defaultOptions" :height="600" :width="600" v-on:animCreated="handleAnimation"/>
</template>

<script>
import Lottie from 'vue-lottie';
import * as animationData from '@/assets/image.json';
export default {
    name: "HomepageHeader",
    components: {
      'lottie': Lottie
    },
    data() {
        return {
            defaultOptions: {animationData: animationData.default},
            animationSpeed: 1,
            anim: null
        }
    },
    methods: {
      handleAnimation: function (anim) {
        this.anim = anim;
      }
    }
}
</script>

<style scoped>
</style>