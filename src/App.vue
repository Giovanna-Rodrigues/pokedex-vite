<script setup>

</script>

<template>
  <!-- NAVBAR -->
  <nav class="navbar navbar-expand-lg" style="background-color:#242a66;">
    <div class="container-fluid">
      <router-link class="navbar-brand" to="/">
        <img src="./assets/pngegg.png" alt="logo" width="13%" class="d-inline-block align-text-top">
      </router-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link class="nav-link" aria-current="page" to="/">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/about">About</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- CONTENT -->
   <div class="main">
    <router-view/>
   </div>

   <footer style="background-color:#242a66;">
    <div>{{ new Date().getFullYear() }}</div>
   </footer>
</template>

<style>
footer{
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 56px;
}
</style>