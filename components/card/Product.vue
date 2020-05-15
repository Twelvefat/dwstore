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
              <img src="https://cf.shopee.co.id/file/fb4f1f1ab0c6bb8754dc4884d0b36dfa" class="img-card" />
          </div>
          <div class="card-body">
              <p class="title-product grey-2"> Baju langka supreme hanya ada 1 didunia </p>
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
                <b-col class="mt-2 text-center">
                    <nuxt-link :to="''" class="btn btn-detail"> Detail </nuxt-link>
                </b-col>
                <b-col class="mt-2 text-center">
                    <nuxt-link :to="''" class="btn btn-buy"> Buy </nuxt-link>
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

    .label-container {
        position: absolute;
        top: 0;
        right: 0;
        margin-top: 10px;
        margin-right: 10px;
    }

    .label-discount {
      position: relative;
      display: block;
      background-color: #60C887;
      min-width: 50px;
      height: 25px;
      border-radius: 1.25rem;
      padding: 0.25rem 0.625rem;
      font-size: 0.75rem;
      color: white;
      text-align: center;
      margin: 0.15rem 0;
    }

    .label-new {
      position: relative;
      display: block;
      background-color: #F2783F;
      min-width: 50px;
      height: 25px;
      border-radius: 1.25rem;
      padding: 0.25rem 0.625rem;
      font-size: 0.75rem;
      color: white;
      text-align: center;
      margin: 0.15rem 0;
      font-style: italic;
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

    .btn {
      width: 90%;
      /* min-width: 6rem; */
    }

    .btn-detail {
        border: 1px solid #1C56D9;
        color: #1C56D9;
        background-color: white;
        padding: 0.38rem 1.9rem;
        border-radius: 1.25rem;
        font-size: 0.75rem;
    }

    .btn-buy {
        border: 1px solid transparent;
        color: white;
        background-color: #1C56D9;
        padding: 0.38rem 1.9rem;
        border-radius: 1.25rem;
        font-size: 0.75rem;
    }

</style>
