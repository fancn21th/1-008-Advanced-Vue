<template>
  <div class="chip">
    <img :src="getImgUrl(imgUrl)" alt="Person" width="96" height="96" />
    <slot></slot>
    <span class="closebtn">&times;</span>
  </div>
</template>

<script>
export default {
  props: {
    imgUrl: {
      type: String,
      required: true,
    },
  },
  methods: {
    getImgUrl(avatar) {
      // https://stackoverflow.com/questions/40491506/vue-js-dynamic-images-not-working
      const images = require.context('../assets/image', false, /\.png$/);
      return images(`./${avatar}.png`);
    },
  },
};
</script>

<style>
.chip {
  display: inline-block;
  padding: 0 25px;
  height: 50px;
  font-size: 18px;
  line-height: 50px;
  border-radius: 25px;
  background-color: #f1f1f1;
}

.chip img {
  float: left;
  margin: 0 10px 0 -25px;
  height: 50px;
  width: 50px;
  border-radius: 50%;
}

.closebtn {
  padding-left: 10px;
  color: #888;
  font-weight: bold;
  float: right;
  font-size: 20px;
  cursor: pointer;
}

.closebtn:hover {
  color: #000;
}
</style>
