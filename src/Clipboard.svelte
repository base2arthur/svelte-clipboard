<script>
  import {  createEventDispatcher } from "svelte";
  
  export let value
  export let className
  export {className as class}
  const dispatch = createEventDispatcher();
 

const click = ()=>{
  (async () => {
    await navigator.clipboard.writeText(value);
    dispatch("copied")
  })();
}
 
</script>

 
<div class="clip__  {className}" on:click={()=>click()}>
<slot>Just a filler</slot>
</div>