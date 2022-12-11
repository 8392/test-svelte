<script lang="ts">
export let xx: number = 666
let testVal: string | number = 'Aadca'
export const handleChild = (e) => {
    // data = '值改了'
    // console.log('e', e)
    testVal = 'ASDASDASSDA'
  }


</script>

<div>
  <!-- AA -->
  <div>{xx}</div>
  <slot>插槽</slot>
  <slot name="footer" {testVal}></slot>
  <button on:click={handleChild}>子组件</button>
</div>

<style>

</style>