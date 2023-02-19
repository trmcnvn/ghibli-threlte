<script lang="ts">
	import { T } from '@threlte/core';
	import { useGltf } from '@threlte/extras';

	const { gltf } = useGltf('/trees.glb', { useDraco: true });
</script>

{#if $gltf}
	<T.Group {...$$props} dispose={false}>
		<T.Mesh
			castShadow
			receiveShadow
			geometry={$gltf.nodes.Foliage.geometry}
			position={[0.33, -0.05, -0.68]}
		>
			<T.MeshStandardMaterial color="#234549" />
		</T.Mesh>
	</T.Group>
{/if}
