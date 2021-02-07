<template>
  <Layout>
    <div class="container">
      <form
        method="post"
        action="https://www.flexyform.com/f/d1692555237541bb809b2009e477d86c693ab83c"
      >
        <div>
          <input type="text" placeholder="Name" name="fullname" required />
        </div>
        <div>
          <input type="email" placeholder="Email" name="_reply_to" required />
        </div>
        <div>
          <textarea name="message" placeholder="Message" required> </textarea>
        </div>
        <button type="submit">SEND</button>
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

  form {
    max-width: 400px;
    width: 100%;

    input,
    textarea,
    button {
      resize: none;
      width: 100%;
      box-sizing: border-box;
      padding: 12px 20px;
      margin: 8px 0;
      border: 2px solid #2a2a2a;
      border-radius: 4px;
      font-size: 15px;
      font-family: inherit;
    }

    textarea {
      height: 100px;
    }

    button {
      cursor:pointer;
      font-size: 20px;
      color: white;
      background-color: #2a2a2a;
      transition: all 0.25s ease;


      &:focus {
        background-color: grey;
      }
    }
  }
}
</style>
