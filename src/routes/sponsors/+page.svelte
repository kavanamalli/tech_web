<script>
  let sponsors = [
    {
      tier: "Platinum Sponsors",
      companies: [
        { name: "Google", logo: "/images/google.svg", link: "https://google.com" },
        { name: "Microsoft", logo: "/images/microsoft.svg", link: "https://microsoft.com" }
      ]
    },
    {
      tier: "Gold Sponsors",
      companies: [
        { name: "Amazon", logo: "/images/amazon.svg", link: "https://amazon.com" },
        { name: "IBM", logo: "/images/ibm.svg", link: "https://ibm.com" }
      ]
    },
    {
      tier: "Silver Sponsors",
      companies: [
        { name: "Infosys", logo: "/images/infosys.png", link: "https://infosys.com" },
        { name: "TCS", logo: "/images/tcs.png", link: "https://tcs.com" }
      ]
    }
  ];
</script>

<section class="sponsors">
  <h1>Our Sponsors</h1>

  {#each sponsors as sponsor}
    <div class="tier">
      <h2>{sponsor.tier}</h2>
      <div class="grid">
        {#each sponsor.companies as company}
          <a href={company.link} target="_blank" class="card">
            <img src={company.logo} alt={company.name} />
            <p>{company.name}</p>
          </a>
        {/each}
      </div>
    </div>
  {/each}

  <div class="cta">
    <h2>Become a Sponsor</h2>
    <p>Partner with us to gain exclusive branding opportunities and global exposure.</p>
    <a href="/contact" class="btn">Join as Sponsor</a>
  </div>
</section>

<style>
  .sponsors {
    text-align: center;
    padding: 60px 20px;
    background: #f4f4f4;
  }
  
  h1 {
    font-size: 2.5rem;
    color: #222;
    font-weight: bold;
    margin-bottom: 30px;
  }

  .tier {
    margin-top: 40px;
  }

  .tier h2 {
    font-size: 1.8rem;
    color: #0056b3;
    font-weight: 600;
    text-transform: uppercase;
    margin-bottom: 20px;
  }

  .grid {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 30px;
  }

  .card {
    background: white;
    padding: 15px;
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    text-align: center;
    width: 180px;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .card:hover {
    transform: translateY(-5px);
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);
  }

  .card img {
    width: 100%;
    height: auto;
    max-height: 80px;
    margin-bottom: 10px;
    filter: grayscale(30%);
    transition: filter 0.3s ease;
  }

  .card:hover img {
    filter: grayscale(0%);
  }

  .card p {
    font-size: 1.1rem;
    font-weight: 500;
    color: #333;
    margin-top: 8px;
  }

  .cta {
    margin-top: 50px;
    padding: 30px;
    background: #fff;
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
  }

  .cta h2 {
    font-size: 1.8rem;
    font-weight: 600;
    color: #222;
    margin-bottom: 10px;
  }

  .cta p {
    font-size: 1.1rem;
    color: #555;
  }

  .btn {
    display: inline-block;
    background: #007bff;
    color: white;
    padding: 12px 20px;
    margin-top: 15px;
    text-decoration: none;
    border-radius: 6px;
    font-weight: bold;
    transition: background 0.3s ease;
  }

  .btn:hover {
    background: #0056b3;
  }
</style>
