 

# Svelte Component

`A Svelte component template.`

## Install

npm install git+https://github.com/base2arthur/svelte-clipboard.git
 

## Usage
See src/Index.js
<Clipboard class="w-full" bind:value on:copied={()=>message_.set("Copied to clipboard")}>
   Any component you desire goes here
</Clipboard>
## License

[MIT](https://opensource.org/licenses/MIT)
