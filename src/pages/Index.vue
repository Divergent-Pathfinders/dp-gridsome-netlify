<template>
  <Layout>

<div>
  <b-jumbotron :header="$static.metadata.siteName" lead="Bootstrap v4 Components for Vue.js 2">
    <p>Welcome to {{ $static.metadata.siteName }}</p>
    <b-button variant="primary" href="#">More Info</b-button>
  </b-jumbotron>
</div>

  </Layout>
</template>

<static-query>
	query {
		metadata {
			siteName
		}
	}
</static-query>

<script>
export default {
  metaInfo: {
    title: ''
  }
}
</script>

<script>
import pageData from '~/data/pages/index.yml'

export default {
  data () {
    return {
      pageData
    }
  }
}
</script>