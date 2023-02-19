<script lang="ts">
	import { T } from '@threlte/core';
	import Trees from './Trees.svelte';
</script>

<T.AmbientLight intensity={0.1} />
<T.DirectionalLight
	color="white"
	position={[15, 15, 15]}
	castShadow
	shadow.mapSize.width={2048}
	shadow.mapSize.height={2048}
/>
<Trees />
