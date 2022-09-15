<script>
	export let open = false
</script>

<aside class="absolute w-full h-full bg-black  shadow-lg" class:open>
	<nav class="p-12 text-4xl child:my-8" on:click={() => open = !open} >
		<a  class="block" href="/">Home</a>
		<a  class="block" href="about">About</a>
		<a class="block" href="contact">Contact</a>
		<a class="block" href="blog">Blog</a>
	</nav>
</aside>

<style>
	aside {
		left: -100%;
		transition: left 0.3s ease-in-out
	}
	
	.open {
		left: 0
	}
</style>