<template>
  <section>
    <h1>{{title}}</h1>
    <p>{{message}}</p>
    <hr>
    <router-link to="/">Go to Top</router-link>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  data: function() {
    return {
        title: 'Other',
        message: 'これは別のページ',
      }
  },
  created: function() {
    setInterval(() => {
      var d = new Date()
      this.now = d.getHours()
        + ":" + d.getMinutes()
        + ":" + d.getSeconds()
    }, 1000)
  }
}
</script>

<style>
.container {
  padding: 5px 10px;
}

h1 {
  font-size: 60px;
  color: #345980;
}

pre {
  padding: 10px;
  font-size: 18px;
  backgrond-color: #efefef;
}
hr {
  margin: 10px 0;
}


.links {
  padding-top: 15px;
}
</style>
