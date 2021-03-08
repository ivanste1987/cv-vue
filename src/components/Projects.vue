<template>
  <div class="projects-component">
    <div class="projects-container">
      <div class="projects-text-container">
        <h3>Projects</h3>
        <p>Built from strach, responsive design, Maintenance of the website</p>
      </div>
      <div class="projects-lists">
        <div class="col">
          <div class="for-git">
            <i class="fab fa-github fa-9x"></i>
            <div class="list" onclick="">
              <ul>
                <li>
                  <a href="https://github.com/ivanste1987/task-app">Todo App</a>
                </li>
                <li>
                  <a href="https://github.com/ivanste1987/weather-website"
                    >Weather App</a
                  >
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="vanila-js">
            <i class="fab fa-js fa-9x"></i>
            <div class="list" onclick="">
              <ul>
                <li>
                  <a href="https://www.a101studio.com/">Architectural Studio</a>
                </li>
                <li>
                  <a href="http://unionconstruction.rs/"
                    >Construction Company</a
                  >
                </li>
                <li>
                  <a href="http://www.frizerskisalonraja.com/"
                    >Hairdressing Salon</a
                  >
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="wordpress">
            <i class="fab fa-wordpress fa-9x"></i>
            <div class="list" onclick="">
              <ul>
                <li>
                  <a href="https://nlptransfer.rs/">NLP Transfer</a>
                </li>
                <li>
                  <a href="https://steccadosso.com/">Handmaid Products</a>
                </li>
                <li>
                  <a href="https://curehub.io/">Consulting Services</a>
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="col"></div>
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
$jscolor: #d1bd26;
$githubcolor: #f04f33;
$wordpresscolor: #21759b;

.projects-component {
  padding: 5% 10%;
  .projects-container {
    width: 80%;
    height: auto;
    margin: 0 auto;
    display: felx;
    flex-direction: column;
    @media screen and(max-width: 1440px) {
      width: 100%;
    }
    .projects-text-container {
      h3,
      p {
        text-align: left;
      }
      p {
        width: 50%;
        @media screen and(max-width: 520px) {
          width: 100%;
        }
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
    }
    .projects-lists {
      display: grid;
      grid-template-columns: 50% 50%;
      grid-template-rows: 50% 50%;
      @media screen and(max-width: 1124px) {
        grid-template-columns: 100%;
        grid-template-rows: auto auto auto;
      }
      .col {
        height: 350px;
        position: relative;
        overflow: hidden;

        .for-git,
        .vanila-js,
        .wordpress {
          display: flex;
          align-items: center;
          justify-content: center;
          width: 100%;
          height: 100%;
          position: relative;
        }
        .for-git {
          background: $githubcolor;
        }
        .vanila-js {
          background: $jscolor;
        }
        .wordpress {
          background: $wordpresscolor;
        }
        i,
        .list {
          transition: all 0.5s ease;
        }
        i {
          @media screen and(max-width: 520px) {
            font-size: 100px;
          }
        }

        .list {
          position: absolute;
          width: 50%;
          right: 0%;
          transform: translate(100%);
          opacity: 0;
          ul {
            padding: 0;
            list-style: none;
            li {
              text-align: left;
              margin: 2%;
            }
          }
        }

        &:hover i {
          transform: translate(-70%);
           @media screen and(max-width: 520px) {
             transform: translate(-80%);
          }
        }
        &:hover .list {
          transform: translate(0%);
          opacity: 1;
           @media screen and(max-width: 520px) {
             transform: translate(-10%);
          }
        }
      }
    }
  }
}

@media screen and(max-width: 1124px) {
  .col:nth-last-child(1) {
    display: none;
  }
}
</style>