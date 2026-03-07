<section class="relative flex items-center justify-center min-h-screen overflow-hidden px-12"
  style="background: #08090c;">

  <div class="absolute inset-0 pointer-events-none"
    style="background: radial-gradient(ellipse 55% 45% at 30% 55%, rgba(255,255,255,0.02) 0%, transparent 70%);">
  </div>

  <div class="relative z-10 flex items-center justify-between w-full max-w-5xl gap-16">

    <!-- figure -->
    <div class="shrink-0 flex flex-col items-center select-none" aria-hidden="true">
      <div class="relative flex flex-col items-center">

        <!-- head -->
        <div class="w-14 h-14 rounded-full flex items-center justify-center"
          style="background: rgba(255,255,255,0.04); border: 2px solid rgba(255,255,255,0.1);">
          <div class="flex gap-2.5 mb-1">
            <div class="w-1.5 h-1.5 rounded-full" style="background: rgba(255,255,255,0.3);"></div>
            <div class="w-1.5 h-1.5 rounded-full" style="background: rgba(255,255,255,0.3);"></div>
          </div>
        </div>

        <!-- neck -->
        <div class="w-3 h-3" style="background: rgba(255,255,255,0.05);"></div>

        <!-- torso + arms -->
        <div class="flex items-start">

          <!-- left arm -->
          <div class="flex flex-col items-end mt-1">
            <div class="w-3 h-10 rounded-full" style="background: rgba(255,255,255,0.06); border: 1px solid rgba(255,255,255,0.09); transform: rotate(-8deg); transform-origin: top center;"></div>
            <div class="w-2.5 h-8 rounded-full -mt-1" style="background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.08); transform: rotate(-20deg); transform-origin: top center;"></div>
            <div class="w-3 h-3 rounded-full -mt-1" style="background: rgba(255,255,255,0.08); border: 1px solid rgba(255,255,255,0.12);"></div>
          </div>

          <!-- torso -->
          <div class="flex flex-col items-center mx-1">
            <div class="w-16 h-20 rounded-xl" style="background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.08);">
              <div class="w-px h-12 mx-auto mt-3" style="background: rgba(255,255,255,0.07);"></div>
            </div>
            <div class="w-14 h-5 rounded-b-lg -mt-1" style="background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.07); border-top: none;"></div>
          </div>

          <!-- right arm -->
          <div class="flex flex-col items-start mt-1">
            <div class="w-3 h-10 rounded-full" style="background: rgba(255,255,255,0.06); border: 1px solid rgba(255,255,255,0.09); transform: rotate(12deg); transform-origin: top center;"></div>
            <div class="w-2.5 h-10 rounded-full -mt-1" style="background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.08); transform: rotate(32deg); transform-origin: top center;"></div>
            <div class="w-3.5 h-3.5 rounded-full -mt-1" style="background: rgba(255,255,255,0.1); border: 1px solid rgba(255,255,255,0.15);"></div>
          </div>

        </div>

        <!-- legs -->
        <div class="flex gap-2 -mt-1">
          <div class="flex flex-col items-center">
            <div class="w-5 h-14 rounded-t-sm rounded-b-lg" style="background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.08);"></div>
            <div class="w-7 h-3 rounded-sm -mt-0.5" style="background: rgba(255,255,255,0.07); border: 1px solid rgba(255,255,255,0.1);"></div>
          </div>
          <div class="flex flex-col items-center">
            <div class="w-5 h-14 rounded-t-sm rounded-b-lg" style="background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.08);"></div>
            <div class="w-7 h-3 rounded-sm -mt-0.5" style="background: rgba(255,255,255,0.07); border: 1px solid rgba(255,255,255,0.1);"></div>
          </div>
        </div>

        <div class="w-24 h-3 mt-1 rounded-full" style="background: rgba(255,255,255,0.04); filter: blur(6px);"></div>
      </div>
    </div>

    <!-- text + buttons -->
    <div class="flex flex-col gap-6">
      <div>
        <p class="text-xs font-bold tracking-widest uppercase mb-3" style="color: #4b5263; letter-spacing: 0.15em;">
          Join the community
        </p>
        <h2 class="text-4xl font-black tracking-tight leading-tight mb-3" style="color: #eef0f8; letter-spacing: -0.03em;">
          Ready to find<br/>your people?
        </h2>
        <p class="text-sm font-light" style="color: #4b5263; line-height: 1.8; max-width: 340px;">
          Create your space in seconds. Free to start, built to grow.
        </p>
      </div>

      <div class="flex flex-col gap-3 w-64">

        <button class="cta-register flex items-center justify-between px-5 py-3.5 rounded-xl transition-all duration-200">
          <div class="flex items-center gap-3">
            <div class="w-7 h-7 rounded-lg flex items-center justify-center" style="background: rgba(255,255,255,0.1);">
              <svg width="14" height="14" viewBox="0 0 14 14" fill="none">
                <path d="M7 1a3 3 0 1 1 0 6 3 3 0 0 1 0-6zm4 9.5c0-1.5-1.8-2.5-4-2.5S3 9 3 10.5V13h8v-2.5z" fill="white"/>
              </svg>
            </div>
            <span class="text-sm font-semibold" style="color: #fff;">Create account</span>
          </div>
          <svg width="14" height="14" viewBox="0 0 14 14" fill="none">
            <path d="M3 7h8M7 3l4 4-4 4" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>

        <button class="cta-login flex items-center justify-between px-5 py-3.5 rounded-xl transition-all duration-200">
          <div class="flex items-center gap-3">
            <div class="w-7 h-7 rounded-lg flex items-center justify-center" style="background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.1);">
              <svg width="14" height="14" viewBox="0 0 14 14" fill="none">
                <path d="M9 1H5a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h4M11 7H6m0 0 2-2M6 7l2 2"
                  stroke="rgba(255,255,255,0.3)" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </div>
            <span class="text-sm font-semibold" style="color: #9ca3af;">Sign in</span>
          </div>
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
    background: rgba(255,255,255,0.09);
    border: 1px solid rgba(255,255,255,0.12);
    cursor: pointer;
  }
  .cta-register:hover {
    background: rgba(255,255,255,0.14);
    border-color: rgba(255,255,255,0.2);
    transform: translateY(-1px);
  }
  .cta-login {
    background: rgba(255,255,255,0.03);
    border: 1px solid rgba(255,255,255,0.08);
    cursor: pointer;
  }
  .cta-login:hover {
    background: rgba(255,255,255,0.06);
    border-color: rgba(255,255,255,0.14);
    transform: translateY(-1px);
  }
</style>