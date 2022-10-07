<!-- +layout.svelte -->
<script >
  
  
  
  /** @type {import('./$types').LayoutData} */
	import Sidebar from '$lib/components/Sidebar.svelte';
    import Navbar from '../lib/components/Navbar.svelte'
    import PageTransition from '../lib/components/PageTransition.svelte'
    import "../app.css";
	  export let data;
    // import Sidebar from '../lib/components/Sidebar.svelte';
    let open = false;
</script >



<Navbar bind:sidebar={open}/>
<Sidebar bind:open/>


<PageTransition pathname={data.pathname}>
<main class="grid justify-center child:justify-center child:grid px-4 lg:px-96 text-xl lg:text-2xl child:my-4">
  <slot/>
</main>
</PageTransition>



