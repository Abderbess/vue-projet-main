<template>
  <footer class="footer">
    <nav>
      <div class="entreprise-info">
        <h3>Coordonnées de l'entreprise</h3>
        <p>Interí-Siège social : Immeuble Ordinal - 123 rue des Mec cools</p>
        <p>Tel: 0973892686 </p>
        <p>Email: emailstyle@gmail.com </p>
      </div>

      <div class="social-icons">
        <a href="https://www.facebook.com/EfreiParis" target="_blank" class="social-icon">
          <img class="img-custom" src="./facebook.png" alt="Facebook">
        </a>

        <a href="https://www.instagram.com/efrei_paris/" target="_blank" class="social-icon">
          <img class="img-custom" src="./instagramm.png" alt="Instagram">
        </a>

        <a href="https://twitter.com/Efrei_Paris" target="_blank" class="social-icon">
          <img class="img-custom" src="./X.jpg" alt="Twitter">
        </a>

        <a href="https://www.linkedin.com/school/efrei/" target="_blank" class="social-icon">
          <img class="img-custom" src="./Linkedin.png" alt="Linkedin">
        </a>
      </div>
    </nav>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>
.footer {
  display: flex;
  justify-content: center;
  align-items: center;
 background-image: linear-gradient(to left bottom, #1c253c, #20283e, #252b41, #292f43, #2d3246, #2b3457, #293667, #273778, #11369a, #0032bc, #0028db, #0509f9);
}

.entreprise-info {
  margin-bottom: 20px;
  text-align: center;
  color: #fff;
}

.social-icons {
  display: flex;
  justify-content: center;
}

.social-icon {
  margin-right: 20px;
}

.img-custom {
  width: 40px;
  height: 40px;
  border-radius: 50%; /* Met les images en forme de cercle */
  transition: transform 0.3s ease; /* Animation de transition pour le grossissement */
}

.img-custom:hover {
  transform: scale(1.3); /* Grossissement au survol */
}
</style>
