<script>
    import Navbar from "$lib/Navbar.svelte";
    import '../app.css'
</script>

<style>
    :global(body), :global(html) {
      margin: 0;
      padding: 0;
    }
  </style>

<Navbar />

<slot />