<template>
  <div class="ratings">
    <div class="table-responsive">
      <table class="table">
        <thead>
          <tr>
            <th>#</th>
            <th>Name</th>
            <th>Rating</th>
            <th>Type</th>
          </tr>
        </thead>
        <tbody>
          <rating-item v-for="item in data" v-bind:rating="item"></rating-item>
        </tbody>
      </table>
    </div>
    <button class="btn btn-primary" v-on:click="create">Create</button>
  </div>
</template>

<script>
// TODO: extract this componenant in a separate file.
import Vue from 'vue'
Vue.component('rating-item', {
  props: ['rating'],
  template: `
    <tr>
      <td>{{ rating.id }}</td>
      <td>{{ rating.name }}</td>
      <td>{{ rating.rating }}</td>
      <td>{{ rating.type }}</td>
    </tr>
    `
})

export default {
  name: 'ratings',
  methods: {
    create () {
      this.ratings.push({})
    }
  },
  data () {
    return {
      data: [
        {id: 1, name: 'Vivants!', rating: 7.5, type: 'book'},
        {id: 2, name: 'Harry Potter 1', rating: 10, type: 'book'},
        {id: 3, name: 'Le Seigneur des Anneaux', rating: 8, type: 'book'},
        {id: 4, name: 'Foobar', rating: 6, type: 'book'},
        {id: 5, name: 'La Bible', rating: 5, type: 'book'},
        {id: 6, name: 'Le Coran', rating: 5, type: 'book'},
        {id: 7, name: 'Harry Potter 2', rating: 10, type: 'book'},
        {id: 8, name: 'Le Corniaud', rating: 6, type: 'movie'}
      ]
    }
  }
}
</script>

<style>
.ratings {
  text-align: left;
}
</style>
