<template>
  <nav class="nav p-2" :class="scrolled ? 'scrolled' : ''">
    <a href="/" title="Free Stock Photos" class="nav__logo">
      <div class="nav__logo__img mr-2">
        <Logo />
      </div>
      <div class="nav__logo__name">Pexels</div>
    </a>
    <div class="nav__search" :class="!scrolled ? 'd-none' : ''">
      <div
        :class="clicked ? 'focus' : ''"
        @click.prevent="clicked = true"
        @mouseout="clicked = false"
      >
        <input
          type="text"
          placeholder="Search for free photos"
          :class="!scrolled ? 'd-none' : ''"
        />
        <i :class="!scrolled ? 'd-none' : ''">s</i>
      </div>
    </div>
    <div class="nav__mobile__menu" @click="$emit('dropped')">
      <div></div>
    </div>
    <ul class="nav__links">
      <span
        class="nav__links__explore pop hide__mobile"
        @mouseover="handleHover({ name: 'explore', value: true })"
        @mouseleave="handleHover({ name: 'explore', value: false })"
      >
        explore
        <div
          class="pop__over"
          :class="hover.explore ? 'd-none' : ''"
          id="explore"
        >
          <div class="pop__over__content">
            <a href="#">discover photos</a>
            <a href="#">popular searches</a>
            <a href="#">leaderboard</a>
            <a href="#">challenges</a>
            <a href="#">free videos</a>
            <a href="#">pexels blog</a>
          </div>
        </div>
      </span>

      <a href="#" class="hide__mobile">license</a>
      <a href="#" class="hide__mobile">upload</a>

      <span
        class="nav__links__dot pop"
        @mouseover="handleHover({ name: 'dot', value: true })"
        @mouseleave="handleHover({ name: 'dot', value: false })"
      >
        . . .
        <div class="pop__over" :class="hover.dot ? 'd-none' : ''">
          <div class="pop__over__content">
            <a href="#">login</a>
            <a href="#">join</a>
            <a href="#">change language</a>
            <a href="#">image & video API</a>
            <a href="#">apps & plugins</a>
            <a href="#">FAQ</a>
            <a href="#">partnerships</a>
            <a href="#">imprint & terms</a>
            <div class="pop__socials">
              <a href="#"><i class="fab fa-instagram"></i></a>
              <a href="#">
                <i class="fab fa-twitter"></i>
              </a>
              <a href="#">
                <i class="fa fa-facebook" aria-hidden="true"></i>
              </a>
              <a href="#">
                <i class="fa fa-pinterest-p" aria-hidden="true"></i>
              </a>
              <a href="#">
                <i class="fa fa-youtube"></i>
              </a>
            </div>
          </div>
        </div>
      </span>

      <a href="#" class="join">join</a>
    </ul>
  </nav>
</template>

<script>
export default {
  props: ["scrolled"],
  data() {
    return {
      clicked: false,
      hover: {
        explore: false,
        dot: false
      }
    };
  },
  methods: {
    handleHover(value) {
      switch (value.name) {
        case "explore":
          this.hover.explore = value.value;
          break;
        case "dot":
          this.hover.dot = value.value;
          break;
        default:
          break;
      }
    }
  }
};
</script>

<style lang="scss">
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.nav {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: space-between;
  padding: 0.5rem 1rem;
  text-transform: capitalize;
  align-items: center;
  height: 4rem;
  background-color: transparent;
  z-index: 20;
  color: white;

  * {
    // color: white;
    // color: $nav_background;
    text-decoration: none;
  }

  &__mobile__menu {
    display: none;
    div,
    &::before,
    &::after {
      background-color: white;
    }
  }

  &__logo {
    font-size: 1rem;
    // width: fit-content;
    display: flex;
    align-items: center;

    &__img {
      width: 2rem;
      svg {
        border-radius: 8px;
        height: 40px;
        width: 40px;
      }
    }

    &__name {
      // display: inline-block;
      margin-left: 1rem;
      font-size: 19px;
      line-height: 1;
      font-weight: 600;
    }
  }

  &__search {
    flex-grow: 1;
    div {
      height: 2.7rem;
      // width: 30rem;
      background-color: white;
      opacity: 0.9;
      border-radius: 0.3rem;
      padding: 1rem;
      margin: auto 10px;
      display: flex;
      justify-content: space-between;
      align-items: center;

      input {
        height: 100%;
        width: 90%;
        background-color: transparent;
        border: none;
        outline: none;
        font-size: 1rem;

        // // position: relative;
        color: #1a1a1a;
        padding: 0.9rem 0.7rem;
        // font-weight: 300;
        font-size: 17px;
        line-height: 22px;
      }
      // input:focus {
      //   background-color: lighten($color: grey, $amount: 100);
      // }
      i {
        // width: 25%;
        color: lighten($color: grey, $amount: 0);
        cursor: pointer;
      }
    }
  }

  &__search {
    .focus {
      background-color: white;
      opacity: 1;
    }
  }

  &__links {
    display: flex;
    align-items: center;

    & > * {
      margin-right: 2rem;
      display: block;
      font-size: 17px;
      line-height: 1;
      font-weight: 400;
      margin-top: 0;
      margin-bottom: 0;
      // color: $color-foreground;
      background: 0 0;
      padding: 0;
      box-shadow: none;
      border: none;
      border-radius: 4px;
      white-space: nowrap;
      cursor: pointer;
      transition: 0.1s opacity ease;

      &:hover {
        opacity: 0.75;
      }
    }

    .join {
      margin-right: 0;
      background-color: $button_background;
      padding: 0.75rem 1.5rem;
      transition: all 200ms ease;
      color: #fff;
      padding: 0.8rem 2rem;
      transition: 0.1s transform ease;
      transition: 0.1s transform ease, 0.1s -webkit-transform ease;
      font-weight: 600;

      &:hover {
        // box-shadow: 0 0px 5px white;
        // color: white;
        transform: translateY(-1px);
      }
    }

    &__explore {
      position: relative;

      &:hover {
        opacity: 1 !important;
      }
    }

    &__dot {
      padding-bottom: 2.5%;
      font-weight: bolder;
      font-size: larger;
      position: relative;

      &:hover {
        opacity: 1 !important;
      }

      .dot {
        // display: none;
      }
    }
  }
}

.nav.scrolled {
  background-color: $nav_background;
  color: white;

  .nav__mobile__menu {
    div,
    &::before,
    &::after {
      background-color: white;
    }
  }

  * {
    color: white;
  }

  input {
    color: $nav_background;
  }
}

#dot > div {
  // box-shadow: 0 3px 5px 10px 1px grey;
  border-radius: 4px;
  box-shadow: 0 0 8px #95979d;
}

.pop__over {
  position: absolute;
  display: none;
  top: 0.5rem;
  right: 0;
  max-width: 400px;
  width: 300px;
  // height: fit-content;
  font-weight: normal;
  font-size: medium;
  line-height: 1.5;
  color: gray !important;
  transition: all 400ms ease-in-out;
  padding: 1rem 0.2rem;

  &.d-none {
    display: block;
  }

  &__content {
    background-color: $color-foreground;
    margin: 1rem 0.2rem;
    border-radius: 6px;
    padding: 0.5rem;
    text-align: justify;
    // box-shadow: 0 0 5px;
    border-radius: 4px;
    box-shadow: 0 0 8px #95979d;

    > a {
      color: gray !important;
      display: block;
      padding: 0.35rem;

      &:hover {
        background-color: gray !important;
        color: white !important;
        opacity: 1 !important;
      }
    }

    .pop__socials {
      position: static;
      justify-content: space-between;
      display: flex;
      background-color: white;
      color: black;
      opacity: 1;
      border-radius: 6px;
      align-items: center;
      // padding-bottom: 1rem;
      margin-top: 1rem;

      a {
        position: relative;
        color: $nav_background !important;
        display: inline-block;
        font-size: 2rem;
        padding: 0.25rem 0.5rem;
      }

      a:hover {
        color: white !important;
        background-color: $nav_background;
      }
    }
  }
}

@media screen and (max-width: 880px) {
  .nav {
    &__logo {
      font-size: 1rem;
      // width: fit-content;
      display: flex;
      align-items: center;

      &__img {
        width: 2rem;
        svg {
          border-radius: 8px;
          height: 40px;
          width: 40px;
        }
      }

      &__name {
        // display: inline-block;
        margin-left: 1rem;
        font-size: 19px;
        line-height: 1;
        font-weight: 600;
      }
    }

    &__links {
      .hide__mobile {
        display: none;
      }
    }
  }
}

.nav__show__mobile.d__none {
  display: none;
}

.nav__show__mobile.scrolled {
  display: none;
}

@media screen and (max-width: 800px) {
  .nav {
    &__logo {
      font-size: 1rem;
      // width: fit-content;
      align-items: center;
      margin-right: 0.5rem;

      &__img {
        width: 2rem;
        svg {
          border-radius: 8px;
          height: 40px;
          width: 40px;
        }
      }

      &__name {
        display: none;
        // display: inline-block;
        margin-left: 1rem;
        font-size: 19px;
        line-height: 1;
        font-weight: 600;
      }
    }

    &__mobile__menu {
      display: inline-block;
      position: relative;
      width: 28px;
      height: 24px;
      cursor: pointer;
      opacity: 0.9;
      transition: all 100ms ease-in-out;

      div,
      &::before,
      &::after {
        background-color: white;
        position: absolute;
        content: "";
        width: 100%;
        height: 3px;
        z-index: 1;
        border-radius: 6px;
      }

      &::before {
        top: 0;
      }

      div {
        top: 42%;
      }

      &::after {
        bottom: 0;
      }
    }

    &__mobile__menu:hover {
      opacity: 0.7;
    }

    &__links {
      display: none;

      .hide__mobile {
        display: none;
      }

      & > * {
        margin-right: 2rem;
        display: block;
        font-size: 17px;
        line-height: 1;
        font-weight: 400;
        margin-top: 0;
        margin-bottom: 0;
        background: 0 0;
        padding: 0;
        box-shadow: none;
        border: none;
        border-radius: 4px;
        white-space: nowrap;
        cursor: pointer;
        transition: 0.1s opacity ease;

        &:hover {
          opacity: 0.75;
        }
      }

      .join {
        // margin-right: 0;
        // background-color: $button_background;
        // padding: 0.75rem 1.5rem;
        // transition: all 200ms ease;

        &:hover {
          // box-shadow: 0 0px 5px white;
          // color: white;
          transform: translateY(-1px);
        }
      }

      &__explore {
        position: relative;

        &:hover {
          opacity: 1 !important;
        }
      }

      &__dot {
        padding-bottom: 2.5%;
        font-weight: bolder;
        font-size: larger;
        position: relative;

        &:hover {
          opacity: 1 !important;
        }

        .dot {
          // display: none;
        }
      }
    }
  }

  .nav.scrolled {
  }

  .nav__show__mobile {
    // display: none;
    text-transform: capitalize;
    width: 100%;
    min-height: 110vh;
    height: 100vh;
    overflow-y: auto;
    padding: 1rem 1rem;
    background-color: $nav_background;
    position: fixed;
    top: 0rem;
    padding-top: 4rem;
    bottom: 0;
    z-index: 2;
    padding-bottom: 12rem;
    line-height: 2.5;

    font-size: 22px;
    font-weight: 400;

    a {
      display: block;
      color: white;
      text-decoration: none;
      position: relative;
      z-index: 1;
      opacity: 0.7;

      .side {
        background-color: gray;
        position: absolute;
        width: 0.5rem;
        background-color: white;
        left: -0.75rem;
        margin: 5px 0;
        content: "";
        z-index: 12;
        top: 0;
        bottom: 0;
        border-radius: 0 6px 6px 0;
      }

      .side.d__none {
        display: none;
      }
    }

    a:hover {
      opacity: 1;
    }
  }

  .nav__show__mobile.d__none {
    display: block;
  }

  .nav__socials {
    display: flex;
    justify-content: space-between;
    align-items: center;
    // height: 2rem;
    position: fixed;
    padding: 0.5rem 1rem;
    bottom: 0;
    right: 0;
    left: 0;
    // background-color: gray;
    font-size: 1.5rem;
    color: white;
    opacity: 1 !important;
    border-top: 1px solid white;
    background-color: $nav_background;

    a {
      // color: white !important;
      opacity: 1 !important;
      display: inline-block;
    }
  }
}
</style>
