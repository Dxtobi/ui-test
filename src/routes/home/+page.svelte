<script>
 
  import Status from './status.svelte';
  import Posts from '$lib/components.g/posts/Posts.svelte';
  
</script>


<div id="app__home" class="">
	<section class="flex gap-5 overflow-x-scroll py-10">
	  <div class="flex flex-col gap-1 items-center ml-4">
		<div class="text-3xl rounded-xl  h-[60px] w-[60px] grid place-content-center  border-custom bg-gradient-to-r from-gray-700 via-gray-900 to-black text-white">
		  <iconify-icon icon="material-symbols:add"></iconify-icon>
		</div>	   
	  </div>
	  {#each [1,0,0,0,0,0] as i}
	  <Status/>
	  {/each}
	</section>
	
	<Posts/>
  </div>