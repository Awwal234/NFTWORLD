<script lang="ts">
import { defineComponent } from 'vue'
import HeaderBanner from './components/HeaderBanner.vue'
import HeroSection from './components/HeroSection.vue'
import CreateSession from './components/CreateSession.vue'
import ExploreMarket from './components/ExploreMarket.vue'
import SubLetter from './components/SubLetter.vue'
import FooterLook from './components/FooterLook.vue'

export default defineComponent({
  components: {
    HeaderBanner,
    HeroSection,
    CreateSession,
    ExploreMarket,
    SubLetter,
    FooterLook,
  }
})
</script>

<template>
  <main class="hidden lg:block bg-[#fff]">
    <HeaderBanner />
    <HeroSection />
    <CreateSession />
    <ExploreMarket />
    <SubLetter />
    <FooterLook />
  </main>
</template>

<style>
@font-face {
  font-family: Satochi Variable;
  src: url(./fonts/Satoshi-Variable.ttf);
}

html {
  height: 100%;
}

body,
main {
  font-family: Satochi Variable;
  min-height: 100vh;
}

body::-webkit-scrollbar {
  width: 3px;
  background: transparent;
}

body::-webkit-scrollbar-thumb {
  width: 3px;
  background: #DE5A10;
  border-radius: 4px;
}
</style>
