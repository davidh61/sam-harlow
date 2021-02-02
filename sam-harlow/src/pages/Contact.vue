<template>
  <Layout>
    <h1>Contact</h1>

    <form
      method="post"
      action="https://www.flexyform.com/f/d1692555237541bb809b2009e477d86c693ab83c"
    >
      <p>
        <label>Fullname</label>
        <input type="text" name="fullname" />
      </p>
      <p>
        <label>Email</label>
        <input type="email" name="_reply_to" />
      </p>
      <button type="submit">Send</button>
    </form>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: "Contact",
  },
};
</script>
