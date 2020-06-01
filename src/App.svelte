<script>
  import Status from "./Status.svelte";
  import Navbar from "./Navbar.svelte";
  import MomentItem from "./MomentItem.svelte";
  import CreateStatusButton from "./CreateStatusButton.svelte";

  let moments = [
    {
      image:
        "https://pbs.twimg.com/profile_images/974736784906248192/gPZwCbdS.jpg"
    },
    {
      image: "https://randomuser.me/api/portraits/men/42.jpg"
    },
    {
      image:
        "https://pbs.twimg.com/profile_images/1165754931791314945/FRdmYcK0.jpg"
    },
    {
      image:
        "https://images-na.ssl-images-amazon.com/images/M/MV5BMTQwMDQ0NDk1OV5BMl5BanBnXkFtZTcwNDcxOTExNg@@._V1_UY256_CR2,0,172,256_AL_.jpg"
    },
    {
      image:
        "https://images.unsplash.com/photo-1502720705749-871143f0e671?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=200&fit=max&s=b8377ca9f985d80264279f277f3a67f5"
    },
    {
      image:
        "https://pbs.twimg.com/profile_images/1108443816565059590/Te-0H20q.png"
    }
  ];
</script>

<style>
  :global(*) {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    -webkit-tap-highlight-color: transparent;
    font-family: "Inter", sans-serif;
  }
  :global(a) {
    text-decoration: none;
  }

  main {
    margin-top: 2rem;
  }
  .spacing {
    height: 1rem;
  }
  .statuses h1 {
    font-weight: 600;
    font-size: 1.2rem;
    margin-left: 0.2rem;
    margin-bottom: 1.2rem;
  }
  .statuses {
    margin: 0rem 1.4rem;
  }

  .moments {
    margin: 0rem 1.4rem;
    margin-bottom: 2rem;
  }
  .moments h1 {
    margin-left: 0.2rem;
    margin-bottom: 1.2rem;
    font-size: 1rem;
  }
  .moments-wrapper {
    display: flex;
    flex-direction: row;
    overflow: auto;
  }

  .navbar-wrapper {
    z-index: 1;
    padding: 0.8rem 0rem;
    width: 100vw;
    bottom: 0;
    position: fixed;
    background: white;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.116);
  }
</style>

<main>
  <div class="moments">
    <h1>Moments</h1>
    <div class="moments-wrapper">
      {#each moments as moment}
        <MomentItem image={moment.image} />
        <div style="padding: 0rem 0.5rem;" />
      {/each}
    </div>
  </div>
  <div class="statuses">
    <h1>Latest updates</h1>
    <Status
      img="https://pbs.twimg.com/profile_images/974736784906248192/gPZwCbdS.jpg"
      time="4 mins ago"
      text="Does anyone think global warming is a good thing? I love Lady Gaga.
      I think she's a really interesting artist."
      username="andreas"
      name="Andreas Brixen" />
    <div class="spacing" />
    <Status
      img="https://pbs.twimg.com/profile_images/1054434556156162054/1H_7AxP0.jpg"
      time="6 mins ago"
      text="I can't belive my grand mothers making me take Out the garbage I'm
      rich fuck this I'm going home I don't need this shit"
      username="arnob"
      name="Arnob Mukherjee" />
    <div class="spacing" />
    <Status
      img="https://images.unsplash.com/photo-1520813792240-56fc4a3765a7?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=200&fit=max&ixid=eyJhcHBfaWQiOjE3Nzg0fQ"
      time="10 mins ago"
      text="typing..."
      username="booker"
      name="Yamilet Booker" />
    <div class="spacing" />
    <Status
      img="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=200&fit=max&s=707b9c33066bf8808c934c8ab394dff6"
      time="50 mins ago"
      text="I just looked at kanye page what the fuck kind a spaced out tweets
      are those. fuck that I aint never looking at that shit again"
      username="myles"
      name="Miyah Myles" />
    <div class="spacing" />
    <Status
      img="https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg?h=350&auto=compress&cs=tinysrgb"
      time="1 hour ago"
      text="Host meme review?"
      username="bright"
      name="Loki Bright" />
  </div>

  <CreateStatusButton />
  <div style="height: 6rem;" />
  <div class="navbar-wrapper">
    <Navbar />
  </div>
</main>
