<template>
  <main class="h-screen w-full flex items-center justify-center bg-gray-50">
    <section class="w-full max-w-sm p-6 bg-white rounded-xl shadow-md">
      <img :src="'logo.png'" alt="Logo" class="w-48 mx-auto h-auto mb-4" />
      <h1 class="text-2xl font-bold text-center mb-4">Login</h1>
      <form method="POST">
        <div class="mb-4">
          <label for="email" class="block text-sm font-medium text-gray-700">Email</label>
          <input
            type="email"
            id="email"
            class="mt-1 block w-full p-2 border border-gray-300 rounded-md"
            required
          />
        </div>
        <div class="mb-4">
          <label for="password" class="block text-sm font-medium text-gray-700">Senha</label>
          <input
            type="password"
            id="password"
            class="mt-1 block w-full p-2 border border-gray-300 rounded-md"
            required
          />
          <a href="/forgot-password" class="text-sm font-light text-blue-600 hover:underline"
            >Esqueceu sua senha?</a
          >
        </div>
        <button
          type="submit"
          class="w-full py-2 px-4 bg-blue-600 text-white rounded-md hover:bg-blue-700 hover:scale-105 transition duration-200 cursor-pointer"
        >
          Entrar
        </button>
      </form>
      <p class="mt-4 text-sm text-center">
        Não tem uma conta? <a href="/register" class="text-blue-600 hover:underline">Registrar</a>
      </p>
      <p class="mt-4 text-sm text-center">
        Voltar para a <a href="/" class="text-blue-600 hover:underline">página inicial</a>
      </p>
    </section>
  </main>
</template>

<script setup></script>
