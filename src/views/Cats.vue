<template>
  <div>
      <h1>Cats for Adoption</h1>
      <b-table striped hover :items="cats">
         <template slot="name" slot-scope="data">
             <router-link :to="`/pets/${data.value}`">
                {{ data.value }}
            </router-link>
      </template>
    </b-table>
  </div>
</template>

<script>
import cats from '@/data/cats'

export default {
  data () {
    return {
      cats
    }
  }
}
</script>
