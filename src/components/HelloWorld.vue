<template>
  <div class="hello">
    <div class="col-md-12">
      <div class="col-md-6 part_1">
        <img src="../assets/logo.png" alt="logo">
      </div>
      <div class="col-md-6 part_2">
        <div class="text">
          <a href="#">
            <h3>+7(499)777-77-77</h3>
          </a><a href="#">
            <h3>+7(499)777-77-77</h3>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data() {
      return {

      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @font-face {
    font-family: 'Myriad_Pro';
    src: url("../fonts/Myriad_Pro.ttf") format("truetype");
  }

  .hello {
    background-color: rgba(128, 128, 128, 0.479);
    background-size: cover;
    width: 100%;
    height: 13rem;
    display: flex;

    .col-md-12 {
      width: 1000px;
      display: flex;

      .part_1 {
        img {
          margin-left: 50%;
          margin-top: 7%;
          width: auto;
          height: auto;
        }
      }

      .part_2 {
        .text {
          margin-left: 15%;
          margin-top: 8%;

          a {
            color: gray;
            text-decoration: none;

            h3 {
              font-size: 170%;
              font-family: 'Myriad_Pro';
            }
          }
        }
      }
    }
  }

  @media (min-width:300px) and (max-width:820px) {
    .hello {
      height: 10rem;

      .col-md-12 {
        .part_1 {
          img {
            width: 100%;
            height: auto;
            margin-top: 30%;
            margin-left: 15%;
          }
        }

        .part_2 {
          .text {
            margin-top: 33%;

            a {
              h3 {
                font-size: 80%;
              }
            }
          }
        }
      }
    }
  }

  @media (min-width:768px) and (max-width:1023px) {
    .hello {
      .col-md-12 {
        .part_1 {
          img {
            width: 70%;
            margin-top: 8%;
            margin-left: 40%;
          }
        }

        .part_2 {
          .text {
            margin-top: 12%;

            a {
              h3 {
                font-size: 130%;
              }
            }
          }
        }
      }
    }
  }

  @media (min-width:1024px) and (max-width:1370px) {
    .hello {
      .col-md-12 {
        .part_1 {
          img {
            margin-top: 10%;
          }
        }

        .part_2 {
          .text {
            margin-top: 11%;
          }
        }
      }
    }
  }

  @media (min-width:1920px) {
    .hello {
      height: 15rem;
    }
  }

  @media (min-width:2500px) {
    .hello {
      width: 170rem;
      height: 17rem;

      .col-md-12 {
        .part_1 {
          img {
            width: 30%;
            margin-top: 5%;
          }
        }

        .part_2 {
          .text {
            margin-top: 6%;

            a {
              h3 {
                font-size: 250%;
              }
            }
          }
        }
      }
    }
  }
</style>