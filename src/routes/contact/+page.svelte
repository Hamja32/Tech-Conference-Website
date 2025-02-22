  <script>
    import { onMount } from "svelte";

    let name = "";
    let email = "";
    let message = "";
    let successMessage = "";

    function handleSubmit(event) {
      event.preventDefault();
      if (name && email && message) {
        successMessage = "Your message has been sent successfully!";
        name = "";
        email = "";
        message = "";
      }
    }
  </script>

  <div class="contact-container mb-12 p-5">
    <div class="contact-form">
      <h2>Get in Touch</h2>
      <p>Have questions? We’d love to hear from you!</p>
      
      <form on:submit={handleSubmit}>
        <div class="form-group">
          <label for="name">Name</label>
          <input type="text" id="name" bind:value={name} required />
        </div>
        
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" bind:value={email} required />
        </div>

        <div class="form-group">
          <label for="message">Message</label>
          <textarea id="message" rows="4" bind:value={message} required></textarea>
        </div>

        <button type="submit">Send Message</button>
      </form>

      {#if successMessage}
        <p class="success-message">{successMessage}</p>
      {/if}
    </div>
    <div class="contact-info">
      <img src='images/follow-us.jpg' alt="Follow Us" class="follow-image" />
      <h2>Follow Us</h2>
      <p>Stay connected with us on social media.</p>
      <div class="Map">
        <iframe class="map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d28620.41305287243!2d72.95600053269885!3d26.27621155552181!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x39418e894b5bbdb9%3A0x408fd55f72866419!2sRajiv%20Gandhi%20Colony%2C%20Suthalagajanand%20Colony%2C%20Jodhpur%2C%20Rajasthan%20342003!5e0!3m2!1sen!2sin!4v1740194756202!5m2!1sen!2sin" width="390" height="150" style="border:1px solid gray;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe></div>
        <!-- <br><br> -->
        <div class="social-links">
          <a href="#" class="social-btn twitter">Twitter</a>
          <a href="#" class="social-btn youtube">YouTube</a>
          <a href="#" class="social-btn github">GitHub</a>
          <a href="#" class="social-btn linkedin">LinkedIn</a>
        </div>
      </div>
  </div>
<br>
<br>
<br>
  <style>
    .contact-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      /* align-items: center; */
      gap: 30px;
      padding: 60px;
      background: #eaa6a6;
      border-radius: 10px;
      /* height: 890px; */
      /* max-height: 1200px; */
    }

    .contact-form, .contact-info {
      flex: 1;  
      max-width: 500px;
      background: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
      text-align: center;
    }

    .form-group {
      margin-bottom: 15px;
      text-align: left;
    }

    input, textarea {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    button {
      width: 100%;
      padding: 12px;
      background: #007bff;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
    }

    button:hover {
      background: #0056b3;
    }

    .follow-image {
      width: 70%;
      max-width: 280px;
      margin-bottom: 20px;
    }

    .social-links {
      margin-top: 20px;
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      justify-content: center;
    }

    .social-btn {
      text-decoration: none;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 10px;
      width: 100px;
      color: white;
      border-radius: 5px;
      font-weight: bold;
      text-align: center;
    }

    .twitter { background: #1DA1F2; }
    .youtube { background: #FF0000; }
    .github { background: #333; }
    .linkedin { background: #0077B5; }

    @media (max-width: 768px) {
      .contact-container {
        flex-direction: column;
        align-items: center;
        padding: 20px;
      }

      .contact-form, .contact-info {
        width: 90%;
        max-width: 400px;
      }
      .map{
        width: 200px;
      }
    }

  
  </style>
