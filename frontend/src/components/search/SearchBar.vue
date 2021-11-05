<template>

  <input type="text" class="url-input" placeholder="상품 주소 입력" v-model="url"
         @keyup.enter="enterUrl">


</template>

<script>
export default {
  name: 'searchBar',
  data() {
    return {
      url: '',

    }
  },
  methods: {
    enterUrl() {
      if (this.url.trim().length == 0) {
        return;
      }

      alert("입력된 URL : " + this.url);
    }
  }
}
</script>

<style lang="scss">
@import url("https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.5.2/animate.min.css");

.url-input {
  width: 100%;
  padding: 10px 18px;
  font-size: 18px;
  margin-bottom: 16px;

  &:focus {
    outline: 0;
  }
}


</style>

