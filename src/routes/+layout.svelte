<script>
  let links = [
    { name: "Home", href: "/" },
    { name: "Speakers", href: "/speakers" },
    { name: "Schedule", href: "/schedule" },
    { name: "Sponsors", href: "/sponsors" },
    { name: "About", href: "/about" },
    { name: "Contact", href: "/contact" }
  ];
</script>

<header>
  <nav>
    <!-- Logo & Title -->
    <div class="logo-container">
      <a href="/">
        <img src="/logo.gif" alt="Tech Conference Logo" class="logo">
      </a>
      <a href="/" class="title">Tech Conference 2025</a>
    </div>

    <!-- Navigation Links -->
    <ul>
      {#each links as link}
        <li><a href={link.href}>{link.name}</a></li>
      {/each}
    </ul>
  </nav>
</header>

<main>
  <slot />
</main>

<footer>
  <p>&copy; 2025 Tech Conference. All rights reserved.</p>
</footer>

<style>
  /* Navbar */
  header {
    background:#333 ;
    padding: 10px 20px;
    color: white;
  }

  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  /* Logo and Title */
  .logo-container {
    display: flex;
    align-items: center;
  }

  .logo {
    height: 50px; /* Adjust based on your logo size */
    margin-right: 10px;
  }

  .title {
    text-decoration: none;
    color: white;
    font-size: 20px;
    font-weight: bold;
  }

  /* Navigation Links */
  ul {
    list-style: none;
    display: flex;
    gap: 20px;
  }

  li a {
    text-decoration: none;
    color: white;
    font-weight: bold;
  }

  li a:hover {
    color: #00f2fe;
  }

  /* Footer */
  footer {
    text-align: center;
    padding: 10px;
    background: #222;
    color: white;
    margin-top: 20px;
  }
</style>
