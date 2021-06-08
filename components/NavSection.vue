<template>
  <div class="NavSection">
    <div class="links">
      <a href="#" class="active">home</a>
      <a href="#">discover</a>
      <a href="#">videos</a>
      <a href="#">leaderboard</a>
      <a href="#">challenges</a>
    </div>
    <hr />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.NavSection {
  width: 100vw;
  display: flex;
  overflow: auto;
  // white-space: nowrap;
  justify-content: center;
  // margin: auto;
  // padding: 0 1rem;

  .links {
    width: 7.5rem;
    overflow: auto;
    display: flex;
    justify-content: center;
    flex-grow: 1;
    padding: 0 25%;
    // padding: 0 2rem;
    // padding-left: 3rem;

    a {
      font-size: 1.125rem;
      text-transform: capitalize;
      line-height: 26px;
      font-weight: 500;
      margin: auto;
      margin-top: 0;
      margin-bottom: 0;
      letter-spacing: 0.4px;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 1.25rem;
      color: lighten($nav_background, 10);
      text-align: center;
      transition: all 400ms ease-in-out;

      &:hover {
        color: $color;
        // border: 2px solid $color;
      }

      &.active {
        border-bottom: 3px solid $color;
        color: $color;
        // border: 2px solid $color;
        border-bottom: 3px solid $color;
      }
    }

    hr {
      color: $color;
    }
  }
}

@media screen and (max-width: 849px) {
  .NavSection {
    .links {
    }
  }
}

@media screen and (max-width: 640px) {
  .NavSection {
    width: 100vw;
    display: flex;
    overflow: auto;
    // white-space: nowrap;
    justify-content: center;
    // margin: auto;
    // padding: 0 1rem;

    .links {
      width: 7.5rem;
      overflow: auto;
      display: flex;
      justify-content: flex-start;
      flex-grow: 1;
      padding: 0 2rem;
      // padding-left: 3rem;
    }
  }
}
// .NavSection{}
</style>
