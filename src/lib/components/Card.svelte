<script>
  export let title;

  export let date;
  export let path;
  export let img;

</script>

<div class="p-1 shadow-xl bg-gradient-to-r from-pink-500 via-red-500 to-yellow-500 rounded-2xl w-[15em]">
    <a class="block  bg-black  rounded-xl" href="{path}">
      
        <img class="rounded-xl card-img p-0" src={img} alt="">
        <h5 class="pr-8 p-6 pb-0 text-4xl font-bold text-[#efefef]">{title}</h5>
        <p class="pr-8 pl-6 pt-0 pb-6 mt-2 text-sm text-[#efefef]">{date}</p>
        <!-- <p class="pr-8 p-6 mt-2 text-xl text-[#efefef]">{body}</p> -->
      
    </a>
  </div>
  