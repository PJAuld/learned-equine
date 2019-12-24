<template>
  <g-link :to="`blog/${id}`">
    <li>
      <div class="img_wrapper">
        <g-image class="img" :src="randomImage()"></g-image>
      </div>
      <h4>{{ title }}</h4>
      <p>{{ shortenText(body) }}</p>
    </li>
  </g-link>
</template>

<script>


export default {
  name: 'BlogPost',
  props: {
    body: {type: String},
    id: {type: String},
    title: {type: String},
  },
  methods: {
    randomImage() {
      const randomEnd = (Math.random() * 100).toFixed(0);
      const randomDims = `3${randomEnd}x3${randomEnd}`;
      return `https://source.unsplash.com/random/${randomDims}`;
    },
    shortenText(text) {
      return text.slice(0, 30) + '...';
    }
  }
}
</script>

<style scoped>
a {
  border: 1px solid #a39d94;
  border-radius: 1%;
  color: inherit;
  padding: 5%;
  margin: 1%;
}

a:hover {
  background-color: #f1ede1;
  transition-duration: 0.3s;
  transition-timing-function: ease-in-out;
}

h4 {
  padding-top: 10px;
}

li {
  list-style: none;
}

.img {
  min-height: 100%;
  min-width: 100%;
  position: absolute;
  width: 100%;
}

.img_wrapper {
  margin: auto;
  overflow: hidden;
  padding-bottom: 90%;
  position: relative;
  width: 90%;
}
</style>
