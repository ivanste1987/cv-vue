<template>
  <div class="education-component">
    <div class="education-container">
      <h3>Education</h3>
      <div class="education-content">
        <div class="col" v-for="edu in education" :key="edu.id">
          <h4>{{ edu.school }}</h4>
          <span>{{ edu.dep }}</span
          ><br />
          <span>{{ edu.lang }}</span
          ><br />
          <p>{{ edu.year }}</p
          ><br />
          <span
            ><a :href="edu.link" v-if="edu.link" class="btn"
              >Check out</a
            ></span
          >
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
      education: dbdata.education,
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
.education-component {
  background: $darkPrimaryColor;
  padding: 5% 10%;
  .education-container {
    width: 80%;
    height: auto;
    margin: 0 auto;
    display: felx;
    flex-direction: column;
    @media screen and(max-width: 1440px) {
      width: 100%;
    }

    p {
      text-align: left;
    }
    p {
      width: 100%;
    }

    h3::before {
      content: "";
      position: absolute;
      bottom: -50%;
      right: 0;
      background: $yellow;
      width: 100px;
      height: 5px;
      border-radius: 2.5px;
      @media screen and(max-width: 800px) {
        left: 0;
      }
    }
    h3 {
      position: relative;
      margin-bottom: 50px;
      color: #ffffff;
      text-align: right;
      @media screen and(max-width: 800px) {
        text-align: left;
      }
    }
     h4{
      color: $yellow;
    }
    .education-content {
      display: grid;
      grid-template-columns: 50% 50%;
      grid-template-rows: auto auto;
      @media screen and(max-width: 800px) {
        display: flex;
        flex-direction: column;
      }
      .col {
        margin: 1% 1% 4%;
        text-align: left;
        padding-bottom: 1%;

        .btn {
          margin-top: 3rem;
          background: transparent;
          outline: none;
          padding: 1rem 1.5rem;
          color: $terracotta;
          border: 1px solid $terracotta;
          transition: all 0.35s ease;
          margin-top: 2%;
          text-transform: uppercase;
          font-weight: 600;
          &:hover {
            color: $fontColor;
            background: $terracotta;
          }
        }
        @media screen and(max-width: 800px) {
          margin: 5% 0 4%;
        }
      }
    }
  }
}
</style>