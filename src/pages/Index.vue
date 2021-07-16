<template>
  <Layout>

<div>
  <b-jumbotron :header="pageData.title" :lead="pageData.strapline">
    <p>{{ pageData.explainer }} </p>
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