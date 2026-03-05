<script>
  import { onMount } from 'svelte';

  let visible = $state(false);

  onMount(() => {
    setTimeout(() => visible = true, 80);
  });
</script>

<section class="relative min-h-screen flex flex-col items-center justify-center overflow-hidden"
  style="background: #08090c;">

  <!-- Ambient glow -->
  <div class="absolute inset-0 pointer-events-none"
    style="background: radial-gradient(ellipse 70% 50% at 50% 40%, rgba(0,102,255,0.10) 0%, transparent 70%);">
  </div>

  <!-- Welcome message -->
  <div class="relative z-10 flex flex-col items-center text-center px-6
    transition-all duration-700 ease-out
    {visible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-6'}">

    <!-- Wave + heading -->
    <div class="flex items-center gap-3 mb-4">
      <!-- Wave SVG -->
      <svg width="36" height="36" viewBox="0 0 36 36" fill="none" xmlns="http://www.w3.org/2000/svg"
        class="wave-hand" aria-hidden="true">
        <text y="28" font-size="28">👋</text>
      </svg>

      <h1 class="text-5xl font-black tracking-tight leading-none"
        style="color: #eef0f8; font-family: 'Syne', sans-serif; letter-spacing: -0.04em;">
        Welcome to <span style="color: #0066FF; filter: drop-shadow(0 0 18px rgba(0,102,255,0.5));">Nexus</span>
      </h1>
    </div>

    <p class="text-lg font-light max-w-md"
      style="color: #4b5263; line-height: 1.75;">
      The platform where your community finds its home.
    </p>
  </div>

  <!-- Scroll down indicator -->
  <div class="absolute bottom-10 flex flex-col items-center gap-2 z-10
    transition-all duration-700 delay-500
    {visible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-4'}">

    <!-- Thin vertical line that pulses downward -->
    <div class="scroll-line" style="width:1px; height:48px; background: linear-gradient(to bottom, transparent, #0066FF, transparent);">
    </div>

    <svg width="12" height="12" viewBox="0 0 12 12" fill="none" class="bounce-arrow">
      <path d="M1 4L6 9L11 4" stroke="#0066FF" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>
  </div>

</section>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Syne:wght@800&display=swap');

  @keyframes wave {
    0%   { transform: rotate(0deg); }
    15%  { transform: rotate(18deg); }
    30%  { transform: rotate(-10deg); }
    45%  { transform: rotate(16deg); }
    60%  { transform: rotate(-8deg); }
    75%  { transform: rotate(10deg); }
    100% { transform: rotate(0deg); }
  }

  @keyframes bounceDown {
    0%, 100% { transform: translateY(0); opacity: 0.5; }
    50%       { transform: translateY(6px); opacity: 1; }
  }

  @keyframes scrollPulse {
    0%   { opacity: 0; transform: scaleY(0); transform-origin: top; }
    50%  { opacity: 1; transform: scaleY(1); }
    100% { opacity: 0; transform: scaleY(0); transform-origin: bottom; }
  }

  .wave-hand {
    animation: wave 2s ease-in-out 0.8s 1;
    transform-origin: 70% 80%;
    display: inline-block;
  }

  .bounce-arrow {
    animation: bounceDown 1.6s ease-in-out infinite;
  }

  .scroll-line {
    animation: scrollPulse 1.8s ease-in-out infinite;
  }
</style>