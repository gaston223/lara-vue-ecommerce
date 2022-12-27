<!--
  This example requires some changes to your config:

  ```
  // tailwind.config.js
  module.exports = {
    // ...
    plugins: [
      // ...
      require('@tailwindcss/forms'),
    ],
  }
  ```
-->
<template>
    <!--
      This example requires updating your template:

      ```
      <html class="h-full bg-gray-50">
      <body class="h-full">
      ```
    -->
    <div class="flex min-h-full items-center justify-center py-12 px-4 sm:px-6 lg:px-8">
        <div class="w-full max-w-md space-y-8">
            <div>
                <h2 class="mt-6 text-center text-3xl font-bold tracking-tight text-gray-900">Créer un nouveau mot de passe</h2>
            </div>
            <form class="mt-8 space-y-6" action="#" method="POST">
                <input type="hidden" name="remember" value="true" />

                <div class="-space-y-px rounded-md shadow-sm">
                    <div>
                        <label for="new-password" class="sr-only">Nouveau mot de passe</label>
                        <input id="new-password" name="password" type="password" required="" class="relative block w-full appearance-none rounded-none rounded-t-md border border-gray-300 px-3 py-2 text-gray-900 placeholder-gray-500 focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm" placeholder="Nouveau mot de passe" />
                    </div>
                    <div>
                        <label for="password-repeat" class="sr-only">Répétez le mot de passe</label>
                        <input id="password-repeat" name="password-repeat" type="password" required="" class="relative block w-full appearance-none rounded-none rounded-b-md border border-gray-300 px-3 py-2 text-gray-900 placeholder-gray-500 focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm" placeholder="Répétez le mot de passe" />
                    </div>
                </div>

                    <div class="text-sm">
                        <router-link :to="{name: 'requestPassword'}" class="font-medium text-indigo-600 hover:text-indigo-500">Se connecter</router-link>
                    </div>


                <div>
                    <button type="submit" class="group relative flex w-full justify-center rounded-md border border-transparent bg-indigo-600 py-2 px-4 text-sm font-medium text-white hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2">
            <span class="absolute inset-y-0 left-0 flex items-center pl-3">
              <LockClosedIcon class="h-5 w-5 text-indigo-500 group-hover:text-indigo-400" aria-hidden="true" />
            </span>
                       Envoyer
                    </button>
                </div>
            </form>
        </div>
    </div>
</template>

<script setup>
import { LockClosedIcon } from '@heroicons/vue/20/solid'
</script>

<style scoped>

</style>
