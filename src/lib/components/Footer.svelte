<script>
  const currentYear = new Date().getFullYear();
</script>

<style>
  .footer {
    width: 100%;
    height: 60px;
    color: #0d062e;
    background: rgb(207, 204, 204);
    border-top: 2px solid #0d062e;
    padding: 20px 30px;
    text-align: center;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    gap: 10px;
    bottom: 0;
    top: 1;
    z-index: 10;
    left: 0;
    position: fixed;
  }

  @media (max-width: 768px) {
   .footer{
    height: 50px;
   }
    }
 



 
</style>

<footer class="footer">
    <p><strong>TechConf</strong> - Innovate. Connect. Inspire.</p>
    <p>Created by Hamza khan</p>
  <p>© {currentYear} TechConf. All Rights Reserved.</p>
</footer>
