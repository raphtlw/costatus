<script>
  export let image;
  export let username;
</script>

<style>
  main {
    text-align: center;
  }
  img {
    border-radius: 100%;
    height: 3.5rem;
    width: 3.5rem;
    object-fit: cover;
    border: 2px solid rgba(16, 140, 255, 0.788);
  }
  #username {
    font-size: 0.8rem;
  }
</style>

<main>
  <img src={image} alt="Story" />
  <span id="username">{username}</span>
</main>
