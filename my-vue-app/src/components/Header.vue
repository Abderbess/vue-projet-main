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
  background-image: linear-gradient(to left top, #242423f1, #3f3f3ef1, #686865f1);
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
  width: 350px; /* ajustez selon la taille de votre logo */
  margin-bottom: 10px; /* Ajout de marge en bas pour l'espace */
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
