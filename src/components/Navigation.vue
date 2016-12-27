<template>
  <div class="navigation">
    <nav class="navbar navbar-fixed-top navbar-dark bg-inverse">
      <a class="navbar-brand" href="#">{{ title }}</a>
      <ul class="nav navbar-nav" v-for="link in links">
        <li class="nav-item">
          <a class="nav-link" href="#">{{ link }}</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      title: 'Lyfee',
      links: [
        'home', 'ratings', 'budget', 'blog', 'health', 'contact'
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
li {
  margin: 0 10px;
}

.navbar-brand {
  text-transform: uppercase;
}

.nav-link {
  text-transform: uppercase;
}
</style>
