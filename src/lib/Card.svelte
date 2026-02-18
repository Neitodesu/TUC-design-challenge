<script>
  import youtubeImg from "../assets/youtube.png";
  import githubImg from "../assets/developer.png";
  import pokeballImg from "../assets/pokeball.png";
  import { fade, fly } from "svelte/transition";
</script>

<div class="card">
  <div class="left">
    <div transition:fade={{ duration: 800 }} class="profile-img"></div>
    <div class="links" transition:fade={{ duration: 2000, delay: 200 }}>
      <a
        href="https://www.youtube.com/@neitodesu"
        target="_blank"
        rel="noopener noreferrer"><img src={youtubeImg} alt="youtube link" /></a
      >
      <a
        href="https://github.com/Neitodesu"
        target="_blank"
        rel="noopener noreferrer"><img src={githubImg} alt="github link" /></a
      >
      <a
        href="https://pokedex-app-b2n.pages.dev/"
        target="_blank"
        rel="noopener noreferrer"
        ><img src={pokeballImg} alt="project link" /></a
      >
    </div>
  </div>
  <div class="right">
    <p in:fly={{ x: 200, delay: 100, duration: 600 }}>
      Hello, I'm <span class="highlight span">Nate!</span>
    </p>
    <p in:fly={{ x: 200, delay: 150, duration: 600 }}>
      Aspiring <span class="highlight span">Full Stack Developer </span> 🚀
    </p>
    <p in:fly={{ x: 200, delay: 200, duration: 600 }}>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Nisi suscipit
      dolorem, <span class="highlight">corporis eligendi eum veritatis.</span>
    </p>
    <p in:fly={{ x: 200, delay: 250, duration: 600 }}>
      <span class="span">Email:</span>
      <a href="https://gmail.com">nbolduc92@gmail.com</a> 📧
    </p>
    <p in:fly={{ x: 200, delay: 300, duration: 600 }}>
      <span class="span">Page:</span> Coming Soon! 🏗️
    </p>
  </div>
</div>

<style>
  .card {
    background-color: #fff;
    border-radius: 0.5rem;
    box-shadow: 2px 1px 1px 1px #0006;
    overflow: hidden;
    width: 400px;
    height: 200px;
    display: grid;
    grid-template-columns: 150px 1fr;

    .left {
      background: center/cover url(../assets/trythis.jpg);
      padding: 1rem;
      display: grid;
      gap: 0.8rem;
      place-content: center;
      filter: drop-shadow(0 0 2px #0006);

      .profile-img {
        width: 100px;
        height: 100px;
        background: center/contain url("../assets/pfp.jpg");
        border-radius: 10rem;
        box-shadow: 0 2px 4px 1px #0006;
        border: 2px solid #d5d5d5;
      }

      .links {
        display: flex;
        gap: 0.4rem;
        margin: 0 auto;

        img {
          width: 26px;
          transition: transform 0.1s ease-out;

          &:hover {
            opacity: 0.6;
            transform: translateY(-3px);
          }
        }
      }
    }

    .right {
      background-color: #fdfdfd;
      color: var(--fc-main);
      font-family: var(--ff-main);
      font-weight: 500;
      padding: 0.4rem 1rem;
      height: 100%;
      font-size: 0.8rem;
      display: flex;
      flex-direction: column;
      align-items: start;
      justify-content: space-around;

      a {
        transition: opacity 0.1s ease-out;
      }

      .span {
        font-weight: 700;
        color: #222;
      }

      .highlight {
        background-color: #8d98a799;
      }

      a:hover {
        text-decoration: underline;
        opacity: 0.6;
      }
    }
  }
</style>
