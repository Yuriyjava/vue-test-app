<template>
  <div class="hello">
    <h1 @click="changeMsg">{{ curMsg }}</h1>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop, Model, Emit, Watch } from "vue-property-decorator";
@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;
  private curMsg = this.msg;
  @Watch('msg') onMsgChange(){
    this.curMsg = this.msg;
  }
  private changeMsg(){
    this.curMsg+=1;
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
