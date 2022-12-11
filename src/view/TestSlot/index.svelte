<script lang="ts">
import Child1 from "./components/Childe.svelte";
let age: number = 66
let getDom: any = null
const handelBtn = (data, e) => {
    // data = '值改了'
    // console.log('e', data, e)
    // console.log('getDom', getDom)
    getDom.handleChild()
  }

</script>

<div>
  AA
  <Child1 bind:this={getDom}>
    <div>插入子组件</div>
    <div slot='footer' let:testVal>
      footer插入
      <div>635</div>
      <div>{testVal}</div>
    </div>
    <div>测试获取dom</div>
    <button on:click={(e) => {handelBtn(age, e)}}>改变值</button>
  </Child1>
</div>

<style>

</style>