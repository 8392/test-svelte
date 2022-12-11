<script lang="ts">
  import Child1 from "./components/Child1.svelte";
  let data = '我是home组件'
  let name: string = '传给子组件的值'
  const handelBtn = () => {
    data = '值改了'
  }

  const handelBtn2 = () => {
    name = '值改了----传给子组件的值'
  }
</script>

<div>
  <div>{data}</div>  
  <Child1 {name} />
  <button on:click={handelBtn}>改变值</button>
  <button on:click={handelBtn2}>改变传入子组件的值</button>
  
</div>

<style>

</style>