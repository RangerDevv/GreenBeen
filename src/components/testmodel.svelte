<script lang='ts'>
    import { T } from '@threlte/core'
</script>
<body>
  <T.Mesh position.y={1}>
    <T.BoxGeometry args={[1, 2, 1]} />
    <T.MeshBasicMaterial color="hotpink" />
  </T.Mesh>
</body>