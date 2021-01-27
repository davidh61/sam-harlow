<template>
  <Layout>
    <div class="container">
      <video controls>
        <source src="/Videos/plsss.mp4" type="video/mp4" />
      </video>
    </div>
  </Layout>
</template>

<script>
export default {};
</script>

<style lang="scss">
.container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  justify-content: center;
  video {
    width: 520px;

    // /* Small devices (portrait tablets and large phones, 600px and up) */
    @media only screen and (max-width: 600px) {
      width: 300px;
    }

    // /* Small devices (portrait tablets and large phones, 600px and up) */
    @media only screen and (min-width: 600px) {
      width: 320px;
    }

    /* Medium devices (landscape tablets, 768px and up) */
    @media only screen and (min-width: 768px) {
      width: 500px
    }

    // /* Large devices (laptops/desktops, 992px and up) */
    // @media only screen and (min-width: 992px) {...}

    // /* Extra large devices (large laptops and desktops, 1200px and up) */
    // @media only screen and (min-width: 1200px) {...}
  }
}
</style>
