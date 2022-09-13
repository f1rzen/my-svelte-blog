<!-- +layout.svelte -->
<script >
     
  /** @type {import('./$types').LayoutData} */
    import Navbar from '../lib/components/Navbar.svelte'
    import PageTransition from '../lib/components/PageTransition.svelte'
    import "../app.css";
	  export let data;
   
</script >



<Navbar />

<PageTransition pathname={data.pathname}>
<main class="grid justify-center child:justify-center child:grid px-4 lg:px-96 text-2xl child:my-4">
  <slot/>
</main>
</PageTransition>



