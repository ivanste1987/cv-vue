<template>
  <div class="header-content">
    <div class="hello-text">
      <div class="logo-container">
        <div class="logo">
          <h2>IS</h2>
        </div>
      </div>
      <div class="text">
        <h4>hello,</h4>
        <h1>I'm Ivan</h1>
        <h3>Freelancer Web Developer</h3>
        <a :href="downloadCvPath" :download="cvFile" class="button"
          >Download CV</a
        >

        <div class="scrollDown">
          <i class="fas fa-mouse fa-3x"></i>
        </div>
      </div>
    </div>
    <div class="right">
      <img src="@/assets/images/rocket.svg" alt="img" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      downloadCvPath: "/pdf/Ivan_Stefanovic.pdf",
      cvFile: "Ivan_Stefanovic.pdf",
    };
  },
};
</script>

<style lang="scss">
$darkPrimaryColor: #313131;
$darkSecondaryColor: #2c2c2c;
$terracotta: #be5347;
$fontColor: #fcfcfc;
$yellow: #ffb633;
.header-content {
  display: grid;
  grid-template-columns: 60% 40%;
  @media screen and(max-width: 1120px) {
    padding: 5%;
  }

  .hello-text {
    position: relative;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-direction: column;
    @media screen and(max-width: 1120px) {
      background: $darkPrimaryColor;
      padding-left: 5%;
    }
    @media screen and(max-width: 420px) {
      background: transparent;
    }
    .logo-container {
      flex: 1;
      display: flex;
      justify-content: flex-start;
      align-items: center;
      max-width: 550px;
      width: 100%;
      .logo {
        padding-top: 10%;
        h2 {
          padding: 0 10px;
          background: $terracotta;
          color: $darkPrimaryColor;
          border: 1px solid $terracotta;
        }
      }
    }
    .text {
      max-width: 550px;
      width: 100%;
      z-index: 2;
      flex: 8;
      display: flex;
      justify-content: center;
      align-items: flex-start;
      flex-direction: column;
      text-align: left;

      h1 {
        color: $yellow;
      }
      .button {
        margin-top: 3rem;
        background: transparent;
        outline: none;
        padding: 1rem 1.5rem;
        color: $terracotta;
        border: 1px solid $terracotta;
        transition: all 0.35s ease;
        margin-right: 2%;
        @media screen and(max-width: 375px) {
          display: none;
        }
        &:hover {
          color: $fontColor;
          background: $terracotta;
        }
      }
    }
    .scrollDown {
      padding-top: 6rem;
      i {
        color: $terracotta;
        animation: scrollDown 2s ease forwards infinite;
        @media screen and(max-width: 620px) {
          display: none;
        }
      }
    }
  }

  .right {
    position: relative;
    background-image: url("../assets/images/home-bg1.svg");
    background-size: cover;
    background-position: bottom right;
    @media screen and(max-width: 620px) {
      background-image: none;
    }
    img {
      transform: rotateX(60deg);
      position: absolute;
      max-width: 400px;
      width: 100%;
      left: 0%;
      top: 0%;
      transform: translate(-40%, 5%);
      transition: all 0.5s ease;
      filter: drop-shadow(12px 12px 7px rgba(0, 0, 0, 0.5));
      z-index: 1;

      &:hover {
        filter: drop-shadow(8px 8px 7px rgba(0, 0, 0, 0.1));
      }
    }
  }
}
@keyframes scrollDown {
  0% {
    transform: translateY(100%);
  }
  50% {
    transform: translateY(0%);
  }
  100% {
    transform: translateY(100%);
  }
}
</style>