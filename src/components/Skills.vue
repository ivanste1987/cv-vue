<template>
  <div class="skills-component">
    <div class="skills-container">
      <h3>Some Skills</h3>
      <div class="lang-icons">
        <div><i class="fab fa-vuejs fa-4x"></i><span>Vue.js</span></div>
        <div><i class="fab fa-js fa-4x"></i><span>JavaScript</span></div>
        <div><i class="fab fa-node fa-4x"></i><span>Node.js</span></div>
        <div><i class="fab fa-html5 fa-4x"></i><span>HTML5</span></div>
        <div><i class="fab fa-css3-alt fa-4x"></i><span>CSS3</span></div>
        <div><i class="fab fa-sass fa-4x"></i><span>SCSS</span></div>
        <div>
          <i class="fas fa-database fa-4x"></i><span>MySql<br />Monogdb</span>
        </div>
        <div><i class="fab fa-wordpress fa-4x"></i><span>Wordpress</span></div>
        <div><i class="fab fa-github fa-4x"></i><span>GitHub</span></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
$darkPrimaryColor: #313131;
$darkSecondaryColor: #2c2c2c;
$terracotta: #be5347;
$fontColor: #fcfcfc;
$yellow: #ffb633;

$vuejscolor: #41b883;
$gitcolor: #f05033;
$jscolor: #f7df1e;
$wordpresscolor: #21759b;
$sasscolor: #cd6799;
$csscolor: #264de4;
$htmlcolor: #e44d26;
$nodejscolor: #90c53f;

.skills-component {
  background: $darkPrimaryColor;
  padding: 5% 10%;
  text-align: right;
  .skills-container {
    width: 80%;
    height: auto;
    margin: 0 auto;
    display: felx;
    flex-direction: column;

    @media screen and(max-width: 1440px) {
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
       @media screen and(max-width: 800px) {
       text-align: left;
      }
    }

    .lang-icons {
      display: flex;
      justify-content: flex-end;
      flex-wrap: wrap;
       @media screen and(max-width: 800px) {
        justify-content: flex-start;
      }
      div {
        flex: 1;
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        margin: 1%;
        &:hover span {
          transform: translateY(0%);
          opacity: 1;
        }
        &:hover .fa-vuejs {
          color: $vuejscolor;
        }
        &:hover .fa-js {
          color: $jscolor;
        }
        &:hover .fa-node {
          color: $nodejscolor;
        }
        &:hover .fa-html5 {
          color: $htmlcolor;
        }
        &:hover .fa-css3-alt {
          color: $csscolor;
        }
        &:hover .fa-sass {
          color: $sasscolor;
        }
        &:hover .fa-wordpress {
          color: $wordpresscolor;
        }
        &:hover .fa-github {
          color: $gitcolor;
        }
        span {
          margin-top: 1%;
          transform: translateY(-100%);
          opacity: 0;
          transition: all 0.5s ease;
        }
        i {
          transition: all 0.5s ease;
          margin: 2.5%;
        }
      }
    }
  }
}
</style>