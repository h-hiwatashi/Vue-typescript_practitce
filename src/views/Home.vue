<template>
  <div class="home">
    <MyButton greet="Hello"></MyButton>
  </div>
</template>

<script lamg="ts">
  // @ is an alias to /src
  import { Component, Vue} from 'vue-property-decorator';
  import MyButton from  '@/components/MyButton.vue'

  @Component({
    components: {
      MyButton,
  },
  })
    export default class Home extends Vue {}
</script>
