<template>
      <div class="card">
          <div class="card-header">
              <div class="label-container">
                  <div class="label-discount">
                    <p>-15%</p>
                  </div>
                  <div class="label-new">
                    <p>New</p>
                  </div>
              </div>
              <nuxt-link :to="'/product/detail'">
                <img src="https://cf.shopee.co.id/file/fb4f1f1ab0c6bb8754dc4884d0b36dfa" class="img-card" />
              </nuxt-link>
          </div>
          <div class="card-body">
              <nuxt-link :to="'/product/detail'"><p class="title-product grey-2"> Baju langka supreme hanya ada 1 didunia </p></nuxt-link>
              <p class="price-product orange-1"> Rp 150.000
                <br/>
                <span class="discount-product grey-5"> Rp 250.000 </span>
                <client-only>
                    <star-rating
                      v-model="rating"
                      :star-size="12"
                      :show-rating="false"
                      :rounded-corners="false"
                      :padding="0"
                      :read-only="true"
                      :round-start-rating="false"
                    ></star-rating>
                </client-only>
              </p>
              <b-row class="no-gutters">
                <b-col class="mt-1 text-center p-1">
                    <nuxt-link :to="''" class="btn btn-blue"> Detail </nuxt-link>
                </b-col>
                <b-col class="mt-1 text-center p-1">
                    <nuxt-link :to="''" class="btn btn-blue active"> Buy </nuxt-link>
                </b-col>
              </b-row>
          </div>
      </div>
</template>

<script>
export default {
  data: () => ({
    rating: 4.5,
    loops: 4,
  })
}
</script>

<style scoped>

    a {
      text-decoration: none;
    }

    .label-container {
        position: absolute;
        top: 0;
        right: 0;
        margin-top: 10px;
        margin-right: 10px;
    }

    .card {
      background-color: white;
      border-radius: 1.25rem;
      border: none;
      box-shadow: 0px 4px 20px rgba(0, 0, 0, 0.05);
      min-width: 170px;
      min-height: 10px;
      padding: 0;
    }

    .card-header{
        padding: 0;
        border-bottom: none;
        background-color: transparent;
    }

    .card-body {
        padding: 1rem;
    }

    .img-card {
        width: 100%;
        height: 180px;
        object-fit: cover;
        border-top-left-radius: 1.25rem;
        border-top-right-radius: 1.25rem;
    }

    .title-product {
        font-size: 0.85rem;
    }

    .price-product {
        font-size: 1rem;
        font-weight: 700;
    }

    .discount-product {
        font-weight: normal;
        font-size: 0.75rem;
        text-decoration: line-through;
    }

</style>
