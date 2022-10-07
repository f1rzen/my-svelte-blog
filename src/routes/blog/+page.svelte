<script>
	import { each } from 'svelte/internal';
    import Card from '../../lib/components/Card.svelte';
    export let data;
</script>
<h1 class="text-6xl">Blog</h1>

<!-- <ul>
    {#each data.posts as post}
      <li>
        <h2>
          <a href={post.path}>
            {post.meta.title}
          </a>
        </h2>
        Published {post.meta.date}
      </li>
    {/each}
  </ul> -->
 <div class="grid w-screen place-items-center">
<ul class="grid grid-cols-1 lg:grid-cols-2 gap-x-16">
    {#each data.posts as post}
      <li class="pt-6 ">
        <a href={post.path}>
          <Card title={post.meta.title} date={post.meta.date} path={post.path} img={post.meta.img}/>
        </a>
      </li>
    {/each}
  </ul>
</div>
<!-- 
<div class="grid grid-cols-1 lg:grid-cols-2 child:m-8">
    <ul>
        <li>
            {#each data.posts as post}
                <Card/>
            {/each}
        </li>
    </ul>
</div> -->

