<script>
  import PageLoading from "$lib/components.g/Loading/PageLoading.svelte";
	import Posts from "$lib/components.g/posts/Posts.svelte";
	import Singlemediapost from "$lib/components.g/posts/singlemediapost.svelte";
	import { fly } from "svelte/transition";
  
	let show_today = true
  
  </script>
  
  
  <PageLoading/>
  <div class="p-4">
	
	  <section class="min-h-[20vh] flex flex-col justify-center items-center">
		  <div class="flex flex-col gap-1 items-center mb-4">
			  <div class="rounded-xl">
				<img src="/users/me6.jfif" alt="user" class="rounded-xl  h-[100px] w-[100px] object-cover"/>
			  </div>
			 <div>
			  <p class="capitalize font-bold  whitespace-nowrap">Anode saga á</p>
			  <p class="capitalize font-semibold   text-sm whitespace-nowrap">@anode_saga</p>
			 </div>
			</div>
	  </section>
	  <section class="flex justify-evenly items-center capitalize">
		  <div class="text-center">
			  <p class="font-bold text-xl">24K</p>
			  <p>Connects</p>
		  </div>
		  <div class="text-center">
			  <p class="font-bold text-xl">20000</p>
			  <p>posts</p>
		  </div>
		  <div class="text-center">
			  <p class="font-bold text-xl">300k</p>
			  <p>points</p>
		  </div>
	  </section>
  
	 <section class="w-full my-8 flex justify-center">
	  <button class="w-[80%] m-auto rounded-full  p-2 md:p-1 text-2xl  border-2">
		  Edit profile
	  </button>
	 </section>
  </div>
  
  <section class="p-4">
	  <div class="flex gap-4 p-2 border-b-2">
		 <button on:click={()=>show_today=true} class={show_today?'font-bold':'' +''}>Todays</button>
		 <button on:click={()=>show_today=false} class={!show_today?'font-bold':'' +''}>Saved</button>
	  </div>
	</section>
  
	{#if show_today}
	<section class="" in:fly={{x:-100, y:0, }} >
	  {#each [1,1,1,]  as i}
		  <Posts/>
	  {/each}
   </section>
	{:else}
	<section class="" in:fly={{x:100, y:0, }} >
	  {#each [1]  as i}
		  <Singlemediapost/>
	  {/each}
   </section>
	{/if}
  


