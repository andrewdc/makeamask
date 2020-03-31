<script>
import {onMount} from 'svelte';

onMount(() => {
FB.api(
    "/119599209673746/photos?fields=images",
    function (response) {
      if (response && !response.error) {
        console.log(response);
      }
    }
);
});

</script>

<style>
  h5 {
    color: grey;
  }

  .centrify {
    text-align: center;
  }
</style>

<div class="centrify">
  <h5>Hello bruh!</h5>
  
</div>