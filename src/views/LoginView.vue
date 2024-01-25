<template>
  <div class="font-sans text-gray-900 antialiased">
    <div
      class="min-h-screen flex flex-col sm:justify-center items-center pt-12 bg-gray-100"
    >
      <div>
        <a href="/">
          <img
            src="@/assets/logo-ghislain.png"
            class="fill-current text-gray-500"
          />
        </a>
      </div>
      <div
        class="max-w-md mt-6 px-6 py-4 bg-white shadow-md overflow-hidden sm:rounded-lg"
      >
        <h2 class="text-center text-xl leading-8">Accés Client</h2>
        <form @submit.prevent="login">
          <div>
            <label for="email" class="block font-medium text-sm text-gray-700">
              Email
            </label>
            <input
              id="email"
              v-model="email"
              type="email"
              name="email"
              class="border-gray-300 py-1.5 px-3 ring-1 ring-inset ring-gray-300 focus:border-indigo-500 focus:ring-indigo-500 rounded-md shadow-sm block mt-1 w-full"
              required
              autofocus
              autocomplete
            />
          </div>

          <div class="mt-4">
            <label
              for="password"
              class="block font-medium text-sm text-gray-700"
            >
              Password
            </label>
            <input
              id="password"
              v-model="password"
              type="password"
              name="password"
              class="border-gray-300 py-1.5 px-3 ring-1 ring-inset ring-gray-300 focus:border-indigo-500 focus:ring-indigo-500 rounded-md shadow-sm block mt-1 w-full"
              required
              autofocus
              autocomplete
            />
          </div>

          <div class="block mt-4">
            <label for="remember_me" class="inline-flex items-center">
              <input
                id="remember_me"
                type="checkbox"
                class="rounded border-gray-300 text-indigo-600 shadow-sm focus:ring-indigo-500"
                name="remember"
              />
              <span class="ml-2 text-sm text-gray-600">Remember me</span>
            </label>
          </div>

          <div class="flex items-center justify-end mt-4">
            <a
              class="underline text-sm text-gray-600 hover:text-gray-900 rounded-md focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
              href=""
            >
              Forgot your password?
            </a>

            <button
              type="submit"
              class="ml-3 inline-flex items-center px-4 py-2 bg-gray-800 border border-transparent rounded-md font-semibold text-xs text-white uppercase tracking-widest hover:bg-gray-700 focus:bg-gray-700 active:bg-gray-900 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2 transition ease-in-out duration-150"
            >
              Log in
            </button>
          </div>
        </form>
        <p v-if="errorMessage" class="text-red-500 mt-4">{{ errorMessage }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: "",
      password: "",
      errorMessage: "",
    };
  },
  methods: {
    login() {
      // Ajoutez ici la logique de connexion, par exemple, une requête API.
      console.log("Connexion avec:", this.email, this.password);

      // Simule une erreur (vous devez remplacer cela par votre logique de gestion d'erreur réelle)
      this.errorMessage = "Les informations de connexion sont incorrectes.";
      // Redirigez l'utilisateur vers une autre page après la connexion.

      // Vous pouvez également réinitialiser les champs de formulaire après une tentative de connexion
      this.email = "";
      this.password = "";

      //   this.$router.push("/dashboard");
    },
  },
};
</script>

<style scoped>
/* Styles spécifiques à cette page */
.text-red-500 {
  color: #e3342f; /* Rouge Tailwind CSS */
}
</style>
