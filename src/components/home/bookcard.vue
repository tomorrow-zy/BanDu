<template>
  <div class="bookcard">
    <img 
    class="bookcard-picture" 
    src="/static/index/u107.png" 
    :lazy-load="lazyLoad"
    v-show="isLoading || error"
    />
    <img 
    class="bookcard-picture" 
    :src="src"
    :lazy-load="lazyLoad"
    @load="onLoad"
    @error="onError"
    v-show="! isLoading && !error"
    />
    <div class="bookcard-text">书名</div>
  </div>
</template>

<script>
export default {
  props: {
    lazyLoad: {
      type: Boolean,
      default: true
    },
    src: {
      type: String,
      default: ''
    }
  },
  watch: {
    src (newValue, preValue) {
      if (newValue && newValue.length > 0 && newValue !== preValue) {
        this.$nextTick(() => {
          this.isLoading = true
          this.error = false
        })
      }
    }
  },
  data () {
    return {
      isLoading: true,
      error: false
    }
  },
  methods: {
    onLoad () {
      this.isLoading = false
      this.error = false
    },
    onError () {
      this.isLoading = false
      this.error = true
    }
  }
}
</script>

<style scoped>
.bookcard{
  margin-right: 13px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.bookcard-picture{

  width: 84px;
  height: 120px;
  border: 0.5px solid black;
  border-radius: 5px;
}
.bookcard-text{
  margin-top: 13px;
  height: 10px;
  line-height: 10px;
  text-align: center;
  font-size: 16px;
  font-weight: 30;
}
</style>