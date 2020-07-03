<script>
  import { onMount } from 'svelte';
  import Lazy from 'svelte-lazy';

  let image;

  onMount(async () => {
    image = await fetch('');
  });
</script>

<style>

</style>

<main>
  <Lazy>
    <img src={image} alt="" />
  </Lazy>
</main>
