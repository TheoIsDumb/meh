<script>
  import { T, useFrame } from '@threlte/core'
  import { color } from '$lib/store'

  let rotation = 0
  useFrame((state, delta) => {
    rotation += delta
  })
</script>

<T.PerspectiveCamera
  makeDefault
  position={[0, 0, 0]}
  fov={100}
  near={0.1}
  far={1000}
/>

<T.DirectionalLight position={[0, 10, 10]} intensity={0.5} />
<T.AmbientLight color="#ffffff" intensity={0.2} />

<T.Mesh
rotation.y={rotation}
rotation.x={rotation}>
  <T.TorusKnotGeometry args={[10, 1, 300, 20, 8, 9]}/>
  <T.MeshToonMaterial color={$color}/>
</T.Mesh>