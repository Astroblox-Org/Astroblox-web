<script>
  const features = [
    {
      title: 'Real-time Messaging',
      desc: 'Lightning fast messages across all your channels with zero lag.',
    },
    {
      title: 'Voice & Video Rooms',
      desc: 'Drop into a room instantly — no links, no scheduling needed.',
    },
    {
      title: 'Roles & Permissions',
      desc: 'Full control over who sees what inside your community.',
    },
    {
      title: 'Organized Channels',
      desc: 'Categories, threads and pins keep every conversation in place.',
    },
    {
      title: 'Notifications',
      desc: 'Stay in the loop with smart alerts that never overwhelm you.',
    },
    {
      title: 'Member Insights',
      desc: 'Understand your community with activity trends and engagement data.',
    },
  ];
</script>

<section class="relative py-28 px-12 overflow-hidden" style="background: #08090c;">

  <!-- bg glow -->
  <div class="absolute inset-0 pointer-events-none"
    style="background: radial-gradient(ellipse 60% 40% at 50% 60%, rgba(0,102,255,0.07) 0%, transparent 70%);">
  </div>

  <!-- heading -->
  <div class="relative z-10 mb-16 max-w-5xl mx-auto">
    <p class="text-xs font-bold tracking-widest uppercase mb-3" style="color: #3a5080; letter-spacing: 0.15em;">
      Platform features
    </p>
    <div class="flex items-end justify-between">
      <h2 class="text-4xl font-black tracking-tight" style="color: #eef0f8; letter-spacing: -0.03em; max-width: 480px;">
        Take control of your <span style="color: #6ea8fe;">community</span>
      </h2>
      <div class="flex items-center gap-3 mb-2">
        <div style="width: 120px; height: 1px; background: repeating-linear-gradient(90deg, rgba(255,255,255,0.1) 0px, rgba(255,255,255,0.1) 4px, transparent 4px, transparent 12px);"></div>
        <div class="w-4 h-4 rounded-full flex items-center justify-center" style="border: 1.5px solid rgba(0,102,255,0.5);">
          <div class="w-1.5 h-1.5 rounded-full" style="background: #0066FF;"></div>
        </div>
      </div>
    </div>
    <p class="text-sm font-light mt-3" style="color: #4b5263; line-height: 1.8; max-width: 480px;">
      Everything your community needs to chat, connect and grow — all in one place.
    </p>
  </div>

  <!-- grid -->
  <div class="relative z-10 max-w-5xl mx-auto grid grid-cols-3 gap-6">
    {#each features as feat (feat.title)}
      <div class="feature-card flex flex-col gap-3 p-5 rounded-xl">

        <div class="w-9 h-9 rounded-lg flex items-center justify-center shrink-0"
          style="background: rgba(0,102,255,0.1); border: 1px solid rgba(0,102,255,0.2);">
          {#if feat.title === 'Real-time Messaging'}
            <svg width="18" height="18" viewBox="0 0 20 20" fill="none">
              <path d="M2 5a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H6l-4 3V5z" stroke="#6ea8fe" stroke-width="1.5" stroke-linejoin="round"/>
              <path d="M6 8h8M6 11h5" stroke="#6ea8fe" stroke-width="1.5" stroke-linecap="round"/>
            </svg>
          {:else if feat.title === 'Voice & Video Rooms'}
            <svg width="18" height="18" viewBox="0 0 20 20" fill="none">
              <rect x="2" y="5" width="11" height="10" rx="2" stroke="#6ea8fe" stroke-width="1.5"/>
              <path d="M13 8l5-3v9l-5-3V8z" stroke="#6ea8fe" stroke-width="1.5" stroke-linejoin="round"/>
            </svg>
          {:else if feat.title === 'Roles & Permissions'}
            <svg width="18" height="18" viewBox="0 0 20 20" fill="none">
              <path d="M10 2l2.5 5 5.5.8-4 3.9.9 5.5L10 14.5l-4.9 2.7.9-5.5L2 7.8l5.5-.8L10 2z" stroke="#6ea8fe" stroke-width="1.5" stroke-linejoin="round"/>
            </svg>
          {:else if feat.title === 'Organized Channels'}
            <svg width="18" height="18" viewBox="0 0 20 20" fill="none">
              <path d="M3 5h14M3 10h14M3 15h8" stroke="#6ea8fe" stroke-width="1.5" stroke-linecap="round"/>
              <circle cx="16" cy="15" r="2.5" stroke="#6ea8fe" stroke-width="1.5"/>
            </svg>
          {:else if feat.title === 'Notifications'}
            <svg width="18" height="18" viewBox="0 0 20 20" fill="none">
              <path d="M10 2a6 6 0 0 0-6 6v3l-1.5 2.5h15L16 11V8a6 6 0 0 0-6-6z" stroke="#6ea8fe" stroke-width="1.5" stroke-linejoin="round"/>
              <path d="M8.5 16.5a1.5 1.5 0 0 0 3 0" stroke="#6ea8fe" stroke-width="1.5" stroke-linecap="round"/>
            </svg>
          {:else}
            <svg width="18" height="18" viewBox="0 0 20 20" fill="none">
              <path d="M3 15l4-5 3 3 3-6 4 8" stroke="#6ea8fe" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
          {/if}
        </div>

        <div>
          <h3 class="text-sm font-bold mb-1" style="color: #d1d5db;">{feat.title}</h3>
          <p class="text-xs font-light leading-relaxed" style="color: #4b5263;">{feat.desc}</p>
        </div>

      </div>
    {/each}
  </div>

</section>

<style>
  .feature-card {
    background: rgba(255,255,255,0.02);
    border: 1px solid rgba(255,255,255,0.06);
    transition: all 0.2s;
  }
  .feature-card:hover {
    background: rgba(0,102,255,0.05);
    border-color: rgba(0,102,255,0.2);
    transform: translateY(-2px);
  }
</style>