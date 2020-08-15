<template>
  <div class="home">
    <p>{{ greetText }}</p>
    <p>
      <MyButton :greet="greetText" @click="onMyButtonClicked"></MyButton>
    </p>
    <p>
      <ResetButton initialValue="Hello" v-model="greetText"></ResetButton>
    </p>
  </div>
</template>

<script lang="ts">
  // @ is an alias to /src
  import { Component, Vue} from 'vue-property-decorator';
  import MyButton from  '@/components/MyButton.vue'
  import ResetButton from  '@/components/ResetButton.vue'

    @Component({
      components: {
        MyButton,
        ResetButton
    },
  })
  export default class Home extends Vue {
    //↓VScodeで「不要な型宣言」でエラーが出てしまう
      public greetText: string = "Hello";

      public onMyButtonClicked(){
          this.greetText = "こんにちは";
      }
  }
</script>
