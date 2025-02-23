<script>
  let selectedDay = "All";
  let schedule = [
    {
      day: "Day 1",
      time: "10:00 AM",
      event: "Opening Keynote",
      speaker: "Nandan Nilekani",
      description: "Kickoff with an inspiring speech on India's digital transformation.",
    },
    {
      day: "Day 2",
      time: "11:00 AM",
      event: "AI in 2025",
      speaker: "Dr. Priya Sharma",
      description: "Exploring AI advancements and their impact on industries.",
    },
    {
      day: "Day 3",
      time: "10:30 AM",
      event: "Scaling Tech Startups",
      speaker: "Narayana Murthy",
      description: "A deep dive into building scalable technology solutions.",
    }
  ];
</script>

<section class="schedule">
  <h1>📅 Conference Schedule</h1>

  <!-- Day Filter Dropdown -->
  <label for="dayFilter">Filter by Day:</label>
  <select id="dayFilter" bind:value={selectedDay}>
    <option value="All">All Days</option>
    <option value="Day 1">Day 1</option>
    <option value="Day 2">Day 2</option>
    <option value="Day 3">Day 3</option>
  </select>

  <div class="timeline">
    {#each schedule.filter(session => selectedDay === "All" || session.day === selectedDay) as session, i}
      <div class="session" style="--delay: {i * 0.2}s">
        <div class="time">{session.time}</div>
        <div class="content">
          <h2>{session.event}</h2>
          {#if session.speaker}
            <p class="speaker"> {session.speaker}</p>
          {/if}
          <p class="description">{session.description}</p>
        </div>
      </div>
    {/each}
  </div>
</section>

<style>
  /* Main Schedule Section */
  .schedule {
    text-align: center;
    padding: 60px 20px;
    max-width: 900px;
    margin: auto;
  }

  h1 {
    font-size: 2.5rem;
    color: #007bff;
    margin-bottom: 20px;
    font-weight: bold;
    text-transform: uppercase;
    letter-spacing: 1.5px;
  }

  /* Dropdown Filter */
  label {
    font-weight: bold;
    font-size: 1.2rem;
  }

  select {
    margin: 10px;
    padding: 8px;
    font-size: 1rem;
    border-radius: 5px;
    border: 1px solid #ccc;
  }

  /* Timeline Layout */
  .timeline {
    display: flex;
    flex-direction: column;
    gap: 25px;
    position: relative;
  }

  .session {
    display: flex;
    align-items: center;
    gap: 20px;
    background: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
    position: relative;
    opacity: 0;
    transform: translateY(20px);
    animation: fadeInUp 0.8s ease-in-out forwards;
    animation-delay: var(--delay);
  }

  /* Timeline Line */
  .timeline::before {
    content: "";
    position: absolute;
    left: 50%;
    top: 0;
    width: 4px;
    height: 100%;
    background: linear-gradient(to bottom, #007bff, #00f2fe);
    transform: translateX(-50%);
  }

  .session:nth-child(even) {
    flex-direction: row-reverse;
  }

  /* Time Box */
  .time {
    background: #007bff;
    color: white;
    padding: 12px 18px;
    border-radius: 50px;
    font-weight: bold;
    min-width: 100px;
    text-align: center;
    font-size: 1.1rem;
    box-shadow: 0 4px 10px rgba(0, 123, 255, 0.3);
  }

  /* Session Content */
  .content {
    flex: 1;
    text-align: left;
    padding: 15px;
  }

  .content h2 {
    font-size: 1.8rem;
    margin: 0;
    color: #333;
    font-weight: 600;
  }

  .speaker {
    font-style: italic;
    color: #555;
    font-weight: bold;
  }

  .description {
    color: #666;
    margin-top: 5px;
    line-height: 1.6;
  }

  /* Fade In Animation */
  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  /* Responsive Design */
  @media (max-width: 768px) {
    .session {
      flex-direction: column;
      text-align: center;
    }

    .timeline::before {
      left: 10px;
    }

    .session:nth-child(even) {
      flex-direction: column;
    }

    .time {
      min-width: auto;
      font-size: 1rem;
    }
  }
</style>
