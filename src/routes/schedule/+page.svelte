<link
    rel="stylesheet"
    href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css"
  />

<script>


  let sessions = [
    { title: "Opening Keynote", day: "Day 1", track: "Main Stage", time: "9:00 AM" },
    { title: "AI & The Future", day: "Day 1", track: "Tech Talks", time: "10:30 AM" },
    { title: "Web Development Trends", day: "Day 2", track: "Main Stage", time: "11:00 AM" },
    { title: "Cybersecurity Panel", day: "Day 2", track: "Security", time: "2:00 PM" },
    { title: "Networking Event", day: "Day 3", track: "Main Stage", time: "3:00 PM" }
  ];

  let activeFilter = "All"; // Default filter

  // Function to filter sessions
  function filterSessions(session) {
    return activeFilter === "All" || session.day === activeFilter || session.track === activeFilter;
  }



  let schedule = [
    {
      date: "March 15, 2025",
      time: "10:00 AM - 11:00 AM",
      topic: "The Future of AI",
      speaker: "John Doe (CEO, TechCorp)"
    },
    {
      date: "March 15, 2025",
      time: "11:30 AM - 12:30 PM",
      topic: "Cybersecurity in 2025",
      speaker: "Jane Smith (CTO, InnovateX)"
    },
    {
      date: "March 15, 2025",
      time: "2:00 PM - 3:00 PM",
      topic: "Blockchain Revolution",
      speaker: "Alice Brown (Lead Engineer, DevWorks)"
    },
    {
      date: "March 16, 2025",
      time: "10:00 AM - 11:00 AM",
      topic: "Cloud Computing Trends",
      speaker: "Michael Lee (Cloud Architect, CloudSync)"
    },
    {
      date: "March 16, 2025",
      time: "11:30 AM - 12:30 PM",
      topic: "The Role of AI in Healthcare",
      speaker: "Dr. Susan Green (AI Researcher, HealthTech)"
    }
  ];
</script>


<!-- Filter Buttons -->
<div class="filter-container">
  <div class="filter-scroll">
    {#each ["All", "Day 1", "Day 2", "Day 3", "Main Stage", "Tech Talks", "Security"] as filter}
      <button 
        class="{activeFilter === filter ? 'active' : ''}" 
        on:click={() => (activeFilter = filter)}
      >
        {filter}
      </button>
    {/each}
  </div>
</div>

<hr>

<!-- Sessions List -->
<div class="sessions-container">
  {#each sessions.filter(filterSessions) as session}
    <div class="session-card">
      <h3>{session.title}</h3>
      <p><strong>Day:</strong> {session.day}</p>
      <p><strong>Track:</strong> {session.track}</p>
      <p><strong>Time:</strong> {session.time}</p>
    </div>
  {/each}
</div>

<!-- Styles -->



<!-- 

<div class="filter-container p-4">
  <button 
    class="{activeFilter === 'All' ? 'active' : ''}" 
    on:click={() => (activeFilter = "All")}
  >All</button>
  
  <button 
    class="{activeFilter === 'Day 1' ? 'active' : ''}" 
    on:click={() => (activeFilter = "Day 1")}
  >Day 1</button>
  
  <button 
    class="{activeFilter === 'Day 2' ? 'active' : ''}" 
    on:click={() => (activeFilter = "Day 2")}
  >Day 2</button>
  
  <button 
    class="{activeFilter === 'Day 3' ? 'active' : ''}" 
    on:click={() => (activeFilter = "Day 3")}
  >Day 3</button>
  
  <button 
    class="{activeFilter === 'Main Stage' ? 'active' : ''}" 
    on:click={() => (activeFilter = "Main Stage")}
  >Main Stage</button>
  
  <button 
    class="{activeFilter === 'Tech Talks' ? 'active' : ''}" 
    on:click={() => (activeFilter = "Tech Talks")}
  >Tech Talks</button>
  
  <button 
    class="{activeFilter === 'Security' ? 'active' : ''}" 
    on:click={() => (activeFilter = "Security")}
  >Security</button>
</div>
<hr>
<div class="sessions-container">
  {#each sessions.filter(filterSessions) as session}
    <div class="session-card box">
      <h3>{session.title}</h3>
      <p><strong>Day:</strong> {session.day}</p>
      <p><strong>Track:</strong> {session.track}</p>
      <p><strong>Time:</strong> {session.time}</p>
    </div>
  {/each}
</div> -->

<!-- Page Header -->
<div class=" text-center my-4 headerText">
  <h1 class="mb-4">Conference Schedule</h1>
  <p>Stay up to date with our exciting lineup of sessions.</p>
</div>

<!-- Schedule Table -->
<div class="container">
  <div class="table-responsive">
    <table class="table table-bordered table-striped text-center">
      <thead class="table-dark">
        <tr>
          <th>Date</th>
          <th>Time</th>
          <th>Topic</th>
          <th>Speaker</th>
        </tr>
      </thead>
      <tbody>
        {#each schedule as session}
          <tr>
            <td>{session.date}</td>
            <td>{session.time}</td>
            <td>{session.topic}</td>
            <td>{session.speaker}</td>
          </tr>
        {/each}
      </tbody>
    </table>
  </div>
</div>
<br>
<br>
<br>
<br>
<br>
<br>
<style>
  table {
    margin-top: 20px;
    margin-bottom: 40px;
  }
  th, td {
    padding: 15px;
    text-align: center;
  }

  .filter-container {
  display: flex;
  gap: 10px;
  margin-bottom: 20px;
}

button {
  padding: 10px 15px;
  border: 1px solid #0d062e;
  cursor: pointer;
  /* background-color: #007bff; */
  color: rgb(0, 0, 0);
  border-radius: 5px;
  transition: 0.3s;
}

button:hover {
  background-color: #e8f857;
  /* color: white; */
}
  .active {
     background-color: #e8f857; 
    font-weight: bold;
  }

.sessions-container {
  display: flex;
  flex-direction: row;
  padding: 10px;
  gap: 15px;
}

.session-card {
  /* background: white; */
  padding: 15px;
  border-radius: 8px;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
}
 /* Filter Buttons - Scrollable for Mobile */
  .filter-container {
    overflow-x: auto;
    white-space: nowrap;
    padding: 10px;
    background: #f8f9fa;
  }

  .filter-scroll {
    display: flex;
    gap: 8px;
  }

  .filter-scroll button {
    padding: 10px 16px;
    border: none;
    background: #e0e0e0;
    cursor: pointer;
    font-size: 14px;
    border-radius: 5px;
    transition: background 0.3s;
  }

  .filter-scroll button.active {
    background: #e8f857;
    color: #0d062e;
    font-weight: bold;
  }

  /* Session Cards - Responsive */
  .sessions-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 15px;
    padding: 10px;
  }

  .session-card {
    padding: 15px;
    border-radius: 10px;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
    background: white;
    
   border: 1px solid #0d062e;
  }

  /* Mobile Adjustments */
  @media (max-width: 600px) {
    .filter-container {
      padding: 8px;
    }
    
    .filter-scroll button {
      padding: 8px 12px;
      font-size: 12px;
    }

    .session-card {
      padding: 12px;
      border: 1px solid #0d062e;
     box-shadow: 11px 13px 31px -7px rgba(0,0,0,0.75);
-webkit-box-shadow: 11px 13px 31px -7px rgba(0,0,0,0.75);
-moz-box-shadow: 11px 13px 31px -7px rgba(0,0,0,0.75);
/* background: #3c3d3e; */
    }
  }
</style>
