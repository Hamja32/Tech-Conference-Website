<script>
  let isOpen = false;
</script>

<style>
  .navbar {
    background: #0d062e;
    border-bottom: 1px solid white;
    padding: 23px;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky;
    top: 0;
    width: 100%;
    z-index: 1000;
    transition: 0.3s ease-in-out;
  }

  .logo {
    font-size: 1.5rem;
    font-weight: bold;
    color: white;
    text-decoration: none;
  }

  .nav-links {
    display: flex;
    gap: 20px;
    list-style: none;
  }

  .nav-links a {
    text-decoration: none;
    font-size: 1.2rem;
    transition: 0.3s ease-in-out;
color: white;
    /* padding-top: 40px;
    padding-right: 20px; */
  }

  .nav-links a:hover {
    color: #ffcc00;
  }

  .menu-toggle {
    display: none;
    font-size: 1.8rem;
    cursor: pointer;
    background: #5454ca;
    padding: 3px;
    border: none;
    width: 30px;
    border-radius: 4px;
    color: white;
  }

  @media (max-width: 768px) {
    .nav-links {
      display: none;
      flex-direction: column;
      background: #d9e3e8;
      position: absolute;
      top: 90px;
      left: 0;
      width: 100%;
      padding: 10px 0;
      text-align: center;
    }

    .nav-links.open {
      display: flex;
    }
    .nav-links a{
      
        color: #0d062e;
    }
    
    .menu-toggle {
      display: block;
      width: 18%;
      background: #000;
      border: 1px solid white;
      border-radius: 4px;
    }
  }
  
</style>

<!-- Navbar -->
<nav class="navbar">
  <a href="/" class="logo">TechConf</a>


<ul class="nav-links {isOpen ? 'open' : ''} mt-2">
  <li><a href="/">Home</a></li>
  <li><a href="/speakers">Speakers</a></li>
  <li><a href="/schedule">Schedule</a></li>
  <li><a href="/sponsors">Sponsors</a></li>
  <li><a href="/about">About</a></li>
  <li><a href="/contact">Contact</a></li>
</ul>

  <button class="menu-toggle" on:click={() => isOpen = !isOpen}>
    ☰
  </button>
</nav>
