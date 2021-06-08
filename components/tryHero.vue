<template>
  <div class="Hero">
    <!-- <img src="~/assets/hero.jpeg" class="Hero_img" /> -->

    <div class="Hero_section">
      <!-- <div class="center"> -->
      <h3 class="Hero_section_intro">
        The best free stock photos & videos shared by talented creators.
      </h3>
      <form action="" class="Hero_section_form">
        <input type="text" placeholder="search for free photos and videos" />
      </form>
      <ul>
        <li><span>Suggested: </span></li>
        <li><a href="#">creative, </a></li>
        <li><a href="#">cool, </a></li>
        <li><a href="#">love, </a></li>
        <li><a href="#">rain, </a></li>
        <li><a href="#">office, </a></li>
        <li><a href="#">city, </a></li>
        <li><a href="#">more</a></li>
      </ul>
      <!-- </div> -->
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
// $height: 700px;
.Hero {
  // height: $height;
  height: 100%;
  width: 100%;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  max-height: 500px;
  min-height: 380px;
  height: 500px;
  // margin: 0 1rem;
  padding: 0 1rem;
  // padding-top: 74px;
  // padding-bottom: 66px;

  img {
    height: 100%;
  }

  &_section {
    max-width: 700px;
    width: 100%;
    z-index: 1;
    // margin: auto;
    width: 100%;
    // padding: 0 1rem;
    // padding: 1.15rem;
    overflow: auto;

    // .center {
    display: inline-block;
    width: 650px;
    // padding-right: 0.5rem;

    ul {
      display: flex;
      color: white;
      white-space: pre;
      padding-top: 5px;

      li {
        a {
          opacity: 0.8;
        }
      }

      &:not(:first-child) {
        // opacity: 0.8;
        color: white;
        // white-space: normal;
        font-weight: 100;
      }
    }
    // }

    form {
      display: block;
      // width: 95%;
      width: 100%;
      background-color: white !important;
      border-radius: 5px;
      padding: 0.2rem 0.8rem;
      height: 3.5rem;

      input {
        background-color: rgba(255, 255, 255, 0.95) !important;
        width: 80%;
        font-size: 1.25rem;
        height: 100%;
        font-weight: 300;
        // background-color: red;
        outline: none;
        border: none;
        padding: 1rem;
        // color: $color-search-bar-placeholder;
        // color: white;

        &:focus-within {
          background-color: $color-search-bar-background-focus;
        }

        &::placeholder {
          background-color: $color-search-bar-background !important;
          text-transform: capitalize;
        }
      }
    }

    &_intro {
      width: 100%;
      font-family: -apple-system, BlinkMacSystemFont, segoe ui, roboto, oxygen,
        cantarell, helvetica neue, ubuntu, sans-serif;
      display: block;
      font-size: 38px;
      line-height: 48px;
      font-weight: 700;
      margin-top: 0;
      margin-bottom: 15px;
      color: white;
      text-align: left;

      font-size: 36px;
      line-height: 48px;
      font-weight: 700;
      margin-top: 0;
      margin-bottom: 15px;
    }
  }
}

.Hero::before {
  top: 0;
  width: 100%;
  height: 500px;
  left: 0;
  // max-height: 500px;
  min-height: 380px;
  position: absolute;
  background-image: url("~/assets/hero.jpeg");
  background-attachment: scroll;
  background-position: top;
  background-size: 100% 100%;
  content: "";
  z-index: -2;
  background-size: cover;
  background-repeat: no-repeat;
}

.Hero::after {
  content: "";
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background: rgba(0, 0, 0, 0.4);
  pointer-events: none;

  content: "";
  z-index: -1;
}
</style>
