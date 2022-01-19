<script>
	let hovering;

	function enter() {
		hovering = true;
	}

	function leave() {
		hovering = false;
	}
</script>

<a href="#" on:mouseenter={enter} on:mouseleave={leave}>
	<slot {hovering}></slot>
</a>