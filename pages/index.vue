<template>
  <div style="overflow-x:hidden">
      <b-row>
        <b-col md="12" cols="12">
          <div class="search-bar">
            <b-form-input
              class="search-box"
              size="sm"
              placeholder="Type Something"
            ></b-form-input>
            <div class="button-search">
              <div>
                <font-awesome-icon :icon="['fas', 'search']" :style="{color:'white', fontSize:14}" />
              </div>
            </div>
          </div>
        </b-col>
      </b-row>
      <b-container>
        <div>
          <b-row class="mt-5">
            <b-col>
              <h5 class="grey-2"> Terbaru </h5>
            </b-col>
          </b-row>
          <b-row class="mt-4">
              <b-col class="mt-3" md="3" cols="6" v-for="loop in loops" :key="loop">
                <Product />
              </b-col>
          </b-row>
          <b-row class="mt-5">
            <b-col>
              <h5 class="grey-2"> Terpopuler </h5>
            </b-col>
          </b-row>
          <b-row class="mt-4">
              <b-col class="mt-3" md="3" cols="6" v-for="loop in loops" :key="loop">
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

  .search-bar {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
      height: 80px;
      background-color: #EDF1FF;
  }

  .button-search {
      background-color: #5B7EF4;
      width: 35px;
      height: 35px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      cursor: pointer;
  }

  .button-search div {
    vertical-align: middle;
  }

  .search-box {
    display: inline-block;
    max-width: 250px;
    width: 100%;
    vertical-align: middle;
    background-color: #435CBC;
    background-clip: padding-box;
    border: 1px solid transparent;
    border-radius: 10px;
    margin-right: 10px;
    color: #B8C7FF;
    font-size: 12px;
    padding: 1rem;
  }

  .search-box:focus {
    box-shadow: none;
    border-color: none;
    outline: none;
  }

  .search-box::placeholder {
    color: #EDF1FF;
    font-size: 12px;
  }

</style>
