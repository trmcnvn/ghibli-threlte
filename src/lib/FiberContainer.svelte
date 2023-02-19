<script lang="ts">
	import { Canvas, OrbitControls, T } from '@threlte/core';
	import Scene from './Scene.svelte';
	import Ground from './Ground.svelte';
</script>

<Canvas shadows>
	<T.PerspectiveCamera makeDefault position={[14.4666, 2.0365, 5.556165]} fov={40} let:ref>
		<OrbitControls minDistance={1} maxDistance={200} />
	</T.PerspectiveCamera>
	<Scene />
	<Ground />
</Canvas>
