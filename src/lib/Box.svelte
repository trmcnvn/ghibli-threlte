<script lang="ts">
	import { T, InteractiveObject, useFrame } from '@threlte/core';

	let mesh: THREE.Mesh;
	let hovered = false;
	let active = false;

	useFrame((_, delta) => {
		mesh.rotation.x += delta;
	});
</script>

<T.Mesh {...$$props} bind:ref={mesh} castShadow scale={active ? 1.5 : 1} let:ref>
	<InteractiveObject
		object={ref}
		interactive
		on:click={() => (active = !active)}
		on:pointerenter={() => (hovered = true)}
		on:pointerleave={() => (hovered = false)}
	/>
	<T.BoxGeometry args={[1, 1, 1]} />
	<T.MeshStandardMaterial color={hovered ? 'hotpink' : 'orange'} />
</T.Mesh>
