<script>
  import MenuIcon from "./MenuIcon.svelte";
  export let sidebar = false

</script>

<nav class="flex items-center lg:px-32 justify-between pb-32 lg:pb-[3em] m-[3em] mb-0">
  <div class="text-4xl">
    <h1><a href="/">ilkay.me</a></h1>
  </div>
  <div class="text-xl hidden md:block lg:visible ">
    <ul class="flex child:mx-4 ">
      <li><a class="hover:underline underline-offset-4" href="/">Home</a></li>
      <li><a class="hover:underline underline-offset-4" href="/about">About</a></li>
      <li><a class="hover:underline underline-offset-4" href="/contact">Contact</a></li>
      <li><a class="hover:underline underline-offset-4" href="/blog">Blog (TR)</a></li>
      
    </ul>
    
  </div>


  <div class="visible md:hidden">
    <MenuIcon bind:open={sidebar}/>
    
  </div>

</nav>
