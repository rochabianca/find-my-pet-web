<template>
  <b-navbar toggleable="lg" type="dark" class="navbar__bg">
    <b-navbar-brand href="#">
      <img
        class="navbar__logo"
        :src="require('@/assets/images/logo.svg')"
        alt="Find My Pet Logo"
      />
      <span class="navbar__logo__name ml-1">Find My Pet</span>
    </b-navbar-brand>
    <b-navbar-toggle target="nav_collapse" />
    <b-collapse is-nav id="nav_collapse">
      <div class="ml-lg-auto m-0">
        <b-navbar-nav>
          <b-nav-item href="#">Perdidos</b-nav-item>
          <b-nav-item href="#">Achados</b-nav-item>
          <b-nav-item href="#">Adote</b-nav-item>
          <b-nav-item href="#">Entrar</b-nav-item>
          <b-nav-item href="#">Junte-se a nós</b-nav-item>
        </b-navbar-nav>
      </div>
    </b-collapse>
  </b-navbar>
</template>

<style lang="scss" scoped>
@import "@/assets/scss/variables.scss";

.navbar__bg {
  background: $primary;
}
.navbar__logo {
  width: 50px;
}
.navbar__logo__name {
  font-weight: 300;
}
</style>
