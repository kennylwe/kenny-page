
<script>
  import { slide } from "svelte/transition";
  let drawing = false;
</script>

{#if drawing}
  <div transition:slide={{ delay: 250, duration: 300 }}>
    fades in  and out
    <p>
      hi hi
    </p>
  </div>
{/if}
<button on:click={() => (drawing = !drawing)}>
  hi hi
</button>


// Other transitions
[Blur, Scale, Fly, Draw, Slide]
<section id="main-content">
    <div id="content-area">
      <h1>Hello!</h1>
      <p>
        This is Kenny! I am currently a sophmore at La Canada High School.
        I like to code and stuff!
      </p>
    </div>
  </section>

  




  <style (lang="css")>
    #main-content {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    #content-area {
      text-align: center;
      max-width: 600px;
      padding: 20px;
      background-color: #f9f9f9;
      border-radius: 8px;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    }

    h1 {
      font-size: 2.5em;
      margin-bottom: 20px;
    }

    p {
      font-size: 1.2em;
      line-height: 1.6;
    }
</style>