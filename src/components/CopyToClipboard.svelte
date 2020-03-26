<script>
  let slotContent = "";
  
$: {
  console.log(slotContent);
}
  const copy = function(){
    let value = slotContent;
    let range = document.createRange();
    range.selectNode(value);
    window.getSelection().addRange(range);

     try {  
    // Now that we've selected the anchor text, execute the copy command  
    var successful = document.execCommand('copy');  
    var msg = successful ? 'successful' : 'unsuccessful';  
    console.log('Copy command was ' + msg);  
  } catch(err) {  
    console.log('Oops, unable to copy');  
  }  

  // Remove the selections - NOTE: Should use
  // removeRange(range) when it is supported  
  window.getSelection().removeAllRanges();  
   
  }
</script>

<style>
  

  svg {
    cursor: pointer;
  }
  .soft {
  padding:10px;
  margin:10px;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  border:none;
  border-radius: 28px;
  background: #f0f0f0;
  box-shadow:  10px 10px 20px #d3d3d3, -10px -10px 20px #ffffff;
  transition: all 0.5s ease-in-out; 
  text-decoration:none;
  font-size:20px;
  height:90px;
  flex:1 0 auto;
}

.soft:hover {
  border-radius: 28px;
  background: linear-gradient(145deg, #ffffff, #d8d8d8);
  box-shadow:  10px 10px 20px #d3d3d3, -10px -10px 20px #ffffff;
  cursor:pointer;
}
</style>

<span bind:this={slotContent}>
  <slot />
</span>

<button class="soft" on:click|preventDefault={copy}>
  Click to Copy Above
  <svg
    title="Copy to clipboard"
    class="octicon octicon-clippy"
    viewBox="0 0 14 16"
    version="1.1"
    width="14"
    height="16"
    aria-hidden="true">
    <path
      fill-rule="evenodd"
      d="M2 13h4v1H2v-1zm5-6H2v1h5V7zm2 3V8l-3 3 3 3v-2h5v-2H9zM4.5
      9H2v1h2.5V9zM2 12h2.5v-1H2v1zm9
      1h1v2c-.02.28-.11.52-.3.7-.19.18-.42.28-.7.3H1c-.55
      0-1-.45-1-1V4c0-.55.45-1 1-1h3c0-1.11.89-2 2-2 1.11 0 2 .89 2 2h3c.55 0 1
      .45 1 1v5h-1V6H1v9h10v-2zM2 5h8c0-.55-.45-1-1-1H8c-.55
      0-1-.45-1-1s-.45-1-1-1-1 .45-1 1-.45 1-1 1H3c-.55 0-1 .45-1 1z" />
  </svg>
</button>
