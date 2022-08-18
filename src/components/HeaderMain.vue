<script setup lang="ts">
import IconDiscord from './icons/IconDiscord.vue'
import IconTwitter from './icons/IconTwitter.vue'
import BtnMemberAccess from './BtnMemberAccess.vue'
</script>

<template>
  <header class="main">
    <div class="segment left">
      <img
        class="main-logo icon"
        src="@/assets/main-logo.png"
        @click="$emit('navTop')"
      />
      <a href="https://discord.com/invite/web3sg" class="icon" target="_blank">
        <IconDiscord class="icon" />
      </a>
      <a
        href="https://twitter.com/web3sg?s=20&t=WHzgl2BW6wE2ffB3OkW7Xg"
        class="icon"
        target="_blank"
      >
        <IconTwitter class="icon" />
      </a>
    </div>
    <div class="segment center">
      <div class="nav-btn" @click="$emit('navGenesis')">Genesis Pass</div>
      <div class="nav-btn" @click="$emit('navAbout')">About Us</div>
      <div class="nav-btn" @click="$emit('navCollab')">Collaborations</div>
      <div class="nav-btn" @click="$emit('navRoadmap')">Roadmap</div>
    </div>
    <div class="segment right">
      <BtnMemberAccess class="btn" />
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  display: flex;
  justify-content: space-between;
  color: white;
  font-family: Poppins, Arial, Helvetica, sans-serif;
  font-weight: 300;
  padding: 14px 40px 14px 28px;
  font-size: 16px;
}

.nav-btn {
  transition: color 0.25s ease;
  &:hover {
    color: $web3sg-purple-light;
  }
}

.icon {
  transition: fill 0.25s ease;
  fill: white;
  &:hover {
    fill: $web3sg-purple-light;
  }
}

.segment {
  display: flex;
  flex-direction: row;
  align-items: center;
  column-gap: 24px;

  &.left {
    flex-grow: 1;
    .icon {
      height: 30px;
      cursor: pointer;
    }
    .icon.main-logo {
      height: 48px;
    }
  }

  &.center {
    column-gap: 80px;
    flex-grow: 3;
    justify-content: center;
    .nav-btn {
      cursor: pointer;
    }
  }

  &.right {
    flex-grow: 1;
    justify-content: end;
  }
}

@media (max-width: $web3sg-tablet-limit) {
  header {
    font-size: 12px;
    padding: 6px 10px 6px 12px;
    .btn {
      padding: 6px 14px;
    }
    .segment {
      column-gap: 4px;
      &.center {
        column-gap: 18px;
      }
    }
  }
}

@media (max-width: $web3sg-mobile-limit) {
  header {
    font-size: 12px;
    padding: 6px 10px 6px 12px;
    .left :not(.main-logo),
    .center {
      display: none;
    }
  }
}
</style>
