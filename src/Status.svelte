<script>
  export let img;
  export let name;
  export let username;
  export let time;
  export let text;
</script>

<style>
  main {
    background-color: rgb(245, 245, 245);
    padding: 1.3rem 1.6rem;
    border-radius: 15px;
    font-family: "Inter";
    height: fit-content;
  }
  .header {
    display: flex;
    align-items: center;
  }
  .header img {
    height: 3rem;
    width: 3rem;
    border-radius: 100%;
    object-fit: cover;
  }
  .header-info {
    margin-left: 1.3rem;
  }
  .header-info h1 {
    font-size: 1rem;
    font-weight: 500;
    color: rgb(32, 32, 32);
    margin: 0.2rem 0rem;
  }
  .header-info h2 {
    font-size: 0.8rem;
    font-weight: 500;
    color: rgb(65, 65, 65);
    margin: 0.2rem 0rem;
  }

  .status h1 {
    margin-top: 0.8rem;
    font-size: 1.2rem;
    font-weight: 400;
  }
</style>

<main>
  <div class="header">
    <img src={img} alt="Profile" class="profile-photo" />
    <div class="header-info">
      <h1>{username}</h1>
      <h2>{time}</h2>
    </div>
  </div>
  <div class="status">
    <h1>{text}</h1>
  </div>
</main>
