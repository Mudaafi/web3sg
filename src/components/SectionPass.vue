<script setup lang="ts">
import SvgPass from './SvgPass.vue'
</script>

<template>
  <section>
    <div class="col col-pass">
      <SvgPass class="pass" />
    </div>
    <div class="col">
      <div>
        <h2>Web3SG Genesis Pass</h2>
        <div class="text">
          The Web3SG Genesis Collection is a collection of 1000 Tiered NFT
          passes that give its holders exclusive rights and access to a plethora
          of networking opportunities, funding and decision-making within the
          WEB3SG community. Passes will be split into two categories, 500
          <span class="red">Citadel</span> Passes and 500
          <span class="purple">Deadlands</span> passes.
        </div>
      </div>
      <a class="btn" href="https://dyno.gg/form/41b1808b" target="_blank">
        <img src="../assets/images/OpenSeaLogo.png" alt="OpenSea Logo" />
        <p>View on OpenSea</p>
      </a>
    </div>
    <div class="bg"></div>
  </section>
</template>

<style scoped lang="scss">
.bg {
  position: absolute;
  opacity: 0.5;
  width: 98vw;
  height: 250%;
  top: 0;
  margin-top: -30vh;
  z-index: -1;
  // background: red;
  background: linear-gradient(
    180deg,
    rgba(0, 0, 0, 0) 0%,
    #000000 32.47%,
    #000000 63.02%,
    rgba(0, 0, 0, 0) 97.92%
  );
}
section {
  display: flex;
  flex-direction: row;
  column-gap: 120px;
  justify-content: center;

  .col {
    display: flex;
    flex-direction: column;
    width: 600px;
    justify-content: space-between;
    &.col-pass {
      width: 450px;
    }
    h2 {
      margin-bottom: 28px;
    }
    .text {
      text-align: justify;
      span.red {
        color: $web3sg-red-light;
      }
      span.purple {
        color: $web3sg-purple-dark;
      }
    }
    .btn {
      display: flex;
      flex-direction: row;
      align-items: center;
      column-gap: 14px;
      color: black;
      font-family: 'Poppins';
      font-size: 16px;
      background: $web3sg-gradient-main;
      padding: 8px 28px 8px 20px;
      border-radius: 10px;
      width: fit-content;
      cursor: pointer;
      img {
        width: 32px;
      }
    }
  }
}

@media (max-width: $web3sg-tablet-limit) {
  section {
    flex-direction: column;
    row-gap: 50px;
    padding: 0 20px;
    text-align: center;
    align-items: center;
    .col {
      width: 75vw;
      &.col-pass {
        width: 45vw;
      }
      .btn {
        margin-top: 20px;
        align-self: center;
      }
    }
  }
}

@media (max-width: $web3sg-mobile-limit) {
  section {
    flex-direction: column;
    row-gap: 30px;
    padding: 0 20px;
    text-align: center;
    align-items: center;
    .col {
      width: 75vw;
      &.col-pass {
        width: 65vw;
      }
      h2 {
        margin-bottom: 14px;
      }
      .btn {
        margin-top: 20px;
        align-self: center;
      }
    }
  }
}
</style>
