<template>
  <div>
    <b-navbar toggleable="md" type="dark" variant="info">
      <b-navbar-brand href="#">Hacktiv8 WP</b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item href="#" @click.prevent="logout" v-if="status">Logout</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  props: ["status"],
  data() {
    return {};
  },
  methods: {
    logout() {
      this.$emit("logout", "logout");
    }
  }
};
</script>

<style>
</style>