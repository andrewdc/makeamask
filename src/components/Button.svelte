<script>
export let href = '';
export let newtab = false;
export let error = false;
</script>

<style>
.soft {
  padding:10px;
  margin:10px;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  border-radius: 28px;
  background: #f0f0f0;
  box-shadow:  10px 10px 20px #d3d3d3, -10px -10px 20px #ffffff;
  transition: all 0.5s ease-in-out; 
  text-decoration:none;
  font-size:1.2em;
  height:90px;
  flex:1 0 auto;
}

.soft:hover {
  border-radius: 28px;
  background: linear-gradient(145deg, #ffffff, #d8d8d8);
  box-shadow:  10px 10px 20px #d3d3d3, -10px -10px 20px #ffffff;
}
.small {
  font-size:0.8em;
  text-align:center;
}
  @media (max-width: 510px) {
    .soft {
      font-size:1em;
      margin:0px;
      flex: 1 0 50%;
      transform:scale(0.8);
    }
  }
</style>

<a class="soft" rel="noreferrer" href="{href}" target="{newtab ? '_blank': ''}">
  <slot name="icon" class="icon"></slot>
  <slot name="text"></slot>
</a>
{#if error}
<div class="small">If you recieve an error above try: <a href="{href}">{href}</a></div>
{/if}