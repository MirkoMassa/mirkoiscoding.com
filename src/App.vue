<template>
  <router-view/>
</template>

<script>
import { gsap } from 'gsap';
import CSSRulePlugin from "gsap/CSSRulePlugin";
gsap.registerPlugin(CSSRulePlugin);

document.addEventListener('DOMContentLoaded', () => {
    gsap.to(["#nav-div",".nav-social", "#icon", '#rect', '#ab-container'], 
    {
        opacity: 1,
        duration: 1,
        ease: gsap.easeInOut
    }

);
})
export default {
  name: 'App',
  data() {
    return {

    }
  },
}
</script>

<style>
  @import 'D:/Coding/personal-website/src/assets/style/style.css';
</style>