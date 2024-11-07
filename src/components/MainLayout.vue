<template>
<div class="main-layout">
<nav class="navbar navbar-expand-lg navbar-light bg-light sticky-top">
  <div class="container-fluid">
    <router-link class="navbar-brand" to="/">cogent</router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <router-link class="nav-link" to="/">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/about">About Us</router-link>
        </li>
        
        <li class="nav-item">
          <router-link class="nav-link" to="/services">Services Us</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/contact">Contact Us</router-link>
        </li>
      </ul>
    </div>
   </div> 
</nav>

<main class="main-content container-fluid my-4">
	<router-view />
</main>

<AppFooter />
</div>
</template>

<script>
import AppFooter from "./AppFooter.vue";
import { provide } from "vue";

export default {
	name: "MainLayout",
	components: {
		AppFooter,
	},
	setup(){

		provide("footerText", "@2024 MyApp. All rights reserved.");
	},
};

</script>
<style>
 .main-content
 {
 min-height: calc(100vh - 100px);
 }

</style>