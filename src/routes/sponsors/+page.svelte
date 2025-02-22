
<script>
  let sponsors = [
    {
      name: "TechCorp",
      logo: "/images/tech.jpg",
      link: "https://www.techcorp.com"
    },
    {
      name: "InnovateX",
      logo: "/images/dev.jpg",
      link: "https://www.innovatex.com"
    },
    {
      name: "CloudSync",
      logo: "/images/innovative.jpg",
      link: "https://www.cloudsync.com"
    },
    {
      name: "DevWorks",
      logo: "/images/cloud.jpg",
      link: "https://www.devworks.com"
    }
  ];
</script>
<div class="sponsors">
  
<!-- Page Header -->
<div class=" text-center my-5 headerText">
  <h1 class="mb-4">Our Sponsors</h1>
  <p>We are grateful for the support of our incredible sponsors.</p>
</div>

<!-- Sponsors Grid -->
<div class="container">
  <div class="row justify-content-center">
    {#each sponsors as sponsor}
      <div class="col-md-3 col-sm-6 mb-4">
        <a href="{sponsor.link}" target="_blank" class="sponsor-card">
          <img src="{sponsor.logo}" alt="{sponsor.name}" class="img-fluid">
        </a>
      </div>
    {/each}
  </div>
</div>

</div>
<style>
  .sponsor-card {
    display: block;
    padding: 15px;
    background: #f8f9fa;
    border-radius: 10px;
    text-align: center;
    transition: transform 0.2s ease-in-out;
  }

  .sponsor-card:hover {
    transform: scale(1.1);
    
  }

  .sponsor-card img {
    max-width: 100%;
    height: 200px;
    border: 2px solid rgb(106, 14, 218);
    border-radius: 5px;
    object-fit: cover;
  }
</style>
