<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h2>Hi {{name.toUpperCase()}}!</h2>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';


@Component({
 beforeRouteEnter(to, from, next){
   //eslint-disable-next-line
   next(vm => vm.name = to.params.name);
 }
})
export default class Home extends Vue {
    private name ='';
}
</script>