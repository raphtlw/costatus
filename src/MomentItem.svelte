<script>
  export let image;
</script>

<style>
  img {
    border-radius: 100%;
    height: 3rem;
    width: 3rem;
    object-fit: cover;
    border: 2px solid rgba(16, 128, 255, 0.788);
  }
</style>

<img src={image} alt="Story" />
