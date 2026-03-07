<section class="relative flex items-center justify-center min-h-screen overflow-hidden px-12"
  style="background: #08090c;">

  <!-- bg glow -->
  <div class="absolute inset-0 pointer-events-none"
    style="background: radial-gradient(ellipse 60% 50% at 50% 50%, rgba(0,102,255,0.08) 0%, transparent 65%);">
  </div>

  <!-- corner lines top-left -->
  <svg class="absolute top-0 left-0 pointer-events-none" width="220" height="220" fill="none">
    <path d="M 60 0 L 60 60 L 0 60" stroke="rgba(255,255,255,0.06)" stroke-width="1" stroke-dasharray="4 8"/>
    <circle cx="60" cy="60" r="4" fill="none" stroke="rgba(0,102,255,0.4)" stroke-width="1.5"/>
    <circle cx="60" cy="60" r="2" fill="rgba(0,102,255,0.5)"/>
    <circle cx="200" cy="30" r="2" fill="none" stroke="rgba(0,102,255,0.25)" stroke-width="1"/>
    <circle cx="30" cy="180" r="1.5" fill="rgba(255,255,255,0.08)"/>
  </svg>

  <!-- corner lines top-right -->
  <svg class="absolute top-0 right-0 pointer-events-none" width="220" height="220" fill="none">
    <path d="M 160 0 L 160 60 L 220 60" stroke="rgba(255,255,255,0.06)" stroke-width="1" stroke-dasharray="4 8"/>
    <circle cx="160" cy="60" r="4" fill="none" stroke="rgba(0,102,255,0.4)" stroke-width="1.5"/>
    <circle cx="160" cy="60" r="2" fill="rgba(0,102,255,0.5)"/>
    <circle cx="30" cy="30" r="2" fill="none" stroke="rgba(0,102,255,0.2)" stroke-width="1"/>
  </svg>

  <!-- corner lines bottom-left -->
  <svg class="absolute bottom-0 left-0 pointer-events-none" width="220" height="220" fill="none">
    <path d="M 60 220 L 60 160 L 0 160" stroke="rgba(255,255,255,0.06)" stroke-width="1" stroke-dasharray="4 8"/>
    <circle cx="60" cy="160" r="4" fill="none" stroke="rgba(0,102,255,0.3)" stroke-width="1.5"/>
    <circle cx="60" cy="160" r="2" fill="rgba(0,102,255,0.4)"/>
  </svg>

  <!-- corner lines bottom-right -->
  <svg class="absolute bottom-0 right-0 pointer-events-none" width="220" height="220" fill="none">
    <path d="M 160 220 L 160 160 L 220 160" stroke="rgba(255,255,255,0.06)" stroke-width="1" stroke-dasharray="4 8"/>
    <circle cx="160" cy="160" r="4" fill="none" stroke="rgba(0,102,255,0.3)" stroke-width="1.5"/>
    <circle cx="160" cy="160" r="2" fill="rgba(0,102,255,0.4)"/>
  </svg>

  <!-- scattered dots -->
  <svg class="absolute inset-0 w-full h-full pointer-events-none" fill="none">
    <circle cx="18%" cy="35%" r="1.5" fill="rgba(0,102,255,0.3)"/>
    <circle cx="82%" cy="65%" r="1.5" fill="rgba(0,102,255,0.3)"/>
    <circle cx="25%" cy="72%" r="1" fill="rgba(255,255,255,0.08)"/>
    <circle cx="75%" cy="28%" r="1" fill="rgba(255,255,255,0.08)"/>
    <circle cx="12%" cy="55%" r="1" fill="rgba(255,255,255,0.05)"/>
    <circle cx="88%" cy="45%" r="1" fill="rgba(255,255,255,0.05)"/>
  </svg>

  <div class="relative z-10 flex items-center justify-between w-full max-w-5xl gap-16">

    <!-- figure -->
    <div class="shrink-0 flex flex-col items-center select-none" aria-hidden="true">
      <div class="relative flex flex-col items-center">

        <!-- head -->
        <div class="w-14 h-14 rounded-full flex items-center justify-center"
          style="background: rgba(0,102,255,0.08); border: 2px solid rgba(0,102,255,0.3); box-shadow: 0 0 20px rgba(0,102,255,0.15);">
          <div class="flex gap-2.5 mb-1">
            <div class="w-1.5 h-1.5 rounded-full" style="background: #0066FF;"></div>
            <div class="w-1.5 h-1.5 rounded-full" style="background: #0066FF;"></div>
          </div>
        </div>

        <!-- neck -->
        <div class="w-3 h-3" style="background: rgba(0,102,255,0.12);"></div>

        <!-- torso + arms -->
        <div class="flex items-start">

          <!-- left arm -->
          <div class="flex flex-col items-end mt-1">
            <div class="w-3 h-10 rounded-full" style="background: rgba(0,102,255,0.15); border: 1px solid rgba(0,102,255,0.25); transform: rotate(-8deg); transform-origin: top center;"></div>
            <div class="w-2.5 h-8 rounded-full -mt-1" style="background: rgba(0,102,255,0.12); border: 1px solid rgba(0,102,255,0.2); transform: rotate(-20deg); transform-origin: top center;"></div>
            <div class="w-3 h-3 rounded-full -mt-1" style="background: rgba(0,102,255,0.25); border: 1px solid rgba(0,102,255,0.4);"></div>
          </div>

          <!-- torso -->
          <div class="flex flex-col items-center mx-1">
            <div class="w-16 h-20 rounded-xl" style="background: rgba(0,102,255,0.08); border: 1px solid rgba(0,102,255,0.2); box-shadow: inset 0 1px 0 rgba(255,255,255,0.05);">
              <div class="w-px h-12 mx-auto mt-3" style="background: rgba(0,102,255,0.2);"></div>
            </div>
            <div class="w-14 h-5 rounded-b-lg -mt-1" style="background: rgba(0,102,255,0.1); border: 1px solid rgba(0,102,255,0.18); border-top: none;"></div>
          </div>

          <!-- right arm pointing out -->
          <div class="flex flex-col items-start mt-1">
            <div class="w-3 h-10 rounded-full" style="background: rgba(0,102,255,0.15); border: 1px solid rgba(0,102,255,0.25); transform: rotate(12deg); transform-origin: top center;"></div>
            <div class="w-2.5 h-10 rounded-full -mt-1" style="background: rgba(0,102,255,0.12); border: 1px solid rgba(0,102,255,0.25); transform: rotate(32deg); transform-origin: top center;"></div>
            <div class="w-3.5 h-3.5 rounded-full -mt-1" style="background: rgba(0,102,255,0.3); border: 1px solid rgba(0,102,255,0.5); box-shadow: 0 0 8px rgba(0,102,255,0.4);"></div>
          </div>

        </div>

        <!-- legs -->
        <div class="flex gap-2 -mt-1">
          <div class="flex flex-col items-center">
            <div class="w-5 h-14 rounded-t-sm rounded-b-lg" style="background: rgba(0,102,255,0.12); border: 1px solid rgba(0,102,255,0.2);"></div>
            <div class="w-7 h-3 rounded-sm -mt-0.5" style="background: rgba(0,102,255,0.18); border: 1px solid rgba(0,102,255,0.3);"></div>
          </div>
          <div class="flex flex-col items-center">
            <div class="w-5 h-14 rounded-t-sm rounded-b-lg" style="background: rgba(0,102,255,0.12); border: 1px solid rgba(0,102,255,0.2);"></div>
            <div class="w-7 h-3 rounded-sm -mt-0.5" style="background: rgba(0,102,255,0.18); border: 1px solid rgba(0,102,255,0.3);"></div>
          </div>
        </div>

        <!-- shadow -->
        <div class="w-24 h-3 mt-1 rounded-full" style="background: rgba(0,102,255,0.1); filter: blur(6px);"></div>
      </div>
    </div>

    <!-- text + buttons -->
    <div class="flex flex-col gap-6 text-center items-center flex-1">
      <div>
        <p class="text-xs font-bold tracking-widest uppercase mb-4" style="color: #3a5080; letter-spacing: 0.15em;">
          Join the community
        </p>
        <h2 class="text-4xl font-black tracking-tight leading-tight mb-4" style="color: #eef0f8; letter-spacing: -0.03em;">
          Ready to find<br/>your people?
        </h2>
        <p class="text-sm font-light" style="color: #4b5263; line-height: 1.8; max-width: 380px;">
          Create your space in seconds. Free to start, built to grow.
        </p>
      </div>

      <div class="flex items-center gap-3 flex-wrap justify-center mt-2">
        <button class="cta-register flex items-center gap-2 px-6 py-3 rounded-xl transition-all duration-200">
          <span class="text-sm font-semibold" style="color:#fff;">Create account</span>
          <svg width="14" height="14" viewBox="0 0 14 14" fill="none">
            <path d="M3 7h8M7 3l4 4-4 4" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>

        <button class="cta-login flex items-center gap-2 px-6 py-3 rounded-xl transition-all duration-200">
          <span class="text-sm font-semibold" style="color: #9ca3af;">Sign in</span>
          <svg width="14" height="14" viewBox="0 0 14 14" fill="none">
            <path d="M3 7h8M7 3l4 4-4 4" stroke="#4b5263" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>
      </div>
    </div>

  </div>

</section>

<style>
  .cta-register {
    background: #0066FF;
    border: 1px solid rgba(0,102,255,0.5);
    cursor: pointer;
    box-shadow: 0 0 24px rgba(0,102,255,0.35);
    transition: all 0.2s;
  }
  .cta-register:hover {
    background: #1a74ff;
    box-shadow: 0 0 36px rgba(0,102,255,0.55);
    transform: translateY(-1px);
  }
  .cta-login {
    background: rgba(255,255,255,0.03);
    border: 1px solid rgba(255,255,255,0.08);
    cursor: pointer;
    transition: all 0.2s;
  }
  .cta-login:hover {
    background: rgba(255,255,255,0.06);
    border-color: rgba(255,255,255,0.14);
    transform: translateY(-1px);
  }
</style>