<script>
    import Navbar from "$lib/Navbar.svelte";
</script>

<style>
    :global(body), :global(html) {
      margin: 0;
      padding: 0;
    }
  </style>

<Navbar />

<slot />