<template>
  <b-container>
    <b-row class="mt-4 sticky-top">
      <b-col>
        <div class="category pt-1 pb-1">
          <ul class="list-inline w-100 mt-3">
            <li class="list-inline-item" v-for="(filter, index) in filters" :key="index">
              <div @click="changeActive(index)" :class="(activeIndex == index) ? 'btn btn-blue active' : 'btn btn-blue'"> {{filter}} </div>
            </li>
          </ul>
        </div>
      </b-col>
    </b-row>
    <b-row class="mt-2">
      <b-col>
        <b-row>
          <b-col>
            <div @click="showFilter = !showFilter" class="btn btn-blue active d-flex align-items-center justify-content-center" style="width:100px">
              <font-awesome-icon :icon="['fas', 'filter']" :style="{color:'white', fontSize:14}" />
              <span class="ml-2">Filter</span>
            </div>
          </b-col>
        </b-row>
        <transition-expand>
          <div v-if="showFilter">
            <b-row class="mt-2 p-2 align-items-end">
              <b-col md="3" cols="12" class="mt-2">
                <h5 class="dark-blue text-filter-list"> Harga </h5>
                <div class="d-flex align-items-center">
                  <b-form-input
                      placeholder="Minimum"
                      class="input-box"
                  >

                  </b-form-input>
                  <div class="mr-2 ml-2 blue"> - </div>
                  <b-form-input
                      placeholder="Maximum"
                      class="input-box"
                  >

                  </b-form-input>
                </div>
              </b-col>
              <b-col md="3" cols="12" class="mt-2">
                <div class="btn btn-blue active">
                  Terapkan
                </div>
              </b-col>
            </b-row>
          </div>
        </transition-expand>
      </b-col>
    </b-row>
    <b-row>
      <b-col>
        <h5 class="text-result grey-2 mt-5"> Menampilkan 10rb+ produk untuk “<span class="bold">baju kebaya</span>” (<span class="bold">1-60 dari 10rb</span>) </h5>
      </b-col>
    </b-row>
    <b-row class="no-gutters">
        <b-col class="mt-3 p-1" md="3" cols="6" v-for="n in 12" :key="n">
          <Product />
        </b-col>
    </b-row>
  </b-container>
</template>

<script>

import Product from '~/components/card/Product'
import TransitionExpand from '~/components/TransitionExpand'
export default {
  data:() => ({
    filters: ['Semua','Baju Wanita','Celana Wanita','Tas','Kemeja Wanita'],
    activeIndex:0,
    showFilter:false
  }),
  components:{
    Product,
    TransitionExpand
  },
  methods:{
    changeActive(index){
      this.activeIndex = index
    },
  }
}
</script>

<style scoped>

  .expand-enter-active,
  .expand-leave-active {
    transition-property: opacity, height;
  }
  .expand-enter,
  .expand-leave-to {
    opacity: 0;
  }

  .list-inline {
    -ms-overflow-style: none;
    overflow-x: scroll;
    white-space: nowrap;
  }

  .list-inline::-webkit-scrollbar {
    display: none !important;
  }

  .category {
    width: 100%;
    background-color: #F6F8FF;
  }

  .text-filter-list {
    font-size: 0.75rem;
  }

  .text-result {
    font-size: 0.85rem;
  }

  .input-box {
    display: inline-block;
    width: 100%;
    vertical-align: middle;
    background-color: white;
    background-clip: padding-box;
    border: 1px solid #1C56D9;
    border-radius: 0.3rem;
    color: #4F4F4F;
    font-size: 12px;
    padding: 0.5rem;
  }

  .input-box:focus {
    box-shadow: none;
    border-color: none;
    outline: none;
  }

  .input-box::placeholder {
    color: #BDBDBD;
    font-size: 0.75rem;
  }

</style>
