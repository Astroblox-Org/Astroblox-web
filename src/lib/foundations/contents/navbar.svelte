<script>
  import { onMount } from 'svelte';

  let scrolled = false;
  let activeItem = 'Home';

  const navItems = ['Home', 'Features', 'Community', 'Pricing'];

  onMount(() => {
    const onScroll = () => scrolled = window.scrollY > 20;
    window.addEventListener('scroll', onScroll, { passive: true });
    return () => window.removeEventListener('scroll', onScroll);
  });
</script>

<header class="fixed top-4 left-0 right-0 z-50 flex justify-center px-4">
  <nav
    class="flex items-center justify-between px-5 transition-all duration-300 {scrolled ? 'py-2.5 w-[85%]' : 'py-3 w-[90%]'}"
    style="background: {scrolled ? 'rgba(12,12,16,0.93)' : 'rgba(12,12,16,0.72)'}; backdrop-filter: blur(18px); -webkit-backdrop-filter: blur(18px); border: 1px solid rgba(255,255,255,0.06); border-radius: 9999px; box-shadow: {scrolled ? '0 8px 32px rgba(0,0,0,0.5)' : '0 4px 16px rgba(0,0,0,0.25)'};"
  >

    <!-- logo -->
    <div class="flex items-center gap-2 shrink-0">
      <div class="w-7 h-7 rounded-full flex items-center justify-center shrink-0"
        style="background: #0066FF; box-shadow: 0 0 12px rgba(0,102,255,0.5); border: 1px solid rgba(0,102,255,0.4);">
        <span class="text-white font-black text-xs">A</span>
      </div>
      <span class="font-semibold text-sm tracking-tight" style="color: #c9cdd6;">Astroblox</span>
    </div>

    <!-- nav items -->
    <ul class="flex items-center gap-0.5 list-none m-0 p-0">
      {#each navItems as item (item)}
        <li>
          <button
            on:click={() => activeItem = item}
            class="relative px-4 py-1.5 rounded-full text-sm font-medium transition-all duration-200 border-0 cursor-pointer outline-none"
            style="background: {activeItem === item ? 'rgba(0,102,255,0.15)' : 'transparent'}; color: {activeItem === item ? '#6ea8fe' : '#4b5260'};"
          >
            {#if activeItem === item}
              <span class="absolute inset-0 rounded-full pointer-events-none"
                style="border: 1px solid rgba(0,102,255,0.35);"></span>
            {/if}
            {item}
          </button>
        </li>
      {/each}
    </ul>

    <!-- cta -->
    <div class="flex items-center gap-2 shrink-0">
      <button class="login-btn px-4 py-1.5 rounded-full text-sm font-medium transition-all duration-200">
        Log in
      </button>
      <button class="register-btn px-4 py-1.5 rounded-full text-sm font-semibold transition-all duration-200">
        Get started
      </button>
    </div>

  </nav>
</header>

<style>
  .login-btn {
    background: transparent;
    border: none;
    cursor: pointer;
    color: #4b5260;
    transition: color 0.2s;
  }
  .login-btn:hover {
    color: #9ca3af;
  }
  .register-btn {
    background: #0066FF;
    color: #fff;
    border: 1px solid rgba(0,102,255,0.4);
    cursor: pointer;
    transition: all 0.2s;
    box-shadow: 0 0 14px rgba(0,102,255,0.35);
  }
  .register-btn:hover {
    background: #1a74ff;
    box-shadow: 0 0 22px rgba(0,102,255,0.55);
  }
</style>