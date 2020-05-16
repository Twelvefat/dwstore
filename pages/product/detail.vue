<template>
  <b-container>
    <b-row class="mt-5">
      <b-col md="4" sm="12" cols="12">
        <client-only>
          <div v-if="!this.isLoading">
            <slick ref="carouselThumbnailImage" :options="thumbnailImage" id="thumbnailImage">
              <img src="https://cf.shopee.co.id/file/fb4f1f1ab0c6bb8754dc4884d0b36dfa" class="thumbnail-image"/>
              <img src="https://www.worldofghibli.id/wp-content/uploads/2020/02/gambar-gambar-baju.jpg" class="thumbnail-image"/>
              <img src="https://cf.shopee.co.id/file/fb4f1f1ab0c6bb8754dc4884d0b36dfa" class="thumbnail-image"/>
              <img src="https://cf.shopee.co.id/file/fb4f1f1ab0c6bb8754dc4884d0b36dfa" class="thumbnail-image"/>
            </slick>
          </div>
          <div class="mt-3" v-if="!this.isLoading">
            <slick ref="carouselsubImage" :options="subImage" id="subImage">
              <img src="https://cf.shopee.co.id/file/fb4f1f1ab0c6bb8754dc4884d0b36dfa" class="sub-image"/>
              <img src="https://www.worldofghibli.id/wp-content/uploads/2020/02/gambar-gambar-baju.jpg" class="sub-image"/>
              <img src="https://cf.shopee.co.id/file/fb4f1f1ab0c6bb8754dc4884d0b36dfa" class="sub-image"/>
              <img src="https://cf.shopee.co.id/file/fb4f1f1ab0c6bb8754dc4884d0b36dfa" class="sub-image"/>
            </slick>
          </div>
        </client-only>
      </b-col>
      <b-col md="8" sm="12" cols="12">
        <b-row>
          <b-col>
            <h1 class="title-product grey-2 mt-3"> Baju langka supreme hanya ada  1 di dunia </h1>
          </b-col>
        </b-row>
        <b-row>
          <b-col>
            <div class="label-container">
              <div class="label-discount mr-1">
                <p>-15%</p>
              </div>
              <div class="label-new">
                <p>New</p>
              </div>
            </div>
          </b-col>
        </b-row>
        <b-row class="mt-1">
          <b-col>
            <div>
              <span class="price-product orange-1"> Rp 150.000 </span>
              <span class="discount-product grey-5"> Rp 250.000 </span>
            </div>
          </b-col>
        </b-row>
        <b-row>
          <b-col>
            <div class="d-flex flex-row align-items-center">
              <client-only>
                <star-rating
                  v-model="rating"
                  :star-size="20"
                  :show-rating="false"
                  :rounded-corners="false"
                  :padding="0"
                  :read-only="true"
                  :round-start-rating="false"
                ></star-rating>
              </client-only>
              <div class="ml-2">
                <h5 class="reviews grey-3 mt-3"> 4.4 (762 Reviews) </h5>
              </div>
            </div>
          </b-col>
        </b-row>
        <b-row class="mt-4">
          <b-col>
            <p class="mark"> Detail </p>
          </b-col>
        </b-row>
        <b-row class="p-1">
          <b-col>
            <div class="d-flex flex-row justify-content-between mt-1">
              <h5 class="text-category grey-3"> Kategori </h5>
              <h5 class="text-category grey-3"> Baju Wanita </h5>
            </div>
            <div class="d-flex flex-row justify-content-between mt-1">
              <h5 class="text-category grey-3"> min Pembelian </h5>
              <h5 class="text-category grey-3"> 1 </h5>
            </div>
            <div class="d-flex flex-row justify-content-between mt-1">
              <h5 class="text-category grey-3"> Berat </h5>
              <h5 class="text-category grey-3"> 350gr </h5>
            </div>
            <div class="d-flex flex-row justify-content-between mt-1">
              <h5 class="text-category grey-3"> Asuransi </h5>
              <h5 class="text-category grey-3"> Ya </h5>
            </div>
          </b-col>
        </b-row>
      </b-col>
    </b-row>
    <b-row class="mt-5">
      <b-col>
        <b-row>
          <b-col>
            <p class="mark"> Description </p>
          </b-col>
        </b-row>
        <b-row class="mt-3 pr-2 pl-2">
          <b-col>
            <p class="text-description grey-3"> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam mollis velit ligula, eu rhoncus mauris laoreet mattis. Cras a dolor neque. In cursus eget orci sit amet placerat. In mollis, lectus a vestibulum vulputate, nunc quam pulvinar lacus, a auctor felis eros et est. Ut porttitor condimentum nunc, bibendum mollis nunc tempor ut. Proin suscipit lectus non nulla dictum dictum. Donec  cursus porttitor tortor, ac aliquam ante. Maecenas eros risus, scelerisque non nisl sed, fermentum egestas augue. Maecenas egestas elementum arcu, id aliquam tellus imperdiet egestas. Nulla leo nunc, feugiat non ultricies id, maximus et nisi.  Pellentesque sed ex vitae nulla viverra ullamcorper. Suspendisse mollis consequat ipsum, ac faucibus nulla mattis et. </p>
          </b-col>
        </b-row>
      </b-col>
    </b-row>
    <b-row class="mt-5">
      <b-col>
        <b-row>
          <b-col>
            <p class="mark"> Reviews </p>
          </b-col>
        </b-row>
        <b-row class="mt-3 pr-2 pl-2">
          <b-col>
            <b-row v-for="(n, index) in 3" :key="index">
              <b-col>
                <client-only>
                  <star-rating
                    v-model="rating"
                    :star-size="18"
                    :show-rating="false"
                    :rounded-corners="false"
                    :padding="0"
                    :read-only="true"
                    :round-start-rating="false"
                  ></star-rating>
                </client-only>
                <div class="mt-4">
                  <p class="rating-username grey-2"> Rizal Fatahillah </p>
                  <p class="rating-description grey-2"> Barang nya rusak gan gak bisa digunain. nyesel deh beli disini, nanti2 gak mau lagi dah beli disini. Pengirimannya juga lama gw nanya sering diabaikan jadi kurang professional banget </p>
                </div>
                <hr v-if="index < 2"/>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
      </b-col>
    </b-row>
    <b-row class="mt-5">
      <b-col>
        <h5 class="grey-2"> Rekomendasi </h5>
      </b-col>
    </b-row>
    <b-row class="mt-5 no-gutters">
        <b-col class="mt-3 p-1" md="3" cols="6" v-for="n in 4" :key="n">
          <Product />
        </b-col>
    </b-row>
  </b-container>
</template>

<script>

import Product from  '~/components/card/Product'

export default {
  data:() => ({
    isLoading:true,
    rating:4.4,
    thumbnailImage: {
        infinite: false,
        slidesToShow: 1,
        asNavFor:"#subImage",
    },
    subImage: {
        arrows:false,
        slidesToScroll:1,
        slidesToShow:4,
        focusOnSelect: true,
        swipe:false,
        swipeToSlide:false,
        asNavFor:"#thumbnailImage",
        infinite:false
    },
  }),
  components: {
    Slick: () => import('vue-slick'),
    Product
  },
  async mounted(){
    this.isLoading = false
  },
}
</script>

<style scoped>
  .thumbnail-image {
      width: 100%;
      height: 350px;
      object-fit: cover;
      border-radius: 1.25rem;
      padding: 0.25rem;
      cursor: pointer;
  }

  .sub-image {
    width: 100%;
    max-width: 100px;
    height: 100px;
    object-fit: cover;
    border-radius: 1.25rem;
    padding: 0.25rem;
    cursor: pointer;
  }

  .title-product {
    font-size: 1.35rem;
    font-weight: normal;
  }

  .price-product {
    font-size: 1.65rem;
    font-weight: 700;
  }

  .discount-product{
    font-size: 1.35rem;
    font-weight: normal;
    text-decoration: line-through;
  }

  .label-container {
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  .reviews {
    font-size: 0.85rem;
  }

  .text-category {
    font-size: 0.85rem;
    font-weight: normal;
  }

  .text-description {
    font-size: 0.85rem;
  }

  .rating-username {
    font-size: 1rem;
    font-weight: normal;
  }

  .rating-description {
    font-size: 0.85rem;
  }

</style>
