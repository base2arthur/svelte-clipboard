<script>
  import {  createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();
  onMount(()=>console.log("Simple"))
</script>

<style>
  
</style>

<slot>Just a filler</slot>
