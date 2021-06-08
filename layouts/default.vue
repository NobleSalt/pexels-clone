<template>
  <div>
    <script
      src="https://kit.fontawesome.com/eb0781ffa9.js"
      crossorigin="anonymous"
    ></script>
    <Nuxt />
  </div>
</template>

<style>
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>

<script>
export default {
  head() {
    return {
      title: "Free Stock Photos · Pexels",
      meta: [
        {
          hid: "description",
          name: "description",
          content:
            "Free stock photos and videos you can use everywhere. ✓ High-quality ✓ 100% free ✓ No attribution needed"
        },
        {
          hid: "keywords",
          name: "keywords",
          content: "free stock photos, pexels, free, images"
        }
      ]
    };
  }
};
</script>
