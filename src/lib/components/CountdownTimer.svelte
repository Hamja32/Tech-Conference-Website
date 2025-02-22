<script>
  import { onMount } from "svelte";

  let eventDate = new Date("2025-02-24T00:00:00").getTime(); // Set your event date
  let days, hours, minutes, seconds;
  let timeLeft;

  function updateCountdown() {
    let now = new Date().getTime();
    timeLeft = eventDate - now;

    if (timeLeft > 0) {
      days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
      hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
      seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);
    } else {
      days = hours = minutes = seconds = 0;
    }
  }

  onMount(() => {
    updateCountdown();
    const interval = setInterval(updateCountdown, 1000);
    return () => clearInterval(interval);
  });
</script>

<div class="countdown-container">
  <h2>Countdown to Tech Conference 2025</h2>
  <div class="countdown">
    <div class="time-box"><span>{days}</span><p>Days</p></div>
    <div class="time-box"><span>{hours}</span><p>Hours</p></div>
    <div class="time-box"><span>{minutes}</span><p>Minutes</p></div>
    <div class="time-box"><span>{seconds}</span><p>Seconds</p></div>
  </div>
</div>

<style>
  .countdown-container {
    text-align: center;
    padding: 20px;
    background: linear-gradient(135deg, #384450, #e2e4e4);
    color: white;
    /* border-radius: 10px; */
    margin: 20px 0;
  }

  .countdown {
    display: flex;
    justify-content: center;
    gap: 20px;
    font-size: 20px;
  }

  .time-box {
    background: rgba(255, 255, 255, 0.2);
    padding: 10px;
    border-radius: 5px;
    min-width: 70px;
  }

  .time-box span {
    font-size: 28px;
    font-weight: bold;
  }

  @media (max-width: 600px) {
    .countdown {
      flex-direction: row;
      align-items: center;
    }
  }
</style>
