<template>
  <div class="footer">
    <div class="footer-container">
      <h3>Contact me</h3>
      <div class="contacts">
        <div class="con">
          <h6>Email</h6>
          <br />
          <div>
            <a href="mailto: ivan.ste1987@gmail.com">ivan.ste1987@gmail.com</a>
          </div>
        </div>

        <div class="con">
          <h6>Phone</h6>
          <br />
          <div>
            <a href="tel: +381652094581">+381(65)/209-45-81</a>
          </div>
        </div>
      </div>
      <div class="contacts">
        <div class="con">
          <h6>Social Networks</h6>
          <br />
          <div>
            <a href="https://www.instagram.com/accounts/password/reset/"><i class="fab fa-instagram fa-2x"></i></a>
            <a href="https://www.linkedin.com/in/ivan-stefanovi%C4%87-60267bb0/"><i class="fab fa-linkedin fa-2x"></i></a>
          </div>
        </div>
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

.footer {
  background: $darkSecondaryColor;
  padding: 5% 10%;
  .footer-container {
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
      text-align: left;
    }
    .contacts {
      display: flex;
      margin-top: 5%;
      @media screen and(max-width: 800px) {
        flex-direction: column;
        .con:nth-child(2) {
          display: none;
        }
      }
      .con {
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: left;
        margin-right: 5%;
        @media screen and(max-width: 800px) {
          margin-bottom: 5%;
        }
        h6 {
          color: $yellow;
        }

        div {
          display: flex;
          align-items: center;
          i {
            margin-right: 1rem;
            transition: all 0.35s ease;
          }
          .fa-linkedin:hover {
            color: #0276a8;
          }
          .fa-instagram:hover {
            color: #c13584;
          }
        }
      }
    }
  }
}
</style>