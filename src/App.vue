<script setup lang="ts">
import { ref } from 'vue'
import HeaderMain from './components/HeaderMain.vue'
import SectionLanding from './components/SectionLanding.vue'
import SvgLandingBg from './components/SvgLandingBg.vue'
import SvgBgLines from './components/SvgBgLines.vue'
import SectionPass from './components/SectionPass.vue'
import SectionAbout from './components/SectionAbout.vue'
import SectionCollaborations from './components/SectionCollaborations.vue'
import SectionRoadmap from './components/SectionRoadmap.vue'
import SectionMembersAccess from './components/SectionMembersAccess.vue'

type SECTIONS = 'genesis' | 'about' | 'collab' | 'roadmap'

const sectionGenesis = ref<InstanceType<typeof SectionPass> | null>(null)
const sectionAbout = ref<InstanceType<typeof SectionAbout> | null>(null)
const sectionCollab = ref<InstanceType<typeof SectionCollaborations> | null>(
  null,
)
const sectionRoadmap = ref<InstanceType<typeof SectionRoadmap> | null>(null)

function scrollToSection(sectionRef: SECTIONS) {
  let section = null
  switch (sectionRef) {
    case 'genesis':
      section = sectionGenesis
      break
    case 'about':
      section = sectionAbout
      break
    case 'collab':
      section = sectionCollab
      break
    case 'roadmap':
      section = sectionRoadmap
      break
    default:
      return
  }

  section.value?.$el.scrollIntoView({
    behavior: 'smooth',
    block: 'start',
  })
}
</script>

<template>
  <HeaderMain
    class="header-main"
    @navGenesis="scrollToSection('genesis')"
    @navAbout="scrollToSection('about')"
    @navCollab="scrollToSection('collab')"
    @navRoadmap="scrollToSection('roadmap')"
  />

  <main>
    <SectionLanding class="section" @navGenesis="scrollToSection('genesis')" />
    <SectionPass class="section" ref="sectionGenesis" />
    <SectionAbout class="section" ref="sectionAbout" />
    <SectionCollaborations class="section" ref="sectionCollab" />
    <SectionRoadmap class="section" ref="sectionRoadmap" />
    <SectionMembersAccess />
  </main>
  <div class="fixed-bg-filter"></div>

  <SvgLandingBg class="bg" />
  <SvgBgLines class="bg bg-0" :loopSpeed="1" />
</template>

<style scoped lang="scss">
.header-main {
  // background-color: aqua;
  background: rgba(4, 4, 6, 0.6);
  box-shadow: inset 0px 4px 4px rgba(0, 0, 0, 0.25);
  position: absolute;
  width: 98.5vw;
  z-index: 10;
}
.section {
  margin-bottom: 120px;
  &:not(:last-child) {
    padding-top: 60px;
  }
}

h1 {
  font-family: Audiowide;
}
.fixed-bg-filter {
  background: $web3sg-bg;
  height: 100vh;
  width: 100vw;
  position: fixed;
  z-index: -5;
  top: 0;
}
.bg {
  width: 98vw;
  position: absolute;
  top: 0;
  z-index: -5;
}
</style>
