<template>
  <div class="nav__show__mobile" :class="!drop ? 'd-none' : ''">
    <a href="#" class="hover__show" data-for="one_-1">
      <div class="side d-none" id="one_-1"></div>
      Home</a
    >
    <hr />
    <a href="#" class="hover__show one" data-for="one_1">
      <div class="side d-none" id="one_1"></div>
      login
    </a>
    <a href="#" class="hover__show one" data-for="one_2">
      <div class="side d-none" id="one_2"></div>
      join
    </a>
    <a href="#" class="hover__show one" data-for="one_3">
      <div class="side d-none" id="one_3"></div>
      change language</a
    >
    <a href="#" class="hover__show one" data-for="one_4">
      <div class="side d-none" id="one_4"></div>
      license
    </a>
    <hr />
    <a href="#" class="hover__show two" data-for="two_1">
      <div class="side d-none" id="two_1"></div>
      Apps and ps plugins
    </a>
    <a href="#" class="hover__show two" data-for="two_2">
      <div class="side d-none" id="two_2"></div>
      FAQ
    </a>
    <a href="#" class="hover__show two" data-for="two_3">
      <div class="side d-none" id="two_3"></div>
      about us
    </a>
    <a href="#" class="hover__show two" data-for="two_4">
      <div class="side d-none" id="two_4"></div>
      Imprint & terms
    </a>
    <div class="nav__socials">
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
</template>

<script>
export default {
  props: ["drop"]
};
</script>

<style></style>
