<footer class="relative w-full overflow-hidden"
  style="background: #08090c; border-top: 1px solid rgba(255,255,255,0.05);">

  <div class="absolute bottom-0 left-0 pointer-events-none"
    style="width:400px;height:200px;background: radial-gradient(ellipse at 0% 100%, rgba(0,102,255,0.07) 0%, transparent 70%);">
  </div>

  <div class="relative z-10 max-w-6xl mx-auto px-12 pt-16 pb-0 flex items-end justify-between gap-12">

    <!-- LEFT -->
    <div class="flex flex-col gap-8 pb-10">

      <!-- Logo -->
      <div class="flex items-center gap-2">
        <div class="w-7 h-7 rounded-lg flex items-center justify-center shrink-0"
          style="background: #0066FF; box-shadow: 0 0 14px rgba(0,102,255,0.4);">
          <span class="text-white font-black text-xs">A</span>
        </div>
        <span class="font-bold text-sm tracking-tight" style="color: #eef0f8;">Astroblox</span>
      </div>

      <!-- Nav links -->
      <nav class="flex flex-wrap gap-x-8 gap-y-2">
        {#each ['Home', 'Features', 'Community', 'Pricing', 'Docs'] as link}
          <a href="/" class="text-sm no-underline transition-colors duration-200" style="color: #4b5263;"
            onmouseenter={(e) => e.currentTarget.style.color='#0066FF'}
            onmouseleave={(e) => e.currentTarget.style.color='#4b5263'}>{link}</a>
        {/each}
      </nav>

      <!-- Social icons -->
      <div class="flex items-center gap-3">
        <!-- X -->
        <a href="/" aria-label="X"
          class="w-8 h-8 rounded-lg flex items-center justify-center transition-all duration-200 no-underline"
          style="background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.07);"
          onmouseenter={(e) => { e.currentTarget.style.borderColor='rgba(0,102,255,0.4)'; e.currentTarget.style.background='rgba(0,102,255,0.1)'; }}
          onmouseleave={(e) => { e.currentTarget.style.borderColor='rgba(255,255,255,0.07)'; e.currentTarget.style.background='rgba(255,255,255,0.04)'; }}>
          <svg width="14" height="14" viewBox="0 0 24 24" fill="#4b5263">
            <path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-4.714-6.231-5.401 6.231H2.746l7.73-8.835L1.254 2.25H8.08l4.253 5.622 5.911-5.622zm-1.161 17.52h1.833L7.084 4.126H5.117z"/>
          </svg>
        </a>
        <!-- Discord -->
        <a href="/" aria-label="Discord"
          class="w-8 h-8 rounded-lg flex items-center justify-center transition-all duration-200 no-underline"
          style="background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.07);"
          onmouseenter={(e) => { e.currentTarget.style.borderColor='rgba(0,102,255,0.4)'; e.currentTarget.style.background='rgba(0,102,255,0.1)'; }}
          onmouseleave={(e) => { e.currentTarget.style.borderColor='rgba(255,255,255,0.07)'; e.currentTarget.style.background='rgba(255,255,255,0.04)'; }}>
          <svg width="14" height="14" viewBox="0 0 24 24" fill="#4b5263">
            <path d="M20.317 4.37a19.791 19.791 0 0 0-4.885-1.515.074.074 0 0 0-.079.037c-.21.375-.444.864-.608 1.25a18.27 18.27 0 0 0-5.487 0 12.64 12.64 0 0 0-.617-1.25.077.077 0 0 0-.079-.037A19.736 19.736 0 0 0 3.677 4.37a.07.07 0 0 0-.032.027C.533 9.046-.32 13.58.099 18.057c.002.022.015.04.033.05a19.89 19.89 0 0 0 5.993 3.03.078.078 0 0 0 .084-.028 14.09 14.09 0 0 0 1.226-1.994.076.076 0 0 0-.041-.106 13.107 13.107 0 0 1-1.872-.892.077.077 0 0 1-.008-.128 10.2 10.2 0 0 0 .372-.292.074.074 0 0 1 .077-.01c3.928 1.793 8.18 1.793 12.062 0a.074.074 0 0 1 .078.01c.12.098.246.198.373.292a.077.077 0 0 1-.006.127 12.299 12.299 0 0 1-1.873.892.077.077 0 0 0-.041.107c.36.698.772 1.362 1.225 1.993a.076.076 0 0 0 .084.028 19.839 19.839 0 0 0 6.002-3.03.077.077 0 0 0 .032-.054c.5-5.177-.838-9.674-3.549-13.66a.061.061 0 0 0-.031-.03z"/>
          </svg>
        </a>
        <!-- GitHub -->
        <a href="/" aria-label="GitHub"
          class="w-8 h-8 rounded-lg flex items-center justify-center transition-all duration-200 no-underline"
          style="background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.07);"
          onmouseenter={(e) => { e.currentTarget.style.borderColor='rgba(0,102,255,0.4)'; e.currentTarget.style.background='rgba(0,102,255,0.1)'; }}
          onmouseleave={(e) => { e.currentTarget.style.borderColor='rgba(255,255,255,0.07)'; e.currentTarget.style.background='rgba(255,255,255,0.04)'; }}>
          <svg width="14" height="14" viewBox="0 0 24 24" fill="#4b5263">
            <path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0 1 12 6.844a9.59 9.59 0 0 1 2.504.337c1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.02 10.02 0 0 0 22 12.017C22 6.484 17.522 2 12 2z"/>
          </svg>
        </a>
      </div>

      <!-- Copyright -->
      <p class="text-xs" style="color: #2a2d35;">
        © {new Date().getFullYear()} Astroblox. All rights reserved.
      </p>
    </div>

    <!-- RIGHT — sitting figure -->
    <div class="shrink-0 flex flex-col items-center select-none" aria-hidden="true" style="margin-bottom: -2px;">

      <!-- HEAD -->
      <div class="w-12 h-12 rounded-full flex items-center justify-center"
        style="background: rgba(0,102,255,0.08); border: 2px solid rgba(0,102,255,0.3); box-shadow: 0 0 20px rgba(0,102,255,0.18);">
        <div class="flex gap-2 mb-0.5">
          <div class="w-1.5 h-1.5 rounded-full" style="background: #0066FF;"></div>
          <div class="w-1.5 h-1.5 rounded-full" style="background: #0066FF;"></div>
        </div>
      </div>

      <!-- NECK -->
      <div class="w-3 h-2.5" style="background: rgba(0,102,255,0.12);"></div>

      <!-- TORSO + ARMS -->
      <div class="flex items-start">
        <!-- LEFT ARM -->
        <div class="flex flex-col items-end mt-1">
          <div class="w-2.5 h-9 rounded-full"
            style="background: rgba(0,102,255,0.15); border: 1px solid rgba(0,102,255,0.22); transform: rotate(6deg); transform-origin: top center;"></div>
          <div class="w-2 h-7 rounded-full -mt-1"
            style="background: rgba(0,102,255,0.12); border: 1px solid rgba(0,102,255,0.18); transform: rotate(10deg); transform-origin: top center;"></div>
          <div class="w-3 h-2.5 rounded-full -mt-1"
            style="background: rgba(0,102,255,0.22); border: 1px solid rgba(0,102,255,0.35);"></div>
        </div>

        <!-- TORSO -->
        <div class="flex flex-col items-center mx-1">
          <div class="w-14 h-16 rounded-xl"
            style="background: rgba(0,102,255,0.09); border: 1px solid rgba(0,102,255,0.2);">
            <div class="w-px h-10 mx-auto mt-2" style="background: rgba(0,102,255,0.18);"></div>
          </div>
          <div class="w-14 h-4 rounded-b-md -mt-1"
            style="background: rgba(0,102,255,0.12); border: 1px solid rgba(0,102,255,0.18); border-top:none;"></div>
        </div>

        <!-- RIGHT ARM -->
        <div class="flex flex-col items-start mt-1">
          <div class="w-2.5 h-9 rounded-full"
            style="background: rgba(0,102,255,0.15); border: 1px solid rgba(0,102,255,0.22); transform: rotate(-6deg); transform-origin: top center;"></div>
          <div class="w-2 h-7 rounded-full -mt-1"
            style="background: rgba(0,102,255,0.12); border: 1px solid rgba(0,102,255,0.18); transform: rotate(-10deg); transform-origin: top center;"></div>
          <div class="w-3 h-2.5 rounded-full -mt-1"
            style="background: rgba(0,102,255,0.22); border: 1px solid rgba(0,102,255,0.35);"></div>
        </div>
      </div>

      <!-- LEGS hanging (sitting) -->
      <div class="flex gap-3 -mt-1">
        <div class="flex flex-col items-center">
          <div class="w-14 h-4 rounded-l-lg"
            style="background: rgba(0,102,255,0.13); border: 1px solid rgba(0,102,255,0.2);"></div>
          <div class="w-4 h-14 rounded-b-lg ml-5"
            style="background: rgba(0,102,255,0.11); border: 1px solid rgba(0,102,255,0.18); border-top: none;"></div>
          <div class="w-6 h-3 rounded-sm ml-4"
            style="background: rgba(0,102,255,0.2); border: 1px solid rgba(0,102,255,0.3);"></div>
        </div>
        <div class="flex flex-col items-center">
          <div class="w-14 h-4 rounded-r-lg"
            style="background: rgba(0,102,255,0.13); border: 1px solid rgba(0,102,255,0.2);"></div>
          <div class="w-4 h-14 rounded-b-lg mr-5"
            style="background: rgba(0,102,255,0.11); border: 1px solid rgba(0,102,255,0.18); border-top: none;"></div>
          <div class="w-6 h-3 rounded-sm mr-4"
            style="background: rgba(0,102,255,0.2); border: 1px solid rgba(0,102,255,0.3);"></div>
        </div>
      </div>

    </div>
  </div>

  <div class="w-full h-px" style="background: linear-gradient(90deg, transparent, rgba(0,102,255,0.2), transparent);"></div>

</footer>