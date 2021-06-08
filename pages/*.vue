<template>
  <div>404</div>
</template>

<script>
export default {
  asyncData({ redirect }) {
    // return redirect("/");
  }
};
// export default {
//   // asyncData(e) {
//   //   const config = {
//   //     headers: {
//   //       Accept: 'application/json',
//   //     },
//   //   }
//   //   // console.log(e.$axios.get(''))
//   //   // console.log(process.env)
//   //   e.$axios.get('https://icanhazdadjoke.com/search', config).then((res) => {
//   //     // console.log(res.data)
//   //   })
//   // },
// }
</script>

<style lang="scss" scoped>
div {
  font-size: 10rem;
  text-align: center;
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  color: $nav_background;
}
</style>
