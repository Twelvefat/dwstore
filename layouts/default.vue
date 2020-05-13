<template>
<div>
  <b-navbar style="background-color:#2B42A3">
    <b-container>
      <b-navbar-brand href="#">NavBar</b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse class="ml-auto mx-auto" id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="#">Link</b-nav-item>
          <b-nav-item href="#">Link</b-nav-item>
          <b-nav-item href="#">Link</b-nav-item>
        </b-navbar-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-form>
            <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
            <div class="button-search">
              <div>
                A
              </div>
            </div>
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
  }

  .button-search {
      background-color: #5B7EF4;
      width: 40px;
      height: 40px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
  }

  .button-search div {
    vertical-align: middle;
  }

</style>
