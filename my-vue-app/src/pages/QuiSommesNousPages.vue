<template>
  <div>
    <div x-data="{ navOpen: false }">
      <header x-show="!navOpen" class="bg-blue-900 p-4 text-white text-center">
        <h1 class="text-3xl font-bold">Qui sommes-nous ?</h1>
      </header>
    </div>

    <main class="max-w-4xl mx-auto p-4 text-center">
      <h1 class="text-3xl font-bold mb-4">
        Abderrahmane Bessalah - Etudiant Développeur
      </h1>
      <p class="mb-4">
        Je suis un étudiant en développement et en data à Efrei Paris, passionné
        par les nouvelles technologies et déterminé à construire une carrière
        réussie dans ce domaine en constante évolution.
      </p>

      <!-- Information about additional persons -->
      <div class="flex justify-around">
        <div>
          <h2 class="text-xl font-bold">Noé Le Roux</h2>
          <p>
            Je suis un étudiant en développement et en data à Efrei Paris,
            passionné par les nouvelles technologies et déterminé à construire
            une carrière réussie dans ce domaine en constante évolution
          </p>
        </div>
        <div>
          <h2 class="text-xl font-bold">Ilian Kherbouche</h2>
          <p>
            Je suis un étudiant en développement et en data à Efrei Paris,
            passionné par les nouvelles technologies et déterminé à construire
            une carrière réussie dans ce domaine en constante évolution
          </p>
        </div>
        <div>
          <h2 class="text-xl font-bold">Dorian Franot</h2>
          <p>
            Je suis un étudiant en développement et en data à Efrei Paris,
            passionné par les nouvelles technologies et déterminé à construire
            une carrière réussie dans ce domaine en constante évolution
          </p>
        </div>
      </div>
    </main>

    <footer class="bg-black text-white text-center p-4">
      <h2 class="text-2xl">Merci à vous</h2>
    </footer>
  </div>
</template>

<script>
export default {
  name: "QuiSommesNous",
};
</script>
<style scoped>
  /* Header styles */
 
  header {
    background-color: #1a202c;
    padding: 1rem;
    color: #fff;
    text-align: center;
  }

  header a {
    margin: 0 0.5rem;
  }

  /* Main styles */
  main {
    max-width: 40rem;
    margin: 0 auto;
    padding: 1rem;
    text-align: center;
  }

  h1 {
    font-size: 1.5rem;
    font-weight: bold;
    margin-bottom: 1rem;
  }

  p {
    margin-bottom: 1rem;
  }

  /* Additional persons styles */
  .flex {
    justify-content: space-around;
  }

  .flex > div {
    flex-basis: 30%;
  }

  h2 {
    font-size: 1.25rem;
    font-weight: bold;
  }

  /* Footer styles */
  footer {
    background-color: #000;
    color: #fff;
    text-align: center;
    padding: 1rem;
  }

  h2 {
    font-size: 2rem;
  }
</style>