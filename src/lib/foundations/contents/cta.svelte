<script>
  let hovered = $state(null);
</script>

<section class="relative flex items-center justify-center min-h-screen overflow-hidden px-12"
  style="background: #08090c;">

  <!-- Ambient -->
  <div class="absolute inset-0 pointer-events-none"
    style="background: radial-gradient(ellipse 55% 45% at 30% 55%, rgba(0,102,255,0.09) 0%, transparent 70%);">
  </div>

  <div class="relative z-10 flex items-center justify-between w-full max-w-5xl gap-16">

    <!-- LEFT — Human figure in Tailwind -->
    <div class="shrink-0 flex flex-col items-center select-none" aria-hidden="true">

      <!-- Glow under feet -->
      <div class="relative flex flex-col items-center">

        <!-- HEAD -->
        <div class="w-14 h-14 rounded-full border-2 flex items-center justify-center mb-0"
          style="background: rgba(0,102,255,0.08); border-color: rgba(0,102,255,0.35);
                 box-shadow: 0 0 24px rgba(0,102,255,0.2);">
          <!-- Face dots -->
          <div class="flex gap-2.5 mb-1">
            <div class="w-1.5 h-1.5 rounded-full" style="background: #0066FF;"></div>
            <div class="w-1.5 h-1.5 rounded-full" style="background: #0066FF;"></div>
          </div>
        </div>

        <!-- NECK -->
        <div class="w-3 h-3" style="background: rgba(0,102,255,0.15);"></div>

        <!-- SHOULDERS + TORSO -->
        <div class="flex items-start">

          <!-- LEFT ARM -->
          <div class="flex flex-col items-end mt-1">
            <!-- upper arm -->
            <div class="w-3 h-10 rounded-full"
              style="background: rgba(0,102,255,0.18); border: 1px solid rgba(0,102,255,0.25);
                     transform: rotate(-8deg); transform-origin: top center;">
            </div>
            <!-- forearm -->
            <div class="w-2.5 h-8 rounded-full -mt-1"
              style="background: rgba(0,102,255,0.12); border: 1px solid rgba(0,102,255,0.2);
                     transform: rotate(-20deg); transform-origin: top center;">
            </div>
            <!-- hand -->
            <div class="w-3 h-3 rounded-full -mt-1"
              style="background: rgba(0,102,255,0.25); border: 1px solid rgba(0,102,255,0.4);">
            </div>
          </div>

          <!-- TORSO -->
          <div class="flex flex-col items-center mx-1">
            <!-- chest -->
            <div class="w-16 h-20 rounded-xl"
              style="background: rgba(0,102,255,0.10); border: 1px solid rgba(0,102,255,0.22);
                     box-shadow: inset 0 1px 0 rgba(255,255,255,0.05);">
              <!-- chest detail line -->
              <div class="w-px h-12 mx-auto mt-3" style="background: rgba(0,102,255,0.2);"></div>
            </div>
            <!-- hips -->
            <div class="w-14 h-5 rounded-b-lg -mt-1"
              style="background: rgba(0,102,255,0.13); border: 1px solid rgba(0,102,255,0.18);
                     border-top: none;">
            </div>
          </div>

          <!-- RIGHT ARM (pointing toward buttons) -->
          <div class="flex flex-col items-start mt-1">
            <!-- upper arm -->
            <div class="w-3 h-10 rounded-full"
              style="background: rgba(0,102,255,0.18); border: 1px solid rgba(0,102,255,0.25);
                     transform: rotate(12deg); transform-origin: top center;">
            </div>
            <!-- forearm — extended outward -->
            <div class="w-2.5 h-10 rounded-full -mt-1"
              style="background: rgba(0,102,255,0.15); border: 1px solid rgba(0,102,255,0.3);
                     transform: rotate(32deg); transform-origin: top center;">
            </div>
            <!-- hand -->
            <div class="w-3.5 h-3.5 rounded-full -mt-1"
              style="background: rgba(0,102,255,0.3); border: 1px solid rgba(0,102,255,0.5);
                     box-shadow: 0 0 10px rgba(0,102,255,0.35);">
            </div>
          </div>

        </div>

        <!-- LEGS -->
        <div class="flex gap-2 -mt-1">
          <!-- Left leg -->
          <div class="flex flex-col items-center">
            <div class="w-5 h-14 rounded-t-sm rounded-b-lg"
              style="background: rgba(0,102,255,0.14); border: 1px solid rgba(0,102,255,0.22);">
            </div>
            <!-- foot -->
            <div class="w-7 h-3 rounded-sm -mt-0.5"
              style="background: rgba(0,102,255,0.2); border: 1px solid rgba(0,102,255,0.3);">
            </div>
          </div>
          <!-- Right leg -->
          <div class="flex flex-col items-center">
            <div class="w-5 h-14 rounded-t-sm rounded-b-lg"
              style="background: rgba(0,102,255,0.14); border: 1px solid rgba(0,102,255,0.22);">
            </div>
            <!-- foot -->
            <div class="w-7 h-3 rounded-sm -mt-0.5"
              style="background: rgba(0,102,255,0.2); border: 1px solid rgba(0,102,255,0.3);">
            </div>
          </div>
        </div>

        <!-- Ground glow -->
        <div class="w-24 h-3 mt-1 rounded-full"
          style="background: rgba(0,102,255,0.12); filter: blur(6px);">
        </div>

      </div>
    </div>

    <!-- RIGHT — Text + auth buttons -->
    <div class="flex flex-col gap-6">

      <div>
        <p class="text-xs font-bold tracking-widest uppercase mb-3"
          style="color: #0066FF; letter-spacing: 0.15em;">
          Join the community
        </p>
        <h2 class="text-4xl font-black tracking-tight leading-tight mb-3"
          style="color: #eef0f8; font-family: 'Syne', sans-serif; letter-spacing: -0.03em;">
          Ready to find<br/>your people?
        </h2>
        <p class="text-sm font-light" style="color: #4b5263; line-height: 1.8; max-width: 340px;">
          Create your space in seconds. Free to start, built to grow.
        </p>
      </div>

      <!-- Auth buttons -->
      <div class="flex flex-col gap-3 w-64">

        <!-- Register -->
        <a href="/register"
          class="flex items-center justify-between px-5 py-3.5 rounded-xl no-underline
                 transition-all duration-200 group"
          style="
            background: #0066FF;
            box-shadow: 0 0 24px rgba(0,102,255,0.3);
          "
          onmouseenter={(e) => {
            e.currentTarget.style.background = '#1a74ff';
            e.currentTarget.style.boxShadow = '0 0 36px rgba(0,102,255,0.5)';
            e.currentTarget.style.transform = 'translateY(-1px)';
          }}
          onmouseleave={(e) => {
            e.currentTarget.style.background = '#0066FF';
            e.currentTarget.style.boxShadow = '0 0 24px rgba(0,102,255,0.3)';
            e.currentTarget.style.transform = 'translateY(0)';
          }}
        >
          <div class="flex items-center gap-3">
            <div class="w-7 h-7 rounded-lg flex items-center justify-center"
              style="background: rgba(255,255,255,0.15);">
              <svg width="14" height="14" viewBox="0 0 14 14" fill="none">
                <path d="M7 1a3 3 0 1 1 0 6 3 3 0 0 1 0-6zm4 9.5c0-1.5-1.8-2.5-4-2.5S3 9 3 10.5V13h8v-2.5z"
                  fill="white"/>
              </svg>
            </div>
            <span class="text-sm font-semibold" style="color: #fff;">Create account</span>
          </div>
          <svg width="14" height="14" viewBox="0 0 14 14" fill="none" class="transition-transform duration-200 group-hover:translate-x-0.5">
            <path d="M3 7h8M7 3l4 4-4 4" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </a>

        <!-- Login -->
        <a href="/login"
          class="flex items-center justify-between px-5 py-3.5 rounded-xl no-underline
                 transition-all duration-200 group"
          style="
            background: rgba(255,255,255,0.03);
            border: 1px solid rgba(255,255,255,0.08);
          "
          onmouseenter={(e) => {
            e.currentTarget.style.borderColor = 'rgba(0,102,255,0.35)';
            e.currentTarget.style.background = 'rgba(0,102,255,0.07)';
            e.currentTarget.style.transform = 'translateY(-1px)';
          }}
          onmouseleave={(e) => {
            e.currentTarget.style.borderColor = 'rgba(255,255,255,0.08)';
            e.currentTarget.style.background = 'rgba(255,255,255,0.03)';
            e.currentTarget.style.transform = 'translateY(0)';
          }}
        >
          <div class="flex items-center gap-3">
            <div class="w-7 h-7 rounded-lg flex items-center justify-center"
              style="background: rgba(0,102,255,0.12); border: 1px solid rgba(0,102,255,0.2);">
              <svg width="14" height="14" viewBox="0 0 14 14" fill="none">
                <path d="M9 1H5a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h4M11 7H6m0 0 2-2M6 7l2 2"
                  stroke="#0066FF" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </div>
            <span class="text-sm font-semibold" style="color: #9ca3af;">Sign in</span>
          </div>
          <svg width="14" height="14" viewBox="0 0 14 14" fill="none" class="transition-transform duration-200 group-hover:translate-x-0.5">
            <path d="M3 7h8M7 3l4 4-4 4" stroke="#4b5263" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </a>

      </div>
    </div>

  </div>

</section>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Syne:wght@800&display=swap');
</style>