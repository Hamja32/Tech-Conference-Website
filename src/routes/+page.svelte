
<style>
    /* Hero Section Styles */
        .hero {
            min-height:50vh;
            /* min-width: 500px; */
            background: linear-gradient(rgb(67, 67, 68),rgba(228, 240, 96, 0.7));
            block-size: cover;
            background-position: center;
            color: white;
            padding: 110px 30px;
            text-align: center;
            /* height: 350px; */
        }
        .speaker-card {
          margin-bottom: 20px;
          border-radius: 10px;
          overflow: hidden;
          transition: transform 0.2s ease-in-out;
          background:#d2d1d1;
          border: 2px solid gray;
          /* filter:brightness(70%); */
        }
      
        .hero h1{
            font-size: 3.4rem;
        }
        .hero p{
            font-size: 1.4rem;
            padding-bottom: 10px;
            color: rgb(234, 224, 224);
        }
        .speaker-card:hover {
          transform: scale(1.05);
           /* filter:brightness(90%); */
        }
      
        .speaker-card img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }
        
        </style>




    <!-- Hero Section -->
    <section class="hero">
        <h1>Tech Conference 2025</h1>
        <p>The premier event for technology professionals and enthusiasts to explore innovations and connect.. 🚀</p>
        <a href="https" class="btn btn-primary goBtn btn-lg">Register Now</a>
    </section>

    <script>
    
      import CountdownTimer from "$lib/components/CountdownTimer.svelte";
    
    </script>
    <main>
      <CountdownTimer />
    </main>
    <!-- Featured Speakers -->
    <div class="container my-4 " style="margin-bottom: 50px;">
        <h2 class="text-center p-6">Featured Keynote Speakers</h2>
        <div class="row mt-4">
            <!-- Speaker 1 -->
            <div class="col-md-3">
                <div class="speaker-card">
                    <img src="/images/speaker5.jpg" class="card-img-top" alt="John Doe">
                    <div class="card-body text-center p-2">
                        <h5 class="card-title">John Doe</h5>
                        <p class="card-text">CEO, TechCorp</p>
                    </div>
                </div>
            </div>
            <!-- Speaker 2 -->
            <div class="col-md-3">
                <div class="speaker-card">
                    <img src="/images/speaker6.jpg" class="card-img-top" alt="Jane Smith">
                    <div class="card-body text-center p-2">
                        <h5 class="card-title">Jane Smith</h5>
                        <p class="card-text">CTO, InnovateX</p>
                    </div>
                </div>
            </div>
            <!-- Speaker 3 -->
            <div class="col-md-3">
                <div class="speaker-card">
                    <img src="/images/speaker1.jpg" class="card-img-top" alt="Alice Brown">
                    <div class="card-body text-center p-2">
                        <h5 class="card-title">John Brown</h5>
                        <p class="card-text">Lead Engineer</p>
                    </div>
                </div>
            </div>
            <!-- Speaker 4 -->
            <div class="col-md-3">
                <div class="speaker-card">
                    <img src="/images/speaker2.jpg" class="card-img-top" alt="Alice Brown">
                    <div class="card-body text-center p-2">
                        <h5 class="card-title">Alice Brown</h5>
                        <p class="card-text">Lead Engineer</p>
                    </div>
                </div>
            </div>
        </div>
    </div>


<br><br>
<br><br>
<br><br>
