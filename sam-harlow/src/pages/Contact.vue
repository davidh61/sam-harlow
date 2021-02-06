<template>
  <Layout>
    <div class="container">
      <form
        method="post"
        action="https://www.flexyform.com/f/d1692555237541bb809b2009e477d86c693ab83c"
      >
        <div>
          <input type="text" placeholder="Name" name="fullname" />
        </div>
        <div>
          <input type="email" placeholder="Email" name="_reply_to" />
        </div>
        <div>
          <textarea name="message" placeholder="Message"> </textarea>
        </div>
        <button type="submit">Send</button>
      </form>
    </div>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: "Contact",
  },
};
</script>

<style lang="scss">
.container {
  display: flex;
  justify-content: space-between;
  justify-content: center;

  .form {

    .input {

    }

  }
}
</style>
