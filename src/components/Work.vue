<template>
  <div class="work-component">
    <div class="work-container">
      <h3>Work Experience</h3>
      <div class="work-experience-container">
        <div class="col" v-for="job in jobs" :key="job.id">
          <h4>{{ job.position }}</h4>
          <span>{{ job.firm }}</span
          ><br />
          <span>{{ job.period }}</span>
          <p>{{ job.desc }}</p>
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
      jobs: dbdata.work,
    };
  },
};
</script>

<style lang="scss" scoped>
$darkPrimaryColor: #313131;
$darkSecondaryColor: #2c2c2c;
$terracotta: #be5347;
$yellow: #ffb633;
$fontColor: #fcfcfc;
.work-component {
  padding: 5% 10%;
  .work-container {
    width: 80%;
    height: auto;
    margin: 0 auto;
    display: felx;
    flex-direction: column;
    @media screen and(max-width: 1440px) {
      width: 100%;
    }
    h3,
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
      left: 0;
      background: $yellow;
      width: 100px;
      height: 5px;
      border-radius: 2.5px;
    }
    h3 {
      position: relative;
      margin-bottom: 50px;
      color: #ffffff;
    }
    h4{
      color: $yellow;
    }
    .work-experience-container {
      width: 100%; 
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      @media screen and(max-width: 800px) {
        flex-direction: column;
      }
      .col {
        width: 48%;
        margin: 1% 1% 1% 0;
        text-align: left;
        display: flex;
        flex-direction: column;
        justify-items: flex-start;
        @media screen and(max-width: 800px) {
           width: 100%;
          
        }
      }
    }
  }
}
</style>