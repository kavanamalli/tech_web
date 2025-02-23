<script>
  let speakers = [
    {
      name: "Nandan Nilekani",
      title: "Co-founder, Infosys",
      image: "/images/speaker1.png",
      bio: "A pioneer in Indian IT, leading digital identity and financial inclusion."
    },
    {
      name: "Narayana Murthy",
      title: "Founder, Infosys",
      image: "/images/speaker2.png",
      bio: "A visionary leader who transformed India's IT industry and inspired a generation of entrepreneurs."
    },
    {
      name: "Dr. Priya Sharma",
      title: "AI & Data Science Professor, IIT Bombay",
      image: "/images/speaker3.png",
      bio: "A leading researcher in artificial intelligence and data science, shaping the future of AI in India."
    }
  ];
</script>

<section class="speakers">
  <h1>Meet Our Speakers</h1>
  <div class="grid">
    {#each speakers as speaker}
      <div class="card">
        <img src={speaker.image} alt={speaker.name} />
        <h2>{speaker.name}</h2>
        <h3>{speaker.title}</h3>
        <p>{speaker.bio}</p>
      </div>
    {/each}
  </div>
</section>

<style>
  .speakers {
    text-align: center;
    padding: 50px 20px;
    background: #f9f9f9;
  }
  
  h1 {
    font-size: 2rem;
    color: #333;
    margin-bottom: 30px;
  }

  .grid {
    display: flex;
    gap: 30px;
    justify-content: center;
    flex-wrap: wrap;
  }

  .card {
    background: white;
    padding: 25px;
    border-radius: 12px;
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
    max-width: 300px;
    text-align: center;
    transition: transform 0.3s ease-in-out;
  }

  .card:hover {
    transform: translateY(-5px);
  }

  .card img {
    width: 200px;
    height: 200px;
    object-fit: cover;
    border-radius: 50%;
    margin-bottom: 15px;
    border: 4px solidrgb(26, 49, 60);
  }

  h2 {
    font-size: 1.5rem;
    color:rgb(30, 56, 84);
    margin-bottom: 10px;
  }

  h3 {
    font-size: 1.5rem;
    color: #555;
    font-weight: normal;
  }

  p {
    font-size: 0.9rem;
    color: #666;
    margin-top: 10px;
  }

  @media (max-width: 768px) {
    .grid {
      flex-direction: column;
      align-items: center;
    }
  }
</style>
