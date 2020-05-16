<template>
  <div style="overflow-x:hidden">
      <b-container>
        <div>
          <b-row class="mt-5">
            <b-col>
              <h5 class="grey-2"> Terbaru </h5>
            </b-col>
          </b-row>
          <b-row class="mt-4 no-gutters">
              <b-col class="mt-3 p-1" md="3" cols="6" v-for="loop in loops" :key="loop">
                <Product />
              </b-col>
          </b-row>
          <b-row class="mt-5">
            <b-col>
              <h5 class="grey-2"> Terpopuler </h5>
            </b-col>
          </b-row>
          <b-row class="mt-4 no-gutters">
              <b-col class="mt-3 p-1" md="3" cols="6" v-for="loop in loops" :key="loop">
                <Product />
              </b-col>
          </b-row>
        </div>
      </b-container>
  </div>
</template>

<script>
import Product from '~/components/card/Product'
export default {
  data:() => ({
    loops: 4
  }),
  components: {
    Product
  }
}
</script>

<style scoped>


</style>
