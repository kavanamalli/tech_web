<script>
  let name = "";
  let email = "";
  let phone = "";
  let submitted = false;

  function registerUser() {
    if (name && email && phone) {
      submitted = true;

      // Simulate form submission (replace this with actual API request later)
      setTimeout(() => {
        name = "";
        email = "";
        phone = "";
      }, 500);
    }
  }
</script>

<section class="register">
  <div class="container">
    <h1>Register for Tech Conference 2025</h1>

    {#if submitted}
      <div class="success-message">
        🎉 Registration Successful! Check your email for confirmation.
      </div>
    {:else}
      <form on:submit|preventDefault={registerUser}>
        <label for="name">Full Name</label>
        <input type="text" id="name" bind:value={name} required />

        <label for="email">Email Address</label>
        <input type="email" id="email" bind:value={email} required />

        <label for="phone">Phone Number</label>
        <input type="tel" id="phone" bind:value={phone} required />

        <button type="submit">Submit</button>
      </form>
    {/if}
  </div>
</section>

<style>
  .register {
    padding: 50px;
    text-align: center;
    background: #f9f9f9;
  }

  .container {
    max-width: 500px;
    margin: auto;
    background: white;
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  }

  h1 {
    color: #333;
    font-size: 2rem;
  }

  form {
    display: flex;
    flex-direction: column;
    gap: 15px;
    margin-top: 20px;
  }

  label {
    font-weight: bold;
    text-align: left;
    display: block;
  }

  input {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }

  button {
    padding: 12px;
    background: #007bff;
    color: white;
    border: none;
    font-size: 1rem;
    font-weight: bold;
    border-radius: 8px;
    cursor: pointer;
    transition: 0.3s;
  }

  button:hover {
    background: #0056b3;
  }

  .success-message {
    background: #d4edda;
    color: #155724;
    padding: 15px;
    border-radius: 8px;
    font-size: 1.2rem;
    font-weight: bold;
    margin-top: 20px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
</style>
