<template>
  <b-container id="app" fluid>
    <b-row>
      <b-col>
        <b-navbar toggleable="lg" type="light" variant="light">
          <b-navbar-brand>
            <b-link :to="{ name: 'home' }">Inicio</b-link>
          </b-navbar-brand>
          <b-navbar-toggle target="navbar-nav"></b-navbar-toggle>
          <b-collapse id="navbar-nav" is-nav>
            <b-navbar-nav class="ml-auto">
              <b-nav-item>
                <b-link v-if="$auth.isAuthenticated" :to="{ name: 'profile' }">Perfil</b-link>
              </b-nav-item>
            </b-navbar-nav>
          </b-collapse>
        </b-navbar>
      </b-col>
    </b-row>
    <b-row>
      <b-col md="9">
        <router-view/>
      </b-col>
    </b-row>
  </b-container>
</template>

<script></script>

<style></style>