<template>
  <div>
    <g-link :to="post.path">
      <h1>{{post.title}}</h1>
    </g-link>
    <p>{{post.body}}</p>
  </div>

</template>

<script>
export default {
  props: ["post"],
}
</script>