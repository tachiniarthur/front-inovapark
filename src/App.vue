<script setup>
import { onMounted } from 'vue'

onMounted(async () => {
  try {
    createUser()
    const response = await fetch('http://localhost:8080/users')
    if (!response.ok) {
      throw new Error(`Erro na requisição: ${response.statusText}`)
    }
    const data = await response.json()
    console.log('Dados da API:', data)
  } catch (error) {
    console.error('Erro ao buscar dados da API:', error)
  }
})

async function createUser() {
  const matricula = '123455'
  const cpf = '123456789002'
  const senha = '12345678900'
  const nomeCompleto = '123456789003'
  const email = '123456789005'

  const response = await fetch('http://localhost:8080/users', {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
    },
    body: JSON.stringify({
      matricula: matricula,
      cpf: cpf,
      senha: senha,
      nome: nomeCompleto,
      email: email,
    }),
  })

  if (!response.ok) {
    throw new Error(`Erro na requisição: ${response.statusText}`)
  }
  const data = await response.json()
  console.log('Dados do usuário criado:', data)
  return data
}
</script>

<template>
  <main>
    <p class="text-3xl underline">FRONT INOVAPARK</p>
  </main>
</template>

<style scoped></style>
