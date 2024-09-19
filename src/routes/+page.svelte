<script>
  export let data;
</script>

<section class="content-box">
  <article>
    <div class="color-bar"></div>
    <h1>{data.person.name} {data.person.surname}</h1>
    <div class="container-circles">
      <div class="circle"></div>
      <div class="circle"></div>
      <div class="circle"></div>
      <div class="circle"></div>
      <div class="circle"></div>
      <div class="circle"></div>
      <div class="circle"></div>
    </div>

    <section>
      <h2>About me</h2>
      <p>{data.person.bio}</p>
    </section>
    <div class="icons-socials">
      <img src="" alt="">
    </div>
  </article>
 
</section>

<style>
  .content-box {
    display: flex;
    justify-content: center;
  
  }

  article {
    background-color: #FFF;
    width: 327px;
    height: 360px;
    justify-content: center;
    margin-top: 1rem;
    border-radius: 0.5rem;
    padding: 1.5rem;
    position: relative;
    z-index: 1; /* Ensures article is on top of bubbles */
  }

  h1 {
    font-family: "Londrina Outline", system-ui;
    font-weight: 400;
    font-style: normal;
    font-size: 64px;
    -webkit-text-stroke: 1.5px black;
    max-width: 10rem;
    margin: 0;
  }

  h2 {
    font-weight: bold;
    font-size: 15px;
    background-color: #576dff78;
    padding: 0.3rem 0.7rem 0.3rem 0.7rem;
    display: inline;
    border-radius: 0.3rem;
  }
  .container-circles {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  z-index: 0; /* Ensures bubbles are behind the content */
}

.circle {
  position: absolute;
  background:linear-gradient(rgba(122, 157, 205, 0.425), rgba(96, 101, 245, 0.618)) ;
  border-radius: 50%;
  opacity: 0.8;
  animation: float 10s ease-in-out infinite;
  animation-play-state: paused; /* Pause the animation initially */
}

article:hover .circle {
  animation-play-state: running; /* Start the animation on hover */
}

article:hover {
  cursor: pointer;  
  box-shadow: 1px 1px 5px 5px rgba(118, 177, 232, 0.81);
 
}

/* Keyframes for random float movement */
@keyframes float {
  0% {
    transform: translate(0, 0) scale(0.7);
    opacity: 1;
  }
  50% {
    transform: translate(20vw, -20vh) scale(1);
    opacity: 0.8;
  }
  100% {
    transform: translate(-15vw, -100vh) scale(1.4);
    opacity: 0;
  }
}

/* Random placement, size, and animation details for each bubble */
.circle:nth-child(1) {
  left: 5%;
  width: 6rem;
  height: 6rem;
  animation-duration: 12s;
  animation-delay: 0s;
}

.circle:nth-child(2) {
  left: 25%;
  width: 4rem;
  height: 4rem;
  animation-duration: 14s;
  animation-delay: 3s;
}

.circle:nth-child(3) {
  left: 45%;
  width: 7rem;
  height: 7rem;
  animation-duration: 10s;
  animation-delay: 5s;
}

.circle:nth-child(4) {
  left: 65%;
  width: 5rem;
  height: 5rem;
  animation-duration: 16s;
  animation-delay: 1s;
}

.circle:nth-child(5) {
  left: 85%;
  width: 8rem;
  height: 8rem;
  animation-duration: 18s;
  animation-delay: 2s;
}

</style>
