<script>
  import Nav from "../components/Nav.svelte";

  export let segment;
</script>

<style>
  main {
    display: flex;
    flex-direction: column;
    max-width: 56rem;
    margin: 0 auto;
  }
</style>

<Nav {segment} />
<main>
  <slot />
</main>
