<template>
<div>
  <b-navbar toggleable="lg" type="dark"  style="background-color:#2B42A3;">
    <b-container>
      <b-navbar-brand :to="'/'">DWStore</b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse class="ml-auto mx-auto" id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item :to="'/'">Home</b-nav-item>
        </b-navbar-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-form>

          </b-nav-form>
        </b-navbar-nav>
      </b-collapse>
    </b-container>
  </b-navbar>
  <b-row>
    <b-col md="12" cols="12">
      <div class="search-bar">
        <b-form-input
          class="search-box"
          size="sm"
          placeholder="Type Something"
        ></b-form-input>
        <div class="button-search">
          <nuxt-link :to="'/search'">
            <font-awesome-icon :icon="['fas', 'search']" :style="{color:'white', fontSize:14}" />
          </nuxt-link>
        </div>
      </div>
    </b-col>
  </b-row>
  <nuxt />
  <b-row class="mt-5">

  </b-row>
</div>
</template>

<style scoped>

  .nav-link {
    color: white !important;
    padding-right: 1rem !important;
    padding-left: 1rem !important;
    font-weight: 300;
    font-size: 14px;
  }

  .navbar-toggler, .navbar-toggler:focus, .navbar-toggler:active {
      outline: 0;
      border: 0;
      box-shadow: none;
  }

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
