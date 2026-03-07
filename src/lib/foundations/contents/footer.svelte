<script>
  let email = '';

  const cols = [
    {
      heading: 'Resources',
      links: ['Help Center', 'Docs', 'Roadmap', 'Changelog'],
    },
    {
      heading: 'Platform',
      links: ['Features', 'Community', 'Pricing', 'Status'],
    },
    {
      heading: 'Company',
      links: ['About', 'Careers', 'Blog', 'Contact'],
    },
  ];
</script>

<footer class="relative w-full overflow-hidden"
  style="background: #08090c; border-top: 1px solid rgba(255,255,255,0.05);">

  <!-- glow -->
  <div class="absolute bottom-0 left-0 pointer-events-none"
    style="width:500px;height:250px;background: radial-gradient(ellipse at 0% 100%, rgba(0,102,255,0.05) 0%, transparent 70%);">
  </div>

  <div class="relative z-10 max-w-6xl mx-auto px-12 pt-16 pb-10">

    <!-- top row -->
    <div class="flex items-start justify-between gap-12 mb-16">

      <!-- logo + tagline -->
      <div class="flex flex-col gap-4 shrink-0 max-w-xs">
        <div class="flex items-center gap-2">
          <div class="w-7 h-7 rounded-full flex items-center justify-center shrink-0"
            style="background: #0066FF; box-shadow: 0 0 12px rgba(0,102,255,0.4); border: 1px solid rgba(0,102,255,0.4);">
            <span class="text-white font-black text-xs">A</span>
          </div>
          <span class="font-bold text-sm tracking-tight" style="color: #c9cdd6;">Astroblox</span>
        </div>
        <p class="text-xs leading-relaxed" style="color: #2e333d;">
          The platform where your community finds its home. Build, grow and connect — all in one place.
        </p>
      </div>

      <!-- link columns -->
      <div class="flex gap-16">
        {#each cols as col (col.heading)}
          <div class="flex flex-col gap-4">
            <p class="text-xs font-bold tracking-widest uppercase" style="color: #c9cdd6; letter-spacing: 0.12em;">
              {col.heading}
            </p>
            {#each col.links as link (link)}
              <button class="footer-link text-sm text-left">{link}</button>
            {/each}
          </div>
        {/each}
      </div>

      <!-- newsletter -->
      <div class="flex flex-col gap-3 shrink-0">
        <p class="text-sm font-semibold" style="color: #c9cdd6;">Stay in the loop</p>
        <p class="text-xs" style="color: #2e333d; max-width: 200px;">Get updates on new features and community news.</p>
        <div class="flex items-center gap-2">
          <input
            bind:value={email}
            type="email"
            placeholder="Enter your email"
            class="newsletter-input px-3 py-2 rounded-lg text-xs outline-none"
            style="width: 160px;"
          />
          <button class="subscribe-btn px-3 py-2 rounded-lg text-xs font-semibold">
            Subscribe
          </button>
        </div>
      </div>

    </div>

    <!-- divider -->
    <div class="w-full h-px mb-8" style="background: linear-gradient(90deg, transparent, rgba(255,255,255,0.06), transparent);"></div>

    <!-- bottom row -->
    <div class="flex items-end justify-between gap-8">

      <!-- copyright + socials -->
      <div class="flex flex-col gap-4">
        <div class="flex items-center gap-3">

          <!-- X -->
          <button class="social-btn w-8 h-8 rounded-lg flex items-center justify-center" aria-label="X">
            <svg width="13" height="13" viewBox="0 0 24 24" fill="#4b5263">
              <path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-4.714-6.231-5.401 6.231H2.746l7.73-8.835L1.254 2.25H8.08l4.253 5.622 5.911-5.622zm-1.161 17.52h1.833L7.084 4.126H5.117z"/>
            </svg>
          </button>

          <!-- Discord -->
          <button class="social-btn discord-btn w-8 h-8 rounded-lg flex items-center justify-center" aria-label="Discord">
            <svg width="13" height="13" viewBox="0 0 24 24" fill="#5865F2">
              <path d="M20.317 4.37a19.791 19.791 0 0 0-4.885-1.515.074.074 0 0 0-.079.037c-.21.375-.444.864-.608 1.25a18.27 18.27 0 0 0-5.487 0 12.64 12.64 0 0 0-.617-1.25.077.077 0 0 0-.079-.037A19.736 19.736 0 0 0 3.677 4.37a.07.07 0 0 0-.032.027C.533 9.046-.32 13.58.099 18.057c.002.022.015.04.033.05a19.89 19.89 0 0 0 5.993 3.03.078.078 0 0 0 .084-.028 14.09 14.09 0 0 0 1.226-1.994.076.076 0 0 0-.041-.106 13.107 13.107 0 0 1-1.872-.892.077.077 0 0 1-.008-.128 10.2 10.2 0 0 0 .372-.292.074.074 0 0 1 .077-.01c3.928 1.793 8.18 1.793 12.062 0a.074.074 0 0 1 .078.01c.12.098.246.198.373.292a.077.077 0 0 1-.006.127 12.299 12.299 0 0 1-1.873.892.077.077 0 0 0-.041.107c.36.698.772 1.362 1.225 1.993a.076.076 0 0 0 .084.028 19.839 19.839 0 0 0 6.002-3.03.077.077 0 0 0 .032-.054c.5-5.177-.838-9.674-3.549-13.66a.061.061 0 0 0-.031-.03z"/>
            </svg>
          </button>

          <!-- GitHub -->
          <button class="social-btn w-8 h-8 rounded-lg flex items-center justify-center" aria-label="GitHub">
            <svg width="13" height="13" viewBox="0 0 24 24" fill="#4b5263">
              <path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0 1 12 6.844a9.59 9.59 0 0 1 2.504.337c1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.02 10.02 0 0 0 22 12.017C22 6.484 17.522 2 12 2z"/>
            </svg>
          </button>

        </div>
        <p class="text-xs" style="color: #2a2d35;">
          © {new Date().getFullYear()} Astroblox. All rights reserved.
        </p>
      </div>

      <!-- figure sitting at edge -->
      <div class="shrink-0 flex flex-col items-center select-none" aria-hidden="true" style="margin-bottom: -10px;">

        <!-- head with face details -->
        <div class="relative w-11 h-11 rounded-full flex items-center justify-center"
          style="background: rgba(0,102,255,0.1); border: 2px solid rgba(0,102,255,0.3); box-shadow: 0 0 16px rgba(0,102,255,0.15);">
          <!-- eyes -->
          <div class="flex gap-2 mb-1">
            <div class="w-1.5 h-1.5 rounded-full" style="background: #0066FF;"></div>
            <div class="w-1.5 h-1.5 rounded-full" style="background: #0066FF;"></div>
          </div>
          <!-- smile -->
          <div class="absolute bottom-2.5 w-4 h-1.5 rounded-b-full" style="border-bottom: 1.5px solid rgba(0,102,255,0.5); border-left: 1.5px solid rgba(0,102,255,0.5); border-right: 1.5px solid rgba(0,102,255,0.5);"></div>
        </div>

        <!-- neck -->
        <div class="w-2.5 h-2" style="background: rgba(0,102,255,0.15);"></div>

        <!-- shoulders + torso -->
        <div class="flex items-start">

          <!-- left arm relaxed down -->
          <div class="flex flex-col items-end mt-0.5">
            <div class="w-2.5 h-8 rounded-full"
              style="background: rgba(0,102,255,0.15); border: 1px solid rgba(0,102,255,0.25); transform: rotate(5deg); transform-origin: top center;"></div>
            <div class="w-2 h-6 rounded-full -mt-1"
              style="background: rgba(0,102,255,0.12); border: 1px solid rgba(0,102,255,0.2); transform: rotate(8deg); transform-origin: top center;"></div>
            <div class="w-3 h-2 rounded-full -mt-0.5"
              style="background: rgba(0,102,255,0.2); border: 1px solid rgba(0,102,255,0.35);"></div>
          </div>

          <!-- torso -->
          <div class="flex flex-col items-center mx-1">
            <div class="w-12 h-14 rounded-xl"
              style="background: rgba(0,102,255,0.08); border: 1px solid rgba(0,102,255,0.2); box-shadow: inset 0 1px 0 rgba(255,255,255,0.04);">
              <!-- shirt detail -->
              <div class="w-px h-8 mx-auto mt-2" style="background: rgba(0,102,255,0.2);"></div>
              <div class="w-4 h-px mx-auto mt-1" style="background: rgba(0,102,255,0.15);"></div>
            </div>
            <div class="w-12 h-3 rounded-b-md -mt-0.5"
              style="background: rgba(0,102,255,0.12); border: 1px solid rgba(0,102,255,0.18); border-top: none;"></div>
          </div>

          <!-- right arm relaxed down -->
          <div class="flex flex-col items-start mt-0.5">
            <div class="w-2.5 h-8 rounded-full"
              style="background: rgba(0,102,255,0.15); border: 1px solid rgba(0,102,255,0.25); transform: rotate(-5deg); transform-origin: top center;"></div>
            <div class="w-2 h-6 rounded-full -mt-1"
              style="background: rgba(0,102,255,0.12); border: 1px solid rgba(0,102,255,0.2); transform: rotate(-8deg); transform-origin: top center;"></div>
            <div class="w-3 h-2 rounded-full -mt-0.5"
              style="background: rgba(0,102,255,0.2); border: 1px solid rgba(0,102,255,0.35);"></div>
          </div>

        </div>

        <!-- sitting legs (horizontal thighs, dangling shins) -->
        <div class="flex gap-2 -mt-0.5">
          <div class="flex flex-col items-center">
            <div class="w-12 h-3 rounded-l-lg"
              style="background: rgba(0,102,255,0.12); border: 1px solid rgba(0,102,255,0.2);"></div>
            <div class="w-3.5 h-10 rounded-b-lg ml-4"
              style="background: rgba(0,102,255,0.1); border: 1px solid rgba(0,102,255,0.18); border-top: none;"></div>
            <div class="w-5 h-2.5 rounded-sm ml-3"
              style="background: rgba(0,102,255,0.18); border: 1px solid rgba(0,102,255,0.3);"></div>
          </div>
          <div class="flex flex-col items-center">
            <div class="w-12 h-3 rounded-r-lg"
              style="background: rgba(0,102,255,0.12); border: 1px solid rgba(0,102,255,0.2);"></div>
            <div class="w-3.5 h-10 rounded-b-lg mr-4"
              style="background: rgba(0,102,255,0.1); border: 1px solid rgba(0,102,255,0.18); border-top: none;"></div>
            <div class="w-5 h-2.5 rounded-sm mr-3"
              style="background: rgba(0,102,255,0.18); border: 1px solid rgba(0,102,255,0.3);"></div>
          </div>
        </div>

        <!-- shadow -->
        <div class="w-20 h-2 mt-1 rounded-full" style="background: rgba(0,102,255,0.08); filter: blur(4px);"></div>
      </div>

    </div>
  </div>

</footer>

<style>
  .footer-link {
    background: transparent;
    border: none;
    cursor: pointer;
    color: #4b5263;
    padding: 0;
    transition: color 0.2s;
  }
  .footer-link:hover {
    color: #9ca3af;
  }
  .social-btn {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(255,255,255,0.07);
    cursor: pointer;
    transition: all 0.2s;
  }
  .social-btn:hover {
    background: rgba(255,255,255,0.08);
    border-color: rgba(255,255,255,0.15);
  }
  .discord-btn {
    background: rgba(88,101,242,0.1);
    border-color: rgba(88,101,242,0.25);
  }
  .discord-btn:hover {
    background: rgba(88,101,242,0.18);
    border-color: rgba(88,101,242,0.4);
  }
  .newsletter-input {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(255,255,255,0.08);
    color: #c9cdd6;
    transition: border-color 0.2s;
  }
  .newsletter-input:focus {
    border-color: rgba(0,102,255,0.4);
  }
  .newsletter-input::placeholder {
    color: #2e333d;
  }
  .subscribe-btn {
    background: #0066FF;
    color: #fff;
    border: none;
    cursor: pointer;
    box-shadow: 0 0 14px rgba(0,102,255,0.3);
    transition: all 0.2s;
  }
  .subscribe-btn:hover {
    background: #1a74ff;
    box-shadow: 0 0 22px rgba(0,102,255,0.5);
  }
</style>