<template>
  <Layout>
    <div class="content">
      <div class="text">
        <h1>Contact</h1>
        <form class="">

          <input type="text" name="name">
          <label for="">Name</label>
          <input type="email" name="email">
          <label for="">Email</label>
          <input type="text" name="subject">
          <label for="">Subject</label>
          <input type="text" name="message">
          <label for="">Message</label>
          <div class="btn_wrapper">
            <input class="btn" type="submit" name="submit" value="Submit">
          </div>
        </form>
      </div>
    </div>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Contact',
  }
}
</script>

<style scoped>
input[type=text], input[type=email] {
  background-color: rgb(240, 231, 218, 0);
  border: none;
  border-bottom: 1px solid #a39d94;
  font-size: 1.1rem;
  padding: 10px;
  width: 100%;
}

input[type=submit] {
  border: 1px solid #a39d94;
  cursor: pointer;
  font-size: 1.1rem;
  margin-top: 5vh;
  padding: 5px 40px;
  width: auto;
}
input[type=submit]:hover {
  background-color: #089b06;
  color: #FFFFFF;
  transition-duration: 0.2s;
  transition-timing-function: ease-in-out;
}

label {
  letter-spacing: 0.1rem;
  margin-bottom: 1.5vh;
  width: 100%;
}

.bg {
  background-image: url('../assets/background/contact.jpg');
}

.btn_wrapper {
  text-align: center;
}
</style>
