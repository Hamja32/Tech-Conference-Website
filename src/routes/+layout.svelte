<script>
  import Footer from "$lib/components/Footer.svelte";
  import Navbar from "$lib/components/Navbar.svelte";

  import "../app.css";
</script>


<!-- Navbar har page par show hoga -->
<Navbar />


<!-- Mount the Footer Here -->
<Footer />

<!-- Yeh slot ensure karega ki har page ka content dikhai de -->
<slot />
