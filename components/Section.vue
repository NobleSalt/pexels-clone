<template>
  <div class="section">
    <div class="section__left">
      New Stock Photos
    </div>
    <ul class="section__left__right">
      <li role="tooltip">
        <a class="js-home-link js-home-trending" href="#">Trending</a>
      </li>
      <li role="tooltip">
        <a class="js-home-link js-home-new" href="#">New</a>
      </li>
      <li class="when-signed-in" role="tooltip">
        <a class="js-home-link js-home-following" href="#">Following</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.dropdown:focus-within .dropdown-menu {
  opacity: 1;
  // transform: translate(0) scale(1);
  visibility: visible;
}
.section {
  display: flex;
  padding: 0 2rem;
  justify-content: space-between;
  color: $nav_background;
  font-size: 1.125rem;
  text-transform: capitalize;
  line-height: 26px;
  font-weight: 500;
}
</style>
