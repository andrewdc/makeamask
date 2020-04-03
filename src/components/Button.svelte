<script>
export let href = '';
export let newtab = false;
export let error = false;
</script>

<style lang="scss">
// .soft {
  // padding:10px;
  // margin:10px;
  // display:flex;
  // flex-direction:column;
  // justify-content:center;
  // align-items:center;
  /* border-radius: 28px; */
  /* background: #f0f0f0;
  box-shadow:  10px 10px 20px #d3d3d3, -10px -10px 20px #ffffff; */
  /* transition: all 0.5s ease-in-out;  */
  // text-decoration:none;
  // font-size:1.2em;
  // height:90px;
  // flex:1 0 auto;
// }

/* .soft:hover {
  border-radius: 28px;
  background: linear-gradient(145deg, #ffffff, #d8d8d8);
  box-shadow:  10px 10px 20px #d3d3d3, -10px -10px 20px #ffffff;
} */


$text: #222a38;
$light-pink: #f0f8ff;
$pink: #e9f3ff;
$dark-pink: #c4ddf9;
$pink-border: #176dab;
$pink-shadow: #e2f8ff;



.button-link {
  position: relative;
  cursor: pointer;
  outline: none;
  border: 0;
  vertical-align: middle;
  text-decoration: none;
  font-size: inherit;
  font-family: inherit;
  margin:10px;
  display:flex;
  flex:1 0 auto;
  flex-direction:column;
  justify-content:center;
  align-items:center;
   font-weight: 600;
    color: $text;
    text-transform: uppercase;
    padding: 1.20em 1.8em;
    background: $light-pink;
    border: 2px solid $pink-border;
    border-radius: 0.75em;
    transform-style: preserve-3d;
    transition: transform 150ms cubic-bezier(0, 0, 0.58, 1), background 150ms cubic-bezier(0, 0, 0.58, 1);
   
    &::before {
      position: absolute;
      content: '';
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: $dark-pink;
      border-radius: inherit;
      box-shadow: 0 0 0 2px $pink-border, 0 0.625em 0 0 $pink-shadow;
      transform: translate3d(0, 0.75em, -1em);
      transition: transform 150ms cubic-bezier(0, 0, 0.58, 1), box-shadow 150ms cubic-bezier(0, 0, 0.58, 1);
    }
    &:hover {
      background: $pink;
      transform: translate(0, 0.25em);
      &::before {
        box-shadow: 0 0 0 2px $pink-border, 0 0.5em 0 0 $pink-shadow;
        transform: translate3d(0, 0.5em, -1em);
      }
    }
    &:active {
      background: $pink;
      transform: translate(0em, 0.75em);
      &::before {
        box-shadow: 0 0 0 2px $pink-border, 0 0 $pink-shadow;
        transform: translate3d(0, 0, -1em);
      }
    }
  }

  .small {
  margin-top:25px;
  font-size:0.8em;
  text-align:center;
}
  @media (max-width: 510px) {
    .button-link {
      font-size:1em;
      margin:0px;
      flex: 1 0 50%;
      transform:scale(0.8);
    }
  }
</style>

<a class="button-link" rel="noreferrer" href="{href}" target="{newtab ? '_blank': ''}">
  <slot name="icon" class="icon"></slot>
  <slot name="text"></slot>
</a>
{#if error}
<div class="small">If you recieve an error above try: <a href="{href}">{href}</a></div>
{/if}