<script>
  import { onMount } from 'svelte';

  let phase = 0;

  onMount(() => {
    setTimeout(() => { phase = 1; }, 100);
    setTimeout(() => { phase = 2; }, 2200);
  });
</script>

<section
  class="relative min-h-screen flex flex-col items-center justify-center overflow-hidden"
  style="background: #08090c;"
>

  <!-- bg glow -->
  <div
    class="absolute inset-0 pointer-events-none transition-opacity duration-1000"
    class:opacity-0={phase !== 2}
    class:opacity-100={phase === 2}
    style="background: radial-gradient(ellipse 65% 45% at 50% 38%, rgba(255,255,255,0.04) 0%, transparent 70%);"
  ></div>

  <!-- greeting -->
  <div
    class="absolute z-20 flex items-center gap-3 select-none transition-all duration-500 ease-out"
    class:greeting-hidden={phase !== 1}
    class:greeting-visible={phase === 1}
  >
    <svg width="36" height="36" viewBox="0 0 36 36" class="wave-hand" aria-hidden="true">
      <text y="28" font-size="28">👋</text>
    </svg>
    <span class="text-2xl font-semibold tracking-tight" style="color: #c9cdd6;">
      Welcome to Astroblox
    </span>
  </div>

  <!-- hero -->
  <div
    class="relative z-10 flex flex-col items-center text-center px-6 transition-all duration-700 ease-out"
    class:hero-hidden={phase !== 2}
    class:hero-visible={phase === 2}
  >

    <!-- badge -->
    <div class="badge flex items-center gap-2 px-3 py-1 rounded-full mb-8 text-xs font-medium tracking-wide">
      <span class="w-1.5 h-1.5 rounded-full" style="background: rgba(255,255,255,0.25);"></span>
      Community Platform
    </div>

    <!-- headline -->
    <h1
      class="font-black leading-none tracking-tighter mb-6"
      style="font-size: clamp(2.8rem, 7vw, 5.5rem); color: #eef0f8; letter-spacing: -0.04em; max-width: 820px;"
    >
      The platform where your<br/>
      <span style="color: #9ca3af;">community finds its home.</span>
    </h1>

    <!-- sub -->
    <p class="text-base font-light mb-10 max-w-md" style="color: #3d4452; line-height: 1.8;">
      Build, grow and manage your community in one place —
      no scattered tools, no noise.
    </p>

    <!-- ctas -->
    <div class="flex items-center gap-3 flex-wrap justify-center">
      <button class="cta-primary px-6 py-2.5 rounded-full text-sm font-semibold">
        Get started →
      </button>
      <button class="cta-ghost px-6 py-2.5 rounded-full text-sm font-medium">
        Learn more
      </button>
    </div>

  </div>

  <!-- scroll indicator -->
  <div
    class="absolute bottom-10 flex flex-col items-center gap-2 z-10 transition-all duration-700"
    class:opacity-0={phase !== 2}
    class:opacity-100={phase === 2}
  >
    <div class="scroll-line"></div>
    <svg width="12" height="12" viewBox="0 0 12 12" fill="none" class="bounce-arrow">
      <path d="M1 4L6 9L11 4" stroke="rgba(255,255,255,0.2)" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>
  </div>

</section>

<style>
  .badge {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.08);
    color: #5a6070;
  }
  .cta-primary {
    background: rgba(255,255,255,0.09);
    color: #d1d5db;
    border: 1px solid rgba(255,255,255,0.12);
    cursor: pointer;
    transition: all 0.2s;
  }
  .cta-primary:hover {
    background: rgba(255,255,255,0.14);
    border-color: rgba(255,255,255,0.18);
  }
  .cta-ghost {
    color: #3d4452;
    background: transparent;
    border: none;
    cursor: pointer;
    transition: color 0.2s;
  }
  .cta-ghost:hover {
    color: #6b7280;
  }
  .greeting-hidden { opacity: 0; transform: translateY(12px); }
  .greeting-visible { opacity: 1; transform: translateY(0); }
  .hero-hidden  { opacity: 0; transform: translateY(20px); pointer-events: none; }
  .hero-visible { opacity: 1; transform: translateY(0); pointer-events: auto; }
  .scroll-line {
    width: 1px;
    height: 44px;
    background: linear-gradient(to bottom, transparent, rgba(255,255,255,0.15), transparent);
    animation: scrollPulse 2s ease-in-out infinite;
  }
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
    0%, 100% { transform: translateY(0); opacity: 0.4; }
    50%       { transform: translateY(5px); opacity: 0.8; }
  }
  @keyframes scrollPulse {
    0%   { opacity: 0; transform: scaleY(0.2); }
    50%  { opacity: 1; transform: scaleY(1); }
    100% { opacity: 0; transform: scaleY(0.2); }
  }
  .wave-hand { animation: wave 2s ease-in-out 0.3s 1; transform-origin: 70% 80%; }
  .bounce-arrow { animation: bounceDown 1.8s ease-in-out infinite; }
</style>