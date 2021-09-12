<script>
  import {  createEventDispatcher } from "svelte";
  export let value
  export let className
  export {className as class}
  const dispatch = createEventDispatcher();
  onMount(()=>console.log("Simple"))

  var clipboard = new ClipboardJS('.clip__');
  clipboard.on('success', function (e) {
  console.info('Action:', e.action);
  console.info('Text:', e.text);
  console.info('Trigger:', e.trigger);
   dispatch("copied")
  e.clearSelection();
});

clipboard.on('error', function (e) {
  console.error('Action:', e.action);
  console.error('Trigger:', e.trigger);
  dispatch("error")
});
</script>

 
<div class="clip__ {className}" data-clipboard-text={value}>
<slot>Just a filler</slot>
</div>