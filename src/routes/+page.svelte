<script lang="ts">
    import { onMount } from 'svelte';
  
    let username: string = '';
    let password: string = '';
    let error: string = '';
  
    function handleSubmit() {
      if (!username || !password) {
        error = 'Please fill in all fields';
        return;
      }
      error = '';
      console.log('Login successful with:', { username, password });
    }
  </script>
  
  <main class="flex items-center justify-center min-h-screen bg-gray-100">
    <div class="bg-white p-8 shadow-lg rounded-lg w-96">
      <h2 class="text-2xl font-bold text-center mb-6">Login</h2>
      
      {#if error}
        <p class="text-red-500 text-sm text-center mb-4">{error}</p>
      {/if}
      
      <form on:submit|preventDefault={handleSubmit}>
        <div class="mb-4">
          <label for="username" class="block text-sm font-medium text-gray-700">Username</label>
          <input 
            id="username" 
            type="text" 
            bind:value={username} 
            class="mt-1 p-2 w-full border rounded-md focus:ring focus:ring-blue-300 outline-none" 
            required
          />
        </div>
        
        <div class="mb-4">
          <label for="password" class="block text-sm font-medium text-gray-700">Password</label>
          <input 
            id="password" 
            type="password" 
            bind:value={password} 
            class="mt-1 p-2 w-full border rounded-md focus:ring focus:ring-blue-300 outline-none" 
            required
          />
        </div>
        
        <button 
          type="submit" 
          class="w-full bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded-md">
          Login
        </button>
      </form>
    </div>
  </main>
  