<script setup lang="ts">
import SvgCollectionCards from './SvgCollectionCards.vue'
</script>

<template>
  <section>
    <div class="column">
      <h2>Roadmap</h2>
      <div class="text">
        Web3SG serves as a bridge for WEB2.0 and WEB3.0. Our mission is to
        create and support world-changing projects and movements.
      </div>
      <div class="card-size-container">
        <div class="card-numbers">2,000</div>
        <SvgCollectionCards class="cards-svg" />
      </div>
      <div class="subtitle">Collection Size</div>
      <div class="variants">
        <div class="variant">
          <div class="variant-card-container">
            <img
              class="variant-cards"
              src="../assets/images/variant-cards.png"
              alt=""
            />
            <div class="variant-card-count">5/500</div>
          </div>
          <div class="subtitle">Sakura</div>
          <hr />
        </div>
        <div class="variant">
          <div class="variant-card-container">
            <img
              class="variant-cards"
              src="../assets/images/variant-cards.png"
              alt=""
            />
            <div class="variant-card-count">39/500</div>
          </div>
          <div class="subtitle">Citadel</div>
          <hr />
        </div>
        <div class="variant">
          <div class="variant-card-container">
            <img
              class="variant-cards"
              src="../assets/images/variant-cards.png"
              alt=""
            />
            <div class="variant-card-count">6/500</div>
          </div>
          <div class="subtitle">Kaijuverse</div>
          <hr />
        </div>
        <div class="variant">
          <div class="variant-card-container">
            <img
              class="variant-cards"
              src="../assets/images/variant-cards.png"
              alt=""
            />
            <div class="variant-card-count">30/500</div>
          </div>
          <div class="subtitle">Deadlands</div>
          <hr />
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  .column {
    width: 50vw;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  h2 {
    margin-bottom: 42px;
  }
  .text {
    margin-bottom: 80px;
    line-height: 20px;
    letter-spacing: 0.05em;
  }
  .card-size-container {
    position: relative;
    width: 100%;
    padding: 100px 0 20px 140px;
    margin-right: 60px;
    .cards-svg {
      position: absolute;
      top: 0;
      right: 0;
      left: 0;
      margin: 0px auto;
      width: 175px;
    }
    .card-numbers {
      color: #f4f4f4;
      font-family: 'Space Grotesk';
      font-weight: 700;
      font-size: 36px;
      letter-spacing: 0.05em;
      z-index: 3;
    }
  }
  .subtitle {
    font-size: 16px;
    color: #f4f4f4;
    opacity: 0.75;
    font-family: Poppins;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 0.05em;
  }
  .variants {
    margin-top: 80px;
    display: grid;
    position: relative;
    grid-template-columns: 1fr 1fr;
    column-gap: 140px;
    // background-color: aqua;
    width: 100%;

    .variant {
      margin-bottom: 40px;
      .variant-card-container {
        position: relative;
        width: 100%;
        padding: 85px 0 80px 0;
        .variant-cards {
          position: absolute;
          width: 247px;
          top: 0;
          left: 0;
          right: 0;
          margin: 0 auto;
        }
        .variant-card-count {
          color: #f4f4f4;
          font-family: 'Space Grotesk';
          font-weight: 700;
          font-size: 28px;
          letter-spacing: 0.05em;
          z-index: 3;
        }
      }
      .subtitle {
        font-size: 14px;
      }
      hr {
        height: 1px;
        width: 40%;
        justify-self: center;
        align-self: center;
        margin: auto;
        border: none;
        background: linear-gradient(
          90deg,
          rgba(128, 147, 255, 0) 0%,
          rgba(255, 234, 231, 0.921538) 16.15%,
          #edb7ff 48.96%,
          #95bfff 73.96%,
          rgba(92, 228, 207, 0) 100%
        );
      }
    }
  }
}

@media (max-width: $web3sg-tablet-limit) {
  section {
    .column {
      width: 80vw;
    }
    h2 {
      margin-bottom: 32px;
    }
  }
}

@media (max-width: $web3sg-mobile-limit) {
  section {
    h2 {
      margin-bottom: 18px;
    }
    .text {
      margin-bottom: 40px;
    }
    .variants {
      grid-template-columns: 1fr;
    }
  }
}
</style>
