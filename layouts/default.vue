<template>
<div>
  <b-navbar toggleable="lg" style="background-color:#2B42A3">
    <b-container>
      <b-navbar-brand href="#">NavBar</b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse class="ml-auto mx-auto" id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="#">Home</b-nav-item>
          <b-nav-item href="#">Home</b-nav-item>
          <b-nav-item href="#">Home</b-nav-item>
        </b-navbar-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-form>

          </b-nav-form>
        </b-navbar-nav>
      </b-collapse>
    </b-container>
  </b-navbar>
  <nuxt />
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

</style>
