/* eslint-disable @typescript-eslint/no-unused-vars */
<script>
  import { onMount } from 'svelte';

  // eslint-disable-next-line @typescript-eslint/ban-ts-comment
  // @ts-expect-error
  let currentIndex = 0;
  let paused = false;
  // eslint-disable-next-line @typescript-eslint/ban-ts-comment
  // @ts-expect-error
  /**
     * @type {string | number | NodeJS.Timeout | undefined}
     */
  let intervalId;

  const features = [
    { title: 'Real-time Messaging', desc: 'Lightning fast messages across all your channels with zero lag.', icon: '💬' },
    { title: 'Voice & Video Rooms', desc: 'Drop into a room instantly — no links, no scheduling.', icon: '🎙️' },
    { title: 'Roles & Permissions', desc: 'Full control over who sees what in your community.', icon: '🛡️' },
    { title: 'Organized Channels', desc: 'Categories, threads and pins keep every conversation in place.', icon: '🗂️' },
  ];

  const next = () => { currentIndex = (currentIndex + 1) % features.length; };
  const prev = () => { currentIndex = (currentIndex - 1 + features.length) % features.length; };
  const goTo = (/** @type {number} */ i) => { currentIndex = i; resetInterval(); };

  const resetInterval = () => {
    clearInterval(intervalId);
    if (!paused) startInterval();
  };

  const startInterval = () => { intervalId = setInterval(next, 3200); };

  onMount(() => {
    startInterval();
    return () => clearInterval(intervalId);
  });

  const handleMouseEnter = () => { paused = true; clearInterval(intervalId); };
  const handleMouseLeave = () => { paused = false; startInterval(); };
</script>

<section class="relative flex flex-col items-center py-28 px-6 overflow-hidden"
  style="background: #08090c;">

  <div class="absolute inset-0 pointer-events-none"
    style="background: radial-gradient(ellipse 60% 40% at 50% 60%, rgba(255,255,255,0.02) 0%, transparent 70%);">
  </div>

  <!-- heading -->
  <div class="relative z-10 text-center mb-16">
    <p class="text-xs font-bold tracking-widest uppercase mb-3" style="color: #4b5263; letter-spacing: 0.15em;">
      What we offer
    </p>
    <h2 class="text-4xl font-black tracking-tight" style="color: #eef0f8; letter-spacing: -0.03em;">
      Everything in one place
    </h2>
  </div>

  <!-- device frame -->
  <div
    class="relative z-10 w-full max-w-2xl"
    role="region"
    aria-label="Feature showcase"
    on:mouseenter={handleMouseEnter}
    on:mouseleave={handleMouseLeave}
  >
    <div class="relative rounded-2xl overflow-hidden"
      style="background: rgba(255,255,255,0.02); border: 1px solid rgba(255,255,255,0.07); box-shadow: 0 0 0 1px rgba(255,255,255,0.03), 0 30px 80px rgba(0,0,0,0.5), inset 0 1px 0 rgba(255,255,255,0.04);">

      <!-- top bar -->
      <div class="flex items-center gap-2 px-5 py-3"
        style="background: rgba(255,255,255,0.03); border-bottom: 1px solid rgba(255,255,255,0.05);">
        <span class="w-2.5 h-2.5 rounded-full" style="background: rgba(255,255,255,0.08);"></span>
        <span class="w-2.5 h-2.5 rounded-full" style="background: rgba(255,255,255,0.08);"></span>
        <span class="w-2.5 h-2.5 rounded-full" style="background: rgba(255,255,255,0.15);"></span>
        <span class="ml-auto text-xs" style="color: rgba(255,255,255,0.12); font-family: monospace;">astroblox.app</span>
      </div>

      <!-- screen -->
      <div class="relative overflow-hidden" style="height: 320px; background: rgba(8,9,12,0.6);">
        <div
          class="flex h-full transition-transform duration-500 ease-in-out"
          style="width: {features.length * 100}%; transform: translateX(-{(currentIndex / features.length) * 100}%);">
          {#each features as feat (feat.title)}
            <div class="flex flex-col items-center justify-center gap-5 px-12 text-center"
              style="width: {100 / features.length}%;">
              <div class="w-16 h-16 rounded-2xl flex items-center justify-center text-3xl"
                style="background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.08);">
                {feat.icon}
              </div>
              <div>
                <h3 class="text-xl font-bold mb-2" style="color: #eef0f8;">{feat.title}</h3>
                <p class="text-sm font-light leading-relaxed" style="color: #4b5263; max-width: 320px;">{feat.desc}</p>
              </div>
            </div>
          {/each}
        </div>
        <div class="absolute top-0 left-0 h-full w-16 pointer-events-none"
          style="background: linear-gradient(to right, rgba(8,9,12,0.7), transparent);"></div>
        <div class="absolute top-0 right-0 h-full w-16 pointer-events-none"
          style="background: linear-gradient(to left, rgba(8,9,12,0.7), transparent);"></div>
      </div>

      <!-- bottom bar -->
      <div class="flex items-center justify-center gap-4 py-4"
        style="background: rgba(255,255,255,0.02); border-top: 1px solid rgba(255,255,255,0.05);">
        <button
          on:click={() => { prev(); resetInterval(); }}
          class="nav-btn w-7 h-7 rounded-full flex items-center justify-center transition-all duration-200 border-0 cursor-pointer"
          aria-label="Previous feature">
          <svg width="12" height="12" viewBox="0 0 12 12" fill="none">
            <path d="M8 2L4 6L8 10" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>

        <div class="flex items-center gap-2">
          // eslint-disable-next-line @typescript-eslint/no-unused-vars
          {#each features as _, i (i)}
            <button
              on:click={() => goTo(i)}
              aria-label="Go to feature {i + 1}"
              class="rounded-full transition-all duration-300 border-0 cursor-pointer p-0 dot-btn"
              class:dot-active={currentIndex === i}
              style="width: {currentIndex === i ? '20px' : '6px'}; height: 6px;">
            </button>
          {/each}
        </div>

        <button
          on:click={() => { next(); resetInterval(); }}
          class="nav-btn w-7 h-7 rounded-full flex items-center justify-center transition-all duration-200 border-0 cursor-pointer"
          aria-label="Next feature">
          <svg width="12" height="12" viewBox="0 0 12 12" fill="none">
            <path d="M4 2L8 6L4 10" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>
      </div>
    </div>

    <div class="absolute -bottom-8 left-1/2 -translate-x-1/2 w-3/4 h-8 pointer-events-none"
      style="background: rgba(255,255,255,0.04); filter: blur(20px); border-radius: 50%;"></div>
  </div>

</section>

<style>
  .nav-btn {
    background: rgba(255,255,255,0.04);
    color: #4b5263;
  }
  .nav-btn:hover {
    background: rgba(255,255,255,0.09);
  }
  .dot-btn {
    background: rgba(255,255,255,0.12);
  }
  .dot-active {
    background: rgba(255,255,255,0.5) !important;
  }
</style>