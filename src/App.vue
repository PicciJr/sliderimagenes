<template>
  <div id="app">
    <img :src="require(`../imgs/${currentImage}`)" class="mainImage" />
    <div class="footer">
      <ul>
        <li>
          <a @mouseover="changeImage('images1.jpg')">
            <img src="../imgs/images1.jpg" class="thumbnail" />
          </a>
        </li>
        <li>
          <a @mouseover="changeImage('images2.jpg')">
            <img src="../imgs/images2.jpg" class="thumbnail" />
          </a>
        </li>
        <li>
          <a @mouseover="changeImage('images3.png')">
            <img src="../imgs/images3.png" class="thumbnail" />
          </a>
        </li>
        <li>
          <a @mouseover="changeImage('images4.png')">
            <img src="../imgs/images4.png" class="thumbnail" />
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>

export default {
  name: "App",
  data() {
    return {
      currentImage: "images2.jpg",
      showModal: false
    };
  },
  methods: {
    changeImage(path) {
      this.currentImage = path;
      console.log(this.currentImage);
    }
  }
};
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

li {
  display: inline-block;
}

.thumbnail {
  border: 1px solid #ddd; /* Gray border */
  border-radius: 4px; /* Rounded border */
  padding: 5px; /* Some padding */
  margin: 5px;
  height: 5em;
  width: 5em; /* Set a small width */
}

.mainImage {
  height: 20rem;
  width: 20rem;
}

img:hover {
  box-shadow: 0 0 2px 1px rgba(0, 140, 186, 0.5);
}

a {
  cursor: pointer;
}
</style>
