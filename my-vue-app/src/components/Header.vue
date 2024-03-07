<template>
  <header class="header">
    <nav class="navbar">
      <div class="container">
        <router-link to="/" class="logo">
          <img src="./logofinal.png" alt="Logo" class="logo-img">
        </router-link>
        <ul class="nav-links">
          <li><router-link to="/">Accueil</router-link></li>
          <li><router-link to="/login">Login</router-link></li>
          <li><router-link to="/contact">Contact</router-link></li>
          <li><router-link to="/QuiSommesNous">Qui sommes nous?</router-link></li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<style>
/* Supprimer les marges de la page */
body, html {
  margin: 0;
  padding: 0;
}

.header {
  width: 100%;
  background-image: linear-gradient(to left top, #1c253c, #2f3751, #424a66, #575e7d, #6c7294, #707595, #747997, #787c98, #6b6e84, #5f6070, #52525d, #45454a);
}

.navbar {
  width: 100%;
}

.container {
  width: 80%; /* ajustez selon vos besoins */
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: column; /* Pour aligner les éléments en colonne */
}

.logo {
  text-decoration: none;
}

.logo-img {
  width: 350px; 
  margin-bottom: 10px; 
}

.nav-links {
  list-style-type: none;
  display: flex;
  margin: 30px;
  padding: 0;
}

.nav-links li {
  margin-right: 20px;
}

.nav-links li:last-child {
  margin-right: 0;
}

.nav-links li a {
  text-decoration: none;
  color: #fff;
}

.nav-links li a:hover {
  color: #007bff;
}
</style>
