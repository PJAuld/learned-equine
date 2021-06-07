<template>
  <div>
    <div class="content_title">
      <h1 class="title main">Learned Equine</h1>
      <h4 class="title sub">It's pronounced "Learn-ed"</h4>
    </div>
    <div class="content">
      <div class="text">
        <div class="showcase_grid">
          <div class="showcase1 grid_item img_wrapper">
            <image class="img" src="~/assets/images/kellie.jpg" />
          </div>
          <div class="showcase2 grid_item img_wrapper">
            <image class="img" src="~/assets/images/lita_3.jpg" />
          </div>
          <div class="showcase3 grid_item img_wrapper">
            <image class="img reposition" src="~/assets/images/obi_2.jpg" />
          </div>
          <div class="showcase4 grid_item img_wrapper">
            <image class="img" src="~/assets/images/parker_jovi_2.jpg" />
          </div>
          <div class="showcase5 grid_item img_wrapper">
            <image class="img" src="~/assets/images/pumpkin.jpg" />
          </div>
          <div class="showcase6 grid_item img_wrapper">
            <image class="img" src="~/assets/images/lita_2.jpg" />
          </div>
        </div>
        <h2>Recent Posts</h2>
        <ul>
          
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
h2 {
  text-align: center;
}

ul {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}

.bg {
  background-image: url('../assets/background/index.jpg');
}

.content_title {
  margin-bottom: 55vh;
  position: relative;
  width: 100%;
}

.main {
  font-family: Garamond;
  font-size: 3rem;
  font-weight: bold;
}

.sub {
  font-style: italic;
}

.text {
  padding: 5vh 5%;
}

.title {
  color: #FFFFFF;
  text-align: center;
}

.showcase_grid {
  align-items: stretch;
  display: grid;
  grid-template-areas:
    'a a a a b b b b c c'
    'a a a a b b b b c c'
    'a a a a d d e e f f'
    'a a a a d d e e f f';
  grid-gap: 2px;
  margin-bottom: 7vh;
}
.grid_item {
  display: flex;
  align-items: center;
}
.showcase1 { grid-area: a; }
.showcase2 { grid-area: b; }
.showcase3 { grid-area: c; }
.showcase4 { grid-area: d; }
.showcase5 { grid-area: e; }
.showcase6 { grid-area: f; }

.img {
  object-fit: cover;
  height: 100%;
  width: 100%;
}
.reposition {
  object-position: 0;
}

@media (max-width: 425px) {
  ul {
    grid-template-columns: 1fr;
  }
}
</style>
