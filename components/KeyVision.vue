<script>
export default {
  methods: {
    a() {},
  },
}
</script>
<template>
  <div class="KeyVision">
    <div class="container">
      <div class="decorator-top">
        <div class="firecracker">
          <img src="~/assets/key_vision/firecracker.png" />
        </div>
        <div class="star">
          <img src="~/assets/key_vision/star.png" />
        </div>
      </div>
      <div class="content">
        <div class="circle">
          <img src="~/assets/key_vision/circle.png" />
        </div>
        <div class="main">
          <div class="text">
            <img src="~/assets/key_vision/feat,SDGS.png" />
          </div>
          <div class="share">
            <a class="line" href="#">
              <img src="~/assets/key_vision/line.png" />
              分享
            </a>
            <a class="fb" href="#">
              <img src="~/assets/key_vision/facebook.png" />
              分享
            </a>
          </div>
        </div>

        <div class="arrow">
          <img src="~/assets/key_vision/arrow.png" />
        </div>
      </div>
    </div>
    <div class="decorator-bottom">
      <div class="people">
        <div class="girl">
          <img src="~/assets/key_vision/girl.png" />
        </div>
        <div class="boy">
          <img src="~/assets/key_vision/boy.png" />
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss">
.KeyVision {
  position: relative;

  .container {
    padding-top: 100px;
    max-width: 1075px;
    margin-right: auto;
    margin-left: auto;
    position: relative;
    @include screen($lg) {
      padding-top: 60px;
    }
  }
  .decorator-top {
    display: flex;
    justify-content: space-between;
    position: absolute;
    width: 100%;
    @include screen($lg) {
      position: static;
    }
    @include screen($md) {
      padding-right: 20px;
      padding-left: 20px;
    }
    & > .firecracker,
    & > .star {
      max-width: 164px;
      animation: animate-zoom-in alternate infinite 1s ease-in-out;
      @include screen($md) {
        max-width: 15%;
      }
      @include screen($sm) {
      }
    }
  }
  .content {
    position: relative;
    & > .circle {
      max-width: 747px;
      margin-right: auto;
      margin-left: auto;
      animation: animate-circle-rotate infinite 10s linear;
      @include screen($md) {
        max-width: 371px;
      }
    }
    & > .main {
      top: 0;
      position: absolute;
      padding-top: 56px;
      width: 100%;
      @include screen($md) {
        padding-top: 0;
      }
      .text {
        margin-bottom: 22px;
        width: 100%;
        @include screen($md) {
          margin-bottom: 11px;
        }
        & > img {
          margin-right: auto;
          margin-left: auto;
          max-width: 426px;
          @include screen($md) {
            max-width: 234px;
          }
        }
      }
    }
    .share {
      display: flex;
      justify-content: center;
      & > a {
        width: 98px;
        height: 43px;
        font-size: 20px;
        color: #fff;
        border-radius: 100px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-weight: 400;
        margin-right: 19px;
        cursor: pointer;
        &:last-of-type {
          margin-right: 0;
        }
        & > img {
          margin-right: 4px;
        }
        @include screen($md) {
          width: 78px;
          height: 34px;
          font-weight: 500;
          line-height: 20px;
          font-size: 14px;
        }
      }
      & > .line {
        background-color: #06c755;
        & > img {
          max-width: 25px;
        }
      }
      & > .fb {
        background-color: #1877f2;
        & > img {
          max-width: 22px;
        }
      }
    }
    & > .arrow {
      max-width: 34px;
      margin: 59px auto;
      height: 444px;
      display: flex;
      align-items: center;
      animation: animate-slide 2s infinite alternate 0.3s ease-in-out;
      @include screen($md) {
        height: 239px;
      }
    }
  }

  .decorator-bottom {
    width: 100%;
    position: absolute;
    bottom: 0;
    & > .people {
      display: flex;
      width: 100%;
      justify-content: space-between;
      .girl,.boy{
        animation: animate-slide 2s alternate infinite ease-in-out;
      }
      .girl {
        max-width: 445px;
        @include screen($md) {
          max-width: 239px;
        }
      }
      .boy {
        max-width: 368px;
        @include screen($md) {
          max-width: 198px;
        }
      }
    }
  }
  @keyframes animate-circle-rotate {
    from {
      transform: rotate(0);
    }
    to {
      transform: rotate(360deg);
    }
  }
  @keyframes animate-zoom-in {
    from {
      transform: scale(1);
    }
    to {
      transform: scale(0.8);
    }
  }
  @keyframes animate-slide {
    from{
      transform: translateY(-30px);
    }
    to{
      transform: translateY(30px);
    }
  }
  
}
</style>
