<template>
  <div class="aboutme-component">
    <div class="aboutme-content">
      <div class="row">
        <div class="img-container">
          <figure>
            <img
              src="https://via.placeholder.com/150x250"
              alt="Profile picture"
            />
          </figure>
        </div>
      </div>
      <div class="row">
        <div class="aboutme-text">
          <h3>About Me</h3>
          <p>{{ aboutText }}</p>
          <div class="buttos-container">
            <a :href="downloadCvPath" :download="cvFile" class="button">Download CV</a>
        
          </div>
        </div>
      </div>
      
    </div>
   
  </div>
</template>

<script>
import dbdata from "../data.js";
export default {
  data() {
    return {
      aboutText: dbdata.about.text,
      downloadCvPath: '/pdf/Ivan_Stefanovic.pdf' ,
      cvFile: 'Ivan_Stefanovic.pdf'
    };
  },
 
};
</script>

<style lang="scss" scoped>
$darkPrimaryColor: #313131;
$darkSecondaryColor: #2c2c2c;
$terracotta: #be5347;
$fontColor: #fcfcfc;
$yellow: #ffb633;
.aboutme-component {
  padding: 10%;
  background-color: $darkPrimaryColor;
  @media screen and(max-width: 1124px) {
    padding: 5%;
  }
  .aboutme-content {
    width: 80%;
    height: auto;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 50% 50%;
    grid-template-rows: auto;
    @media screen and(max-width: 1440px) {
      width: 100%;
    }
    @media screen and(max-width: 1124px) {
      display: flex;
      flex-direction: column-reverse;
    }
  }
  .row {
    display: flex;
    flex-direction: column;
    justify-content: center;
    @media screen and(max-width: 1124px) {
      padding: 5%;
    }

    .img-container {
      position: relative;
      &:hover figure::before {
        transform: translate(1%, -1%);
      }
      &:hover img {
        transform: translate(-1%, 1%);
        @media screen and(max-width: 1124px) {
          transform: translate(0%, 0%);
        }
      }
      figure::before {
        content: "";
        position: absolute;
        top: 10%;
        left: -15%;
        border: 20px solid $yellow;
        width: 95%;
        height: 95%;
        z-index: -1;
        transition: all 0.5s ease;

        @media screen and(max-width: 870px) {
          display: none;
        }
      }
      figure {
        position: relative;
        width: 400px;
        height: 500px;
        margin: 0 auto;
        z-index: 0;
        @media screen and(max-width: 520px) {
          max-width: 100%;
          width: 100%;
          height: auto;
        }

        img {
          width: 100%;
          height: 100%;
          transition: all 0.5s ease;
        }
      }
    }
    .aboutme-text {
      display: flex;
      flex-direction: column;
      justify-content: center;
    }
    h3,
    p,
    .buttos-container {
      text-align: left;
      z-index: 2;
      
      @media screen and(max-width: 520px) {
        button:nth-child(1) {
          display: none;
        }
      }
    }
    p{
      margin-bottom:3rem; 
    }
    h3::before {
      content: "";
      position: absolute;
      bottom: -50%;
      left: 0;
      background: $yellow;
      width: 100px;
      height: 5px;
      border-radius: 2.5px;
      //z-index: -1;
    }
    h3 {
      position: relative;
      margin-bottom: 50px;
      color: #ffffff;
    }
    .button {
      margin-top: 3rem;
      background: transparent;
      outline: none;
      padding: 1rem 1.5rem;
      color: $terracotta;
      border: 1px solid $terracotta;
      transition: all 0.35s ease;
      
      &:hover {
        color: $fontColor;
        background: $terracotta;
      }
    }
  }
}
</style>