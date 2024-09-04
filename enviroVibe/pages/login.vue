<script setup lang="ts">
const supabase = useSupabaseClient()

const email = ref('')

const signInWithOtp = async () => {
  const { error } = await supabase.auth.signInWithOtp({
    email: email.value,
    options: {
      emailRedirectTo: 'http://localhost:3000/confirm',
    }
  })
  if (error) console.log(error)
}
</script>

<template>
  <div>Login!
    <form>
      <div class="inputs">
        <label for="email">Email</label>
        <div>{{ email }}</div>
        <input id="email" type="email" placeholder="email" v-model="email" />
      </div>
      <button type="submit" @click="signInWithOtp">Login</button>
    </form>
  </div>
</template>