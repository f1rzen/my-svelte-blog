<!-- <svg class="hover:cursor-pointer" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="none" d="M0 0h24v24H0z"/><path d="M3 4h18v2H3V4zm6 7h12v2H9v-2zm-6 7h18v2H3v-2z" fill="rgba(255,255,255,1)"/></svg> -->

<script>
	export let open = false
</script>

<button class="text-[#efefef] cursor-pointer mr-4 border-none focus:outline-none" class:open on:click={() => open = !open}>
	<svg width=32 height=24>
		<line id="top" x1=0 y1=2  x2=32 y2=2/>
		<line id="middle" x1=0 y1=12 x2=24 y2=12/>
		<line id="bottom" x1=0 y1=22 x2=32 y2=22/>
	</svg>
</button>

<style>
	svg {
		min-height: 24px;
		transition: transform 0.3s ease-in-out;
	}
	
	svg line {
		stroke: currentColor;
		stroke-width: 3;
		transition: transform 0.3s ease-in-out
	}
	
	button {
		z-index: 20;
	}
	
	.open svg {
		transform: scale(0.7)
	}
	
	.open #top {
		transform: translate(6px, 0px) rotate(45deg)
	}
	
	.open #middle {
		opacity: 0;
	}
	
  .open #bottom {
		transform: translate(-12px, 9px) rotate(-45deg)
	}
</style>