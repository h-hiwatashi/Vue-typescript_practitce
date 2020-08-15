<template>
    <button @click="onClick">Reset</button>
</template>

<script lang="ts">
    import {Component, Prop, Emit,  Vue} from "vue-property-decorator";

    @Component
    export default class MyButton extends Vue{
        private initialValue!: string;

        @Prop()
        public value!: string;

        //ライフサイクルフック
        public created(){
            this.initialValue = this.value;
        }

        @Emit()
        public input(value: string){
        }

        public onClick(){
            this.input(this.initialValue);
        }
    }
</script>
}
</script>