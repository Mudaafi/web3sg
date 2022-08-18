<script setup lang="ts"></script>

<template>
  <section>
    <h1>WEB3SG</h1>
    <div class="subtext">
      An exclusive community built on the foundations of integrating <br />the
      most brilliant minds in both the Web 2 and 3 space.
    </div>
    <div class="btn" @click="$emit('navGenesis')">
      <div class="btn-text">Discover More</div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
section {
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  h1 {
    margin-top: 120px;
    font-family: Audiowide;
    font-weight: 400;
    font-size: 7.5vw;
    text-align: center;

    letter-spacing: 0.2em;
    text-transform: capitalize;
    background: linear-gradient(
      90deg,
      #6b323e 10.15%,
      #f4fff8 50.52%,
      #354a99 83.85%
    );
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-fill-color: transparent;
    width: 98.5vw;
  }
  div.subtext {
    width: 44vw;
    line-height: 28px;
    font-family: 'Space Grotesk';
    text-align: center;
    color: white;
    text-shadow: 1px -1.5px 6px #a6a6a6;
    font-weight: 400;
    margin-bottom: 40px;
  }
  .btn {
    border-radius: 12px;
    background: $web3sg-gradient-main;
    font-family: 'Space Grotesk';
    color: white;
    padding: 2px;
    font-size: 16px;
    cursor: pointer;
    .btn-text {
      border-radius: 10px;
      padding: 8px 30px;
      background: #35282d;
    }
  }
}
// -- Mobile Styles
@media (max-width: $web3sg-tablet-limit) {
  section {
    height: auto;
    justify-content: flex-start;
    div.subtext {
      width: 90vw;
      font-size: 18px;
      line-height: 28px;
      font-weight: 400;
      margin-bottom: 32px;
    }
    h1 {
      margin-top: 0;
    }
  }
}

@media (max-width: $web3sg-mobile-limit) {
  section {
    div.subtext {
      width: 90vw;
      font-size: 11px;
      line-height: 18px;
      font-weight: 400;
      margin-bottom: 20px;
    }
    .btn {
      font-size: 12px;
      .btn-text {
        padding: 6px 18px;
      }
    }
  }
}
</style>
