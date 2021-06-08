<template>
  <!-- <div class="Image p-3 lg:w-1/3 sm:w-1/2 "> -->
  <div
    class="Image"
    @mouseover="showSmall = true"
    @mouseleave="showSmall = false"
  >
    <img :style="{ height }" src="/hero.jpeg" alt="" />
    <!-- <img :style="{ height }" src="/hero.jpeg" alt="" /> -->
    <div class="ImageSmallSection p-2" :class="showSmall ? 'show' : ''">
      <div class="ImageSmallSectionLeft">
        <div class="img">
          <img src="/default.png" alt="" />
        </div>
        <span class="some">Emmanuel Izuchukwu</span>
      </div>
      <div class="ImageSmallSectionRight">
        <!-- <img src="/download.svg" alt="" /> -->
        <i class="download-icon"
          ><svg
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
            height="100px"
            width="100px"
            fill="#000000"
            version="1.1"
            x="0px"
            y="0px"
            viewBox="0 0 100 100"
            style="enable-background:new 0 0 100 100;"
            xml:space="preserve"
          >
            <g>
              <path
                d="M72.2,43.2L58,57.4V17c0-2.2-1.8-4-4-4s-4,1.8-4,4v40.4L35.8,43.2c-1.6-1.6-4.1-1.6-5.7,0c-1.6,1.6-1.6,4.1,0,5.7l21,21   C52,70.7,53,71,54,71s2-0.4,2.8-1.2l21-21c1.6-1.6,1.6-4.1,0-5.7C76.3,41.6,73.8,41.6,72.2,43.2z"
              ></path>
              <path
                d="M32,87h44c2.2,0,4-1.8,4-4s-1.8-4-4-4H32c-2.2,0-4,1.8-4,4S29.8,87,32,87z"
              ></path>
            </g>
          </svg>
        </i>
        <i class="download-icon"
          ><svg
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
            height="100px"
            width="100px"
            fill="#000000"
            version="1.1"
            x="0px"
            y="0px"
            viewBox="0 0 100 100"
            style="enable-background:new 0 0 100 100;"
            xml:space="preserve"
          >
            <g>
              <path
                d="M72.2,43.2L58,57.4V17c0-2.2-1.8-4-4-4s-4,1.8-4,4v40.4L35.8,43.2c-1.6-1.6-4.1-1.6-5.7,0c-1.6,1.6-1.6,4.1,0,5.7l21,21   C52,70.7,53,71,54,71s2-0.4,2.8-1.2l21-21c1.6-1.6,1.6-4.1,0-5.7C76.3,41.6,73.8,41.6,72.2,43.2z"
              ></path>
              <path
                d="M32,87h44c2.2,0,4-1.8,4-4s-1.8-4-4-4H32c-2.2,0-4,1.8-4,4S29.8,87,32,87z"
              ></path>
            </g>
          </svg>
        </i>
        <i class="download-icon"
          ><svg
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
            height="100px"
            width="100px"
            fill="#000000"
            version="1.1"
            x="0px"
            y="0px"
            viewBox="0 0 100 100"
            style="enable-background:new 0 0 100 100;"
            xml:space="preserve"
          >
            <g>
              <path
                d="M72.2,43.2L58,57.4V17c0-2.2-1.8-4-4-4s-4,1.8-4,4v40.4L35.8,43.2c-1.6-1.6-4.1-1.6-5.7,0c-1.6,1.6-1.6,4.1,0,5.7l21,21   C52,70.7,53,71,54,71s2-0.4,2.8-1.2l21-21c1.6-1.6,1.6-4.1,0-5.7C76.3,41.6,73.8,41.6,72.2,43.2z"
              ></path>
              <path
                d="M32,87h44c2.2,0,4-1.8,4-4s-1.8-4-4-4H32c-2.2,0-4,1.8-4,4S29.8,87,32,87z"
              ></path>
            </g>
          </svg>
        </i>
        <!-- <i class="fa fa-heart"></i> -->
        <i class="fa fa-heart"></i>
        <i class="fa fa-heart"></i>
      </div>
    </div>
  </div>
</template>

<script>
import Download from "~/static/download.svg";

export default {
  // components: { Download },
  props: ["height"],
  data() {
    return {
      showSmall: false
    };
  }
};
</script>

<style lang="scss" scoped>
.Image {
  // max-width: 300px;
  position: relative;
  // bottom: 1rem;
  height: fit-content;
  max-width: 100%;
  width: 100%;
  background-color: gray;
  margin-bottom: 1.25rem;
  overflow: hidden;
  z-index: 1;
  cursor: pointer;

  img {
    position: relative;
    width: 0px;
    min-width: 1000px;
    zoom: -1;
    height: auto;
  }

  &SmallSection {
    position: absolute;
    opacity: 0;
    transition: all 700ms ease;
    padding: 0 0.5rem;
    display: flex;
    justify-content: space-between;
    left: 0;

    &Left {
      display: flex;
      align-items: center;
      justify-self: flex-start;
      flex-grow: 1;
      width: 70%;

      .img {
        display: inline-block;
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background-color: #e8e8e8;
        overflow: hidden;

        img {
          margin-left: -2.5px;
          margin-top: -2px;
          width: 40px;
          height: 40px;
          min-width: 40px;
          display: inline-block;
          zoom: 1.25;
        }
      }

      .some {
        display: inline-block;
        font-size: 1rem;
        margin-right: 40px;
        margin-left: 5px;
        // white-space: nowrap;
        display: inline-block;
        vertical-align: middle;
        text-overflow: clip;
        overflow: hidden;
        color: #e8e8e8;
      }
    }

    &Right {
      display: flex;
      justify-content: flex-end;

      img {
        width: 40px;
        height: 40px;
      }

      i {
        display: inline-block;
        width: 1.75rem;
        height: 1.75rem;
        font-size: 1.75rem;
        color: white;
        svg {
          fill: #111;
          width: 1.75rem;
          height: 1.75rem;
        }
      }
    }
  }

  &SmallSection.show {
    opacity: 1;
    z-index: 1;
    display: flex;
    width: 100%;
    bottom: 0;
    justify-content: space-between;
    align-items: center;
    height: 5rem;
    transition: all 700ms ease;
  }

  &SmallSection.show::before {
    position: absolute;
    z-index: -1;
    content: "";
    left: 0;
    border-radius: 5px 5px 0 0;
    background-color: gray;
    opacity: 0.3;
    width: 100%;
    height: 100%;
  }
}

// @media screen and (max-width: 690px) {
//   .Image {
//     max-height: 500px;
//     position: relative;
//     // bottom: 1rem;
//     height: fit-content;
//     width: 100%;
//     background-color: gray;
//     margin-bottom: 1.25rem;
//     overflow: hidden;
//     z-index: 1;

//     img {
//       position: relative;
//       width: 0px;
//       // height: 500px;
//       vertical-align: middle;
//       margin: 0 auto;
//       zoom: -1;
//       height: auto;
//       // position: absolute;
//       // top: 0;
//       // bottom: 0;
//       // left: 0;
//       // right: 0;
//       // z-index: -1;
//     }

//     &SmallSection {
//       // position: absolute;
//       // z-index: 1;
//       // bottom: 0;
//       // opacity: 0;
//       // transition: all 700ms ease;
//     }

//     &SmallSection.show {
//       // position: absolute;
//       // opacity: 1;
//       // z-index: 1;
//       // bottom: 0;
//       // transition: all 700ms ease;
//     }
//   }
// }
</style>
