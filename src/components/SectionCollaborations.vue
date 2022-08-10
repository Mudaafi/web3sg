<template>
  <section>
    <h1>COLLABORATIONS</h1>
    <h1 class="reflected">COLLABORATIONS</h1>
    <div class="collaborators">
      <a
        class="collaborator"
        href="https://twitter.com/ALPACADABRAZ"
        target="_blank"
      >
        <img src="../assets/images/Alpacadabraz.png" alt="Alpacadabraz pfp" />
        <div class="name">Alpacadabraz</div>
      </a>

      <a
        class="collaborator"
        href="https://twitter.com/SkyVerseNFT"
        target="_blank"
      >
        <img src="../assets/images/Skyverse.png" alt="Skyverse pfp" />
        <div class="name">Skyverse</div>
      </a>

      <a
        class="collaborator"
        href="https://twitter.com/KaijuKingz"
        target="_blank"
      >
        <img src="../assets/images/KaijuKingz.png" alt="Kaiju Kingz pfp" />
        <div class="name">Kaiju Kingz</div>
      </a>

      <a
        class="collaborator"
        href="https://twitter.com/RagnarokMeta"
        target="_blank"
      >
        <img src="../assets/images/RagnarokMeta.png" alt="Ragnarok Meta pfp" />
        <div class="name">Ragnarok Meta</div>
      </a>

      <a
        class="collaborator"
        href="https://twitter.com/Imaginary_Ones"
        target="_blank"
      >
        <img
          src="../assets/images/ImaginaryOnes.png"
          alt="Imaginary Ones pfp"
        />
        <div class="name">Imaginary Ones</div>
      </a>

      <a
        class="collaborator"
        href="https://twitter.com/Primatesnft"
        target="_blank"
      >
        <img src="../assets/images/Primates.png" alt="Primates pfp" />
        <div class="name">Primates</div>
      </a>

      <a
        class="collaborator"
        href="https://twitter.com/TheParallaxHQ"
        target="_blank"
      >
        <img src="../assets/images/Parallax.png" alt="Parallax pfp" />
        <div class="name">Parallax</div>
      </a>

      <a
        class="collaborator"
        href="https://twitter.com/DWC_NFT"
        target="_blank"
      >
        <img
          src="../assets/images/DWCCarbonPass.png"
          alt="DWC Carbon Pass pfp"
        />
        <div class="name">DWC Carbon Pass</div>
      </a>
    </div>
  </section>
</template>

<style lang="scss" scoped>
section {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 0 140px;
  h1 {
    margin-bottom: 0;
    font-family: Audiowide;
    font-size: 40px;
    font-weight: 400;
    line-height: 40px;
    text-align: center;
    text-transform: capitalize;
    background: $web3sg-gradient-main;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-fill-color: transparent;
    &.reflected {
      margin-bottom: 100px;
      margin-top: 0;
      filter: blur(1px);
      background: linear-gradient(
        90deg,
        rgba(255, 255, 255, 0.51) 0%,
        #9b5a6d 16.15%,
        #ffffff 50.99%,
        #92a0d4 75%,
        rgba(187, 202, 255, 0.5) 100%
      );
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      text-fill-color: transparent;
      opacity: 0.25;
    }
  }
  .collaborators {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    column-gap: 120px;
    justify-content: center;
    .collaborator {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin-bottom: 48px;
      img {
        width: 150px;
        margin-bottom: 18px;
      }
      .name {
        font-size: 28px;
        font-family: 'Turret Road';
        font-weight: 800;
        background: $web3sg-gradient-main;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
        text-fill-color: transparent;
        text-shadow: 0 0 4px rgba(255, 255, 255, 0.3);
        letter-spacing: 0.02em;
      }
    }
  }
}
</style>
