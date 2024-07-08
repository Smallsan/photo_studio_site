<script>
    import { onMount } from 'svelte';
    import Navbar from "$lib/Navbar.svelte";
    import '../app.css'
    onMount(() => {
        // Dynamically load the AOS script
        const script = document.createElement('script');
        script.src = 'https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.js';
        script.onload = () => {
            // @ts-ignore
            AOS.init({
                // AOS options here
                duration: 800,
                once: true,
            });
        };
        document.head.appendChild(script);
    });

</script>

<svelte:head>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.css">
</svelte:head>

<style>
    :global(body), :global(html) {
      margin: 0;
      padding: 0;
    }
  </style>

<Navbar />

<slot />