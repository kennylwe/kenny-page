
<script>
  import { slide } from "svelte/transition";
  let drawing = false;
</script>

<title>Kenny's site</title>

<div id="background"></div>


{#if drawing}
  <div transition:slide={{ delay: 100, duration: 1000 }}>
    <section id="main-content">
    <div id="content-area">
      <h1>Hello!</h1>
      <p>
        This is Kenny! I am currently a sophmore at La Canada High School.
        I like to code and stuff!
      </p>
    </div>
  </section>
</div>

{/if}
<button on:click={() => (drawing = !drawing)}>
  {drawing ? "Hide Content" : "Show Content"}
</button>


<!--
  This is a simple Svelte component that toggles the visibility of a section
  with a slide transition when the button is clicked.
// Other transitions
<!  [Blur, Scale, Fly, Draw, Slide]
-->




  <style (lang="css")>
    #main-content {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    #background {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: #1f1e1e;
      z-index: -1;
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