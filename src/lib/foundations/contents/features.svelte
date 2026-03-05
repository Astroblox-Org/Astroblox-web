<script>
  import { onMount } from 'svelte';

  let currentIndex = $state(0);
  let paused = $state(false);
  // @ts-ignore
  let intervalId;

  const features = [
    {
      title: 'Real-time Messaging',
      desc: 'Lightning fast messages across all your channels with zero lag.',
      icon: '💬',
      color: '#0066FF',
    },
    {
      title: 'Voice & Video Rooms',
      desc: 'Drop into a room instantly — no links, no scheduling.',
      icon: '🎙️',
      color: '#0088ff',
    },
    {
      title: 'Roles & Permissions',
      desc: 'Full control over who sees what in your community.',
      icon: '🛡️',
      color: '#0055cc',
    },
    {
      title: 'Organized Channels',
      desc: 'Categories, threads and pins keep every conversation in place.',
      icon: '🗂️',
      color: '#3385ff',
    },
  ];

  const next = () => { currentIndex = (currentIndex + 1) % features.length; };
  const prev = () => { currentIndex = (currentIndex - 1 + features.length) % features.length; };

  // @ts-ignore
  const goTo = (i) => { currentIndex = i; resetInterval(); };

  const resetInterval = () => {
    // @ts-ignore
    clearInterval(intervalId);
    if (!paused) startInterval();
  };

  const startInterval = () => {
    intervalId = setInterval(next, 3200);
  };

  onMount(() => {
    startInterval();
    // @ts-ignore
    return () => clearInterval(intervalId);
  });

  $effect(() => {
    // @ts-ignore
    if (paused) clearInterval(intervalId);
    else startInterval();
  });
</script>

<section class="relative flex flex-col items-center py-28 px-6 overflow-hidden"
  style="background: #08090c;">

  <!-- Ambient -->
  <div class="absolute inset-0 pointer-events-none"
    style="background: radial-gradient(ellipse 60% 40% at 50% 60%, rgba(0,102,255,0.07) 0%, transparent 70%);">
  </div>

  <!-- Cover text -->
  <div class="relative z-10 text-center mb-16">
    <p class="text-xs font-bold tracking-widest uppercase mb-3" style="color: #0066FF; letter-spacing: 0.15em;">
      What we offer
    </p>
    <h2 class="text-4xl font-black tracking-tight" style="color: #eef0f8; font-family: 'Syne', sans-serif; letter-spacing: -0.03em;">
      Everything in one place
    </h2>
  </div>

  <!-- Device frame -->
  <div
    class="relative z-10 w-full max-w-2xl"
    role="region"
    aria-label="Feature showcase"
    onmouseenter={() => paused = true}
    onmouseleave={() => paused = false}
  >
    <!-- Outer device shell -->
    <div class="relative rounded-2xl overflow-hidden"
      style="
        background: rgba(255,255,255,0.02);
        border: 1px solid rgba(0,102,255,0.2);
        box-shadow:
          0 0 0 1px rgba(255,255,255,0.04),
          0 30px 80px rgba(0,0,0,0.5),
          0 0 60px rgba(0,102,255,0.08),
          inset 0 1px 0 rgba(255,255,255,0.06);
        backdrop-filter: blur(2px);
      ">

      <!-- Device top bar -->
      <div class="flex items-center gap-2 px-5 py-3"
        style="background: rgba(255,255,255,0.03); border-bottom: 1px solid rgba(255,255,255,0.05);">
        <span class="w-2.5 h-2.5 rounded-full" style="background: rgba(255,255,255,0.1);"></span>
        <span class="w-2.5 h-2.5 rounded-full" style="background: rgba(255,255,255,0.1);"></span>
        <span class="w-2.5 h-2.5 rounded-full" style="background: rgba(0,102,255,0.4);"></span>
        <span class="ml-auto text-xs" style="color: rgba(255,255,255,0.15); font-family: monospace;">nexus.app</span>
      </div>

      <!-- Screen — see-through, features slide inside -->
      <div class="relative overflow-hidden" style="height: 320px; background: rgba(8,9,12,0.6);">

        <!-- Sliding track -->
        <div
          class="flex h-full transition-transform duration-500 ease-in-out"
          style="width: {features.length * 100}%; transform: translateX(-{(currentIndex / features.length) * 100}%);"
        >
          {#each features as feat}
            <div
              class="flex flex-col items-center justify-center gap-5 px-12 text-center"
              style="width: {100 / features.length}%;"
            >
              <!-- Icon bubble -->
              <div class="w-16 h-16 rounded-2xl flex items-center justify-center text-3xl"
                style="background: rgba(0,102,255,0.12); border: 1px solid rgba(0,102,255,0.2);
                       box-shadow: 0 0 30px rgba(0,102,255,0.12);">
                {feat.icon}
              </div>

              <div>
                <h3 class="text-xl font-bold mb-2" style="color: #eef0f8; font-family: 'Syne', sans-serif;">
                  {feat.title}
                </h3>
                <p class="text-sm font-light leading-relaxed" style="color: #4b5263; max-width: 320px;">
                  {feat.desc}
                </p>
              </div>
            </div>
          {/each}
        </div>

        <!-- Glassy edge fade left -->
        <div class="absolute top-0 left-0 h-full w-16 pointer-events-none"
          style="background: linear-gradient(to right, rgba(8,9,12,0.7), transparent);">
        </div>
        <!-- Glassy edge fade right -->
        <div class="absolute top-0 right-0 h-full w-16 pointer-events-none"
          style="background: linear-gradient(to left, rgba(8,9,12,0.7), transparent);">
        </div>

      </div>

      <!-- Device bottom bar — dots + arrows -->
      <div class="flex items-center justify-center gap-4 py-4"
        style="background: rgba(255,255,255,0.02); border-top: 1px solid rgba(255,255,255,0.05);">

        <!-- Prev -->
        <button onclick={() => { prev(); resetInterval(); }}
          class="w-7 h-7 rounded-full flex items-center justify-center transition-all duration-200 border-0 cursor-pointer"
          style="background: rgba(255,255,255,0.04); color: #4b5263;"
          aria-label="Previous feature"
          onmouseenter={(e) => e.currentTarget.style.background = 'rgba(0,102,255,0.15)'}
          onmouseleave={(e) => e.currentTarget.style.background = 'rgba(255,255,255,0.04)'}>
          <svg width="12" height="12" viewBox="0 0 12 12" fill="none">
            <path d="M8 2L4 6L8 10" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>

        <!-- Dot indicators -->
        <div class="flex items-center gap-2">
          {#each features as _, i}
            <button
              onclick={() => goTo(i)}
              aria-label="Go to feature {i + 1}"
              class="rounded-full transition-all duration-300 border-0 cursor-pointer p-0"
              style="
                width: {currentIndex === i ? '20px' : '6px'};
                height: 6px;
                background: {currentIndex === i ? '#0066FF' : 'rgba(255,255,255,0.12)'};
                box-shadow: {currentIndex === i ? '0 0 8px rgba(0,102,255,0.6)' : 'none'};
              "
            ></button>
          {/each}
        </div>

        <!-- Next -->
        <button onclick={() => { next(); resetInterval(); }}
          class="w-7 h-7 rounded-full flex items-center justify-center transition-all duration-200 border-0 cursor-pointer"
          style="background: rgba(255,255,255,0.04); color: #4b5263;"
          aria-label="Next feature"
          onmouseenter={(e) => e.currentTarget.style.background = 'rgba(0,102,255,0.15)'}
          onmouseleave={(e) => e.currentTarget.style.background = 'rgba(255,255,255,0.04)'}>
          <svg width="12" height="12" viewBox="0 0 12 12" fill="none">
            <path d="M4 2L8 6L4 10" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>

      </div>
    </div>

    <!-- Reflection glow under device -->
    <div class="absolute -bottom-8 left-1/2 -translate-x-1/2 w-3/4 h-8 pointer-events-none"
      style="background: rgba(0,102,255,0.12); filter: blur(20px); border-radius: 50%;">
    </div>

  </div>

</section>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Syne:wght@700;800&display=swap');
</style>