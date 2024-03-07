<template>
  <main class="body">
  <div class="contact-pages">
    <h1>Contactez-nous</h1>
    <p>
      Pour toute question ou demande, veuillez remplir le formulaire ci-dessous
      :
    </p>

    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="name">Nom :</label>
        <input type="text" id="name" v-model="name" required />
      </div>

      <div class="form-group">
        <label for="email">Email :</label>
        <input type="email" id="email" v-model="email" required />
      </div>

      <div class="form-group">
        <label for="message">Message :</label>
        <textarea id="message" v-model="message" required></textarea>
      </div>

      <button type="submit">Envoyer</button>
    </form>

    <div v-if="showSuccessMessage" class="success-message">Message envoyé</div>
    <div v-if="showErrorMessage" class="error-message">
      Erreur lors de l'envoi du message
    </div>
  </div>
</main>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      message: "",
      showSuccessMessage: false,
      showErrorMessage: false,
    };
  },
  methods: {
    submitForm() {
      // Vérifie si tous les champs sont remplis
      if (this.name && this.email && this.message) {
        // Simuler l'envoi du formulaire en affichant simplement le message de succès
        this.showSuccessMessage = true;
        this.showErrorMessage = false;

        // Réinitialiser les champs du formulaire après un court délai
        setTimeout(() => {
          this.name = "";
          this.email = "";
          this.message = "";
          this.showSuccessMessage = false;
        }, 3000); // Réinitialiser après 3 secondes
      } else {
        this.showSuccessMessage = false;
        this.showErrorMessage = true;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

.body{
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: #C8AD7F;
}

.contact-pages {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.form-group {
  margin-bottom: 20px;
}

label {
  display: block;
  font-weight: bold;
}

input[type="text"],
input[type="email"],
textarea {
  width: 100%;
  padding: 10px;
  font-size: 16px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

input[type="text"]:focus,
input[type="email"]:focus,
textarea:focus {
  outline: none;
  border-color: #007bff;
}

button {
  padding: 10px 20px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 16px;
}

button:hover {
  background-color: #0056b3;
}

.success-message,
.error-message {
  margin-top: 10px;
  padding: 10px;
  color: #fff;
  font-weight: bold;
  border-radius: 5px;
}

.success-message {
  background-color: #28a745;
}

.error-message {
  background-color: #dc3545;
}

</style>
