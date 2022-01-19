<script>
  import { slide } from "svelte/transition";
  import Hoverable from "./Hoverable.svelte";

  export let img;
  export let title;
  export let info;
</script>

<Hoverable let:hovering={active}>
  <section class="box-container" style={`background-image: url('img/${img}')`}>
    <div class="expandable-info">
      <div class="info-body">
        <h3 class="info-title">{title}</h3>
        {#if active}
          <p transition:slide class="info-paragraph">{info}</p>
        {/if}
      </div>
      <div class="arrow"><span> > </span></div>
    </div>
  </section>
</Hoverable>

<style>
  .box-container {
    width: 44vw;
    max-width: 464px;
    height: 300px;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    background-size: cover;
    background-position: center;
    --blue: #0a304e;
  }
  .box-container:hover {
    --blue: #3168a6;
  }
  .expandable-info {
    display: flex;
    justify-content: flex-end;
    overflow: hidden;
    background: var(--blue);
    color: white;
    transition: 0.5s;
  }
  .info-title{
    margin: 8px 0px;
  }
  .info-paragraph{
    margin: -3px 0px 8px 0px;
  }
  .info-body {
    padding: 0px 12px;
    width: 95%;
  }
  .arrow {
    background: black;
    width: 16px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  @media screen and (max-width: 900px) {
    .box-container {
      min-width: 99%
    }
  }
</style>
