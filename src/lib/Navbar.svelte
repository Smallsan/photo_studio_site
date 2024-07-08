<script>
    let isMenuOpen = false;
</script>

<nav class="flex justify-between items-center py-2 px-6 bg-white relative">
    <div class="flex items-center">
        <a href="/" class="flex items-center no-underline">
            <img src="/images/logo.jpg" alt="Logo" class="h-10 w-auto mr-2" />
            <span class="text-2xl font-script text-black ml-2">Tan's Self Portrait Studio</span>
        </a>
    </div>
    <button class="md:hidden" on:click={() => (isMenuOpen = !isMenuOpen)}>
        <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
    </button>
    <div class="hidden md:flex">
        <a href="/" class="py-2 px-4 text-base text-gray-800 no-underline hover:text-custom-brown">Home</a>
        <a href="/about" class="py-2 px-4 text-base text-gray-800 no-underline hover:text-custom-brown">About</a>
        <a href="/contact" class="py-2 px-4 text-base text-gray-800 no-underline hover:text-custom-brown">Contact</a>
        <a href="/gallery" class="py-2 px-4 text-base text-gray-800 no-underline hover:text-custom-brown">Gallery</a>
        <a href="/services" class="py-2 px-4 text-base text-gray-800 no-underline hover:text-custom-brown">Services</a>
    </div>
    <div class={`absolute top-full left-0 w-full ${isMenuOpen ? 'block' : 'hidden'} md:hidden`}>
        <ul class="flex flex-col items-center m-0 p-0 list-none bg-white shadow-md">
            <li class="w-full text-center"><a href="/" class="block py-2 px-0 text-base text-gray-800 no-underline hover:text-custom-brown">Home</a></li>
            <li class="w-full text-center"><a href="/about" class="block py-2 px-0 text-base text-gray-800 no-underline hover:text-custom-brown">About</a></li>
            <li class="w-full text-center"><a href="/contact" class="block py-2 px-0 text-base text-gray-800 no-underline hover:text-custom-brown">Contact</a></li>
            <li class="w-full text-center"><a href="/gallery" class="block py-2 px-0 text-base text-gray-800 no-underline hover:text-custom-brown">Gallery</a></li>
            <li class="w-full text-center"><a href="/services" class="block py-2 px-0 text-base text-gray-800 no-underline hover:text-custom-brown">Services</a></li>
        </ul>
    </div>
</nav>

<style>
	nav {
		position: sticky;
		top: 0;
		z-index: 1000; /* Ensure the menu stays on top of other content */
		background-color: white; /* Ensure the background is not transparent */
	}
	@font-face {
		font-family: 'Brush Script MT';
		src: url('/fonts/BrushScript.otf') format('opentype');
	}
	.font-script {
		font-family: 'Brush Script MT', cursive;
	}
	.no-underline {
		text-decoration: none;
	}
	.hover\:text-custom-brown:hover {
		color: #d9b99b;
	}
	/* Additional styles for the toggle button */
	button {
		background: none;
		border: none;
		cursor: pointer;
	}
	/* Ensure the menu items are centered */
	ul li a {
		justify-content: center;
	}
	/* Adjustments for the dropdown menu */
	.absolute {
		z-index: 10; /* Ensure the menu is above other content */
	}
	.shadow-md {
		box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* Optional: Adds a shadow for better visibility */
	}
</style>
