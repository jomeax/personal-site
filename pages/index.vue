<template>
  <div><h1>The sun went up in Frebbenby at:</h1>

    <pre>{{post.location.time[0].sunrise.time}}</pre>
  </div>
</template>

<script>
export default {
  async asyncData({params, $http}) {
    const post = await $http.$get('https://api.met.no/weatherapi/sunrise/2.0/.json?lat=60.218718&lon=-19.679863&date=2020-10-19&offset=-00:00')
    return {post}
  }
}
</script>

