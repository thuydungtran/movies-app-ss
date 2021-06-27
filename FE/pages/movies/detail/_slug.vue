<template>
  <h1>{{ slug }}</h1>
</template>

<script>
export default {
  async asyncData({ params }) {
    // eslint-disable-next-line no-console
    console.log('param is' + params)
    // eslint-disable-next-line no-debugger
    debugger
    const slug = await params.slug // When calling /abc the slug will be "abc"
    return { slug }
  },
}
</script>
