<script>
  import { onMount } from "svelte";

  let countdown = "";
  const eventDate = new Date("2025-04-15T09:00:00"); // Event Date

  function updateCountdown() {
    const now = new Date();
    const difference = eventDate - now;

    if (difference > 0) {
      const days = Math.floor(difference / (1000 * 60 * 60 * 24));
      const hours = Math.floor((difference / (1000 * 60 * 60)) % 24);
      const minutes = Math.floor((difference / (1000 * 60)) % 60);
      countdown = `${days}d ${hours}h ${minutes}m`;
    } else {
      countdown = "Event Started!";
    }
  }

  onMount(() => {
    updateCountdown();
    setInterval(updateCountdown, 60000); // Update every minute
  });

  let highlights = [
    { title: "🔥 Cutting-Edge Talks", description: "Insights from world-class speakers on AI, Cloud, and IoT." },
    { title: "💡 Hands-On Workshops", description: "Practical learning with industry experts guiding you." },
    { title: "🤝 Networking Hub", description: "Meet industry leaders and build valuable connections." },
    { title: "🚀 Startup Showcases", description: "Experience innovative demos from emerging startups." },
    { title: "📈 Career Advancement", description: "Get insights from industry leaders and explore new job opportunities." },
    { title: "🎓 Exclusive Certifications", description: "Earn certificates from hands-on workshops to boost your resume." }
  ];
</script>

<section class="hero">
  <div class="container">
    <h1> Tech Conference 2025</h1>
    <p>The ultimate gathering of innovators, engineers, and thought leaders.</p>
    
    <div class="countdown">
      <span>Event Starts In:</span>
      <strong>{countdown}</strong>
    </div>

    <a href="/register" class="cta-button">Register Now</a>
  </div>
</section>

<section class="highlights">
  <div class="container">
    <h2>Why Attend?</h2>
    <div class="grid">
      {#each highlights as item}
        <div class="card">
          <h3>{item.title}</h3>
          <p>{item.description}</p>
        </div>
      {/each}
    </div>
  </div>
</section>

<style>
  /* Hero Section */
  .hero {
    background: linear-gradient(to right, #007bff, #00f2fe);
    color: white;
    text-align: center;
    padding: 80px 20px;
    animation: fadeIn 1s ease-in-out;
  }

  .hero .container {
    max-width: 800px;
    margin: auto;
  }

  .hero h1 {
    font-size: 2.8rem;
    margin-bottom: 10px;
    font-weight: bold;
  }

  .hero p {
    font-size: 1.4rem;
    margin-bottom: 20px;
  }

  .countdown {
    font-size: 1.5rem;
    margin-bottom: 20px;
    font-weight: bold;
    background: rgba(255, 255, 255, 0.2);
    display: inline-block;
    padding: 10px 20px;
    border-radius: 20px;
  }

  .cta-button {
    display: inline-block;
    background: white;
    color: #007bff;
    padding: 12px 25px;
    font-size: 1.2rem;
    border-radius: 30px;
    font-weight: bold;
    text-decoration: none;
    transition: 0.3s ease-in-out;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  }

  .cta-button:hover {
    background: #0056b3;
    color: white;
    transform: scale(1.05);
  }

  /* Highlights Section */
  .highlights {
    background: #f9f9f9;
    text-align: center;
    padding: 60px 20px;
  }

  .highlights .container {
    max-width: 900px;
    margin: auto;
  }

  .highlights h2 {
    font-size: 2.5rem;
    margin-bottom: 20px;
    color: #333;
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    margin-top: 30px;
  }

  .card {
    background: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: 0.3s ease-in-out;
  }

  .card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15);
  }

  .card h3 {
    color: #007bff;
    margin-bottom: 10px;
    font-size: 1.5rem;
  }

  .card p {
    color: #555;
    font-size: 1.1rem;
    line-height: 1.5;
  }

  /* Animations */
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(-20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>
