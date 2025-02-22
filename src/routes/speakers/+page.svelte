<script>
 let speakers = [
    
  {
    name: "Jane Smith",
    title: "CTO, InnovateX",
    img: "/images/speaker1.jpg",
    bio: "Jane is a pioneer in blockchain technology and has contributed to multiple decentralized finance projects."
  },
  {
    name: "Michael Johnson",
    title: "Lead Developer, OpenWeb",
    img: "/images/speaker2.jpg",
    bio: "Michael specializes in open-source web technologies and has worked on projects that power millions of websites globally."
  },
  {
    name: "Emily Davis",
    title: "AI Researcher, DeepTech",
    img: "/images/speaker3.jpg",
    bio: "Emily's research focuses on machine learning fairness and AI ethics, ensuring responsible AI development and many more."
  },
  {
    name: "Sophia Miller",
    title: "Data Scientist, BigData Labs",
    img: "/images/speaker5.jpg",
    bio: "Sophia has a deep understanding of data analytics and has built AI-driven recommendation systems for top enterprises."
  },
  {
    name: "David Wilson",
    title: "Cloud Architect, SkyNet Solutions",
    img: "/images/speaker7.jpg",
    bio: "David is an expert in cloud computing, helping organizations transition to scalable and cost-effective cloud infrastructures."
  },
  {
    name: "Olivia Taylor",
    title: "UX Designer, Creative Minds",
    img: "/images/speaker8.jpg",
    bio: "Olivia creates intuitive and engaging digital marketing experiences, specializing in user-centered design strategies."
  },
  
    {
      name: "John Doe",
      title: "CEO, TechCorp",
      img: "/images/speaker6.jpg",
      bio: "John has been a leader in AI innovation for over a decade. He is passionate about building ethical AI solutions."
    },
    {
      name: "Jane Smith",
      title: "CTO, InnovateX",
      img: "/images/speaker2.jpg",
      bio: "Jane specializes in cybersecurity and cloud computing. She has worked with Fortune 500 companies to improve security protocols."
    },
    {
      name: "Alice Brown",
      title: "Lead Engineer, DevWorks",
      img: "/images/speaker3.jpg",
      bio: "Alice is a software architect known for her expertise in blockchain and decentralized applications with 400 companies help."
    },
  ]
  
</script>

<style>


  .speaker-card {
    margin-bottom: 20px;
    border-radius: 10px;
    overflow: hidden;
    transition: transform 0.2s ease-in-out;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
    background-color: #180f44;
    color:white ;
    padding: 25px;
    text-align: justify;
    line-height: 1.8;
  }

  .speaker-card:hover {
    transform: scale(1.05);
       filter: drop-shadow(0 0 0.25rem blue);
  }

  .speaker-card img {
    width: 100%;
    height: 250px;
    object-fit: cover;
    border-radius: 8px;
    border: 1px solid white;
  }

  .container {
    max-width: 1220px;
    margin: auto;
    padding: 30px 10px;
    margin-bottom: 60px;
  }

  h1 {
    text-align: center;
    margin-bottom: 20px;
  }

</style>

<!-- Page Header -->
<div class="headerText">
    <h1>Meet Our Speakers</h1>
  <p class="text-center">Learn from industry experts who are shaping the future of technology.</p>
</div>
<div class="container">

  <!-- Speaker Grid -->
  <div class="row">
    {#each speakers as speaker}
      <div class="col-md-4">
        <div class="card speaker-card">
          <img src="{speaker.img}" class="card-img-top" alt="{speaker.name}">
          <div class="card-body">
            <h5 class="card-title">{speaker.name}</h5>
            <p class="card-text badge"><strong>{speaker.title}</strong></p>
            <p class="card-text">{speaker.bio}</p>
          </div>
        </div>
      </div>
    {/each}
  </div>
</div>
