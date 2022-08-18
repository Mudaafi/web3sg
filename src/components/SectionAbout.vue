<template>
  <section>
    <div class="overlay col">
      <h2>About Us</h2>
      <div class="text">
        Web3SG serves as a bridge between the web2 and the web3 space. Web3SG
        was formed with the aim to provide support and technical infrastructure
        to enable both established projects as well those within the process of
        launching to efficiently carry out their plans. This can be in the form
        of partnership selection, Full stack development, tokenomics, branding.
        We want to make the NFT space one that is thriving with legitimacy. One
        that does not solely revolve around ideals and promises, but one that
        delivers in both the good times and bad.
      </div>
      <div class="text">
        Another core focus of ours is to enable Web2 companies to integrate and
        break through the Web3 space. The NFT and Crypto markets are sensitive
        and skeptical of large conglomerates entering the space and bringing
        their traditional strategies here. However we believe for this nascent
        space to truly grow, we have to enable these successful traditional
        business models to establish themselves within our ecosystem. We want to
        be the bridge for these companies within Web2 to enter the space with
        ease.
      </div>
    </div>
    <div class="col bg-img"></div>
  </section>
</template>

<style scoped lang="scss">
section {
  display: flex;
  flex-direction: row;
  padding: 0 0 0 100px;
  column-gap: 80px;
  .col {
    width: 75vw;
    &.overlay {
      background-color: #1e181a;
      border-radius: 40px;
      padding: 62px 60px 50px;

      h2 {
        margin-bottom: 28px;
      }
      div {
        &:not(:last-child) {
          margin-bottom: 28px;
        }
        text-align: justify;
      }
    }
    &.bg-img {
      width: 25vw;
      background-size: cover;
      background-position: center top;
      background-image: url('../assets/images/BgImageAbout.png');
    }
  }
}

@media (max-width: $web3sg-tablet-limit) {
  section {
    justify-content: center;
    padding: 0;
    .col {
      width: 90vw;
    }
    .col:is(:last-child) {
      display: none;
    }
  }
}

@media (max-width: $web3sg-mobile-limit) {
  section {
    justify-content: center;
    padding: 0;
    text-align: center;
    .col {
      width: 90vw;
      &.overlay {
        h2 {
          margin-bottom: 12px;
        }
        padding: 31px 30px 25px;
      }
    }
  }
}
</style>
