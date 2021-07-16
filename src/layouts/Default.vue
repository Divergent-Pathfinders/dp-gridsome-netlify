<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="primary">
      <b-navbar-brand to="/">{{ $static.metadata.siteName }}</b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item to="/about/">About</b-nav-item>
          <b-nav-item to="/posts/">Posts</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  <slot/>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>