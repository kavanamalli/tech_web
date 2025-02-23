<script>
  let aboutDetails = [
    { 
        title: "Our Mission", 
        description: "Empowering technology enthusiasts, professionals, and students by providing a platform to explore the latest innovations and trends in the industry." },
    { 
        title: "Our Vision", 
        description: "To create an inclusive and engaging technology conference that fosters learning, collaboration, and groundbreaking discussions for a better future." },
    { 
        title: "Unparalleled Learning", 
        description: "Engage with top-notch speakers and gain insights into AI, cloud computing, and emerging technologies." },
    { 
        title: "Interactive Sessions", 
        description: "Experience hands-on workshops, Q&A sessions, and real-time problem-solving challenges to enhance your skills." },
    { 
        title: "Collaborative Environment", 
        description: "Network with tech enthusiasts, industry professionals, and startups to build lasting connections." },
    { 
        title: "Future-Ready Insights", 
        description: "Stay ahead of the curve with expert discussions on the future of technology, industry disruptions, and the next big innovations." 
    }

  ];
</script>

<section class="about">
  <div class="container">
    <h1>About Tech Conference 2025</h1>
    <p>
      Tech Conference 2025 is more than just an event—it's a movement towards innovation, learning, and collaboration. Join us in an immersive experience that connects the brightest minds in technology.
    </p>

    <div class="details">
      {#each aboutDetails as item}
        <div class="card">
          <h3>{item.title}</h3>
          <p>{item.description}</p>
        </div>
      {/each}
    </div>
  </div>
</section>

<style>
  .about {
    padding: 60px 20px;
    text-align: center;
    background: #f4f4f4;
  }

  .container {
    max-width: 900px;
    margin: auto;
  }

  h1 {
    color: #222;
    font-size: 2.5rem;
  }

  p {
    font-size: 1.2rem;
    color: #555;
    line-height: 1.6;
  }

  .details {
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
  }
</style>