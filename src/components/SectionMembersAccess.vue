<script setup lang="ts">
import SvgPass from './SvgPass.vue'
import BtnMemberAccess from './BtnMemberAccess.vue'
</script>

<template>
  <section>
    <div class="hero">
      <div class="column column-pass">
        <SvgPass class="pass" />
      </div>
      <div class="column column-text">
        <h2>Web3SG Members</h2>
        <div class="text">
          Already hold the Web3SG Pass? <br />
          Authenticate your NFT and gain access
        </div>
      </div>
      <div class="column">
        <BtnMemberAccess class="btn" />
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
section {
  padding: 0 130px 140px;
  .hero {
    padding: 60px 80px;
    background: #0d0911;
    display: grid;
    grid-template-columns: 0.5fr 3fr 1fr;
    .column {
      display: flex;
      flex-direction: column;
      justify-content: center;
      &.column-pass {
        align-items: flex-end;
        margin-right: 50px;
      }
      .pass {
        width: 150px;
      }
      &.column-text {
        justify-content: space-between;
        h2 {
          font-size: 24px;
        }
        .text {
          font-family: 'Space Grotesk';
          font-style: normal;
          font-weight: 300;
          font-size: 14px;
          line-height: 20px;
          /* or 125% */

          letter-spacing: 0.05em;

          color: $web3sg-grey-dark;
        }
      }
      .btn {
        width: 80%;
      }
    }
  }
}

@media (max-width: $web3sg-tablet-limit) {
  section {
    padding: 0;
    .hero {
      padding: 60px 50px;
      grid-template-columns: 0.5fr 3fr 1.5fr;
      .column:last-child {
        .btn {
          width: 100%;
        }
      }
    }
  }
}

@media (max-width: $web3sg-mobile-limit) {
  section .hero {
    padding: 40px 25px;

    display: flex;
    flex-direction: column;
    row-gap: 32px;
    justify-content: center;
    text-align: center;
    .column {
      &.column-pass {
        align-items: center;
        margin-right: 0px;
      }
      &.column-text {
        justify-content: space-between;
        h2 {
          font-size: 22px;
          margin-bottom: 12px;
        }
      }
    }
  }
}
</style>
