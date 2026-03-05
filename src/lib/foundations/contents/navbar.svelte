<script>
  import { onMount } from 'svelte';

  let scrolled = $state(false);
  let activeItem = $state('Home');

  const navItems = ['Home', 'Features', 'Community', 'Pricing'];

  onMount(() => {
    const onScroll = () => scrolled = window.scrollY > 20;
    window.addEventListener('scroll', onScroll, { passive: true });
    return () => window.removeEventListener('scroll', onScroll);
  });
</script>

<header class="fixed top-4 left-0 right-0 z-50 flex justify-center px-4 transition-all duration-300">
  <nav
    class="flex items-center justify-between px-5 transition-all duration-300
           {scrolled ? 'py-2.5 w-[85%]' : 'py-3 w-[90%]'}"
    style="
      background: {scrolled ? 'rgba(10,10,14,0.92)' : 'rgba(10,10,14,0.75)'};
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      border: 1px solid rgba(255,255,255,0.07);
      border-radius: 9999px;
      box-shadow: {scrolled ? '0 8px 32px rgba(0,0,0,0.4)' : '0 4px 16px rgba(0,0,0,0.2)'};
    "
  >

    <!-- LEFT — Logo -->
    <a href="/" class="flex items-center gap-2 no-underline shrink-0">
      <div
        class="w-7 h-7 rounded-lg flex items-center justify-center shrink-0"
        style="background: #0066FF; box-shadow: 0 0 14px rgba(0,102,255,0.45);">
        <span class="text-white font-black text-xs">A</span>
      </div>
      <span class="font-bold text-sm tracking-tight" style="color: #e8eaf0;">
        Astroblox
      </span>
    </a>

    <!-- CENTER — Nav items -->
    <ul class="flex items-center gap-1 list-none m-0 p-0">
      {#each navItems as item}
        <li>
          <button
            onclick={() => activeItem = item}
            class="relative px-4 py-1.5 rounded-full text-sm font-medium
                   transition-all duration-200 border-0 cursor-pointer"
            style="
              background: {activeItem === item ? 'rgba(0,102,255,0.15)' : 'transparent'};
              color: {activeItem === item ? '#0066FF' : '#6b7280'};
              outline: none;
            "
          >
            {#if activeItem === item}
              <span class="absolute inset-0 rounded-full"
                style="border: 1px solid rgba(0,102,255,0.3);"></span>
            {/if}
            {item}
          </button>
        </li>
      {/each}
    </ul>

    <!-- RIGHT — CTA buttons -->
    <div class="flex items-center gap-2 shrink-0">
      <a href="/login"
        class="px-4 py-1.5 rounded-full text-sm font-medium no-underline transition-all duration-200"
        style="color: #9ca3af; background: transparent;"
        onmouseenter={(e) => e.currentTarget.style.color = '#e8eaf0'}
        onmouseleave={(e) => e.currentTarget.style.color = '#9ca3af'}>
        Log in
      </a>
      <a href="/register"
        class="px-4 py-1.5 rounded-full text-sm font-semibold no-underline transition-all duration-200"
        style="background: #0066FF; color: #fff; box-shadow: 0 0 16px rgba(0,102,255,0.35);"
        onmouseenter={(e) => { e.currentTarget.style.background='#1a7aff'; e.currentTarget.style.boxShadow='0 0 22px rgba(0,102,255,0.55)'; }}
        onmouseleave={(e) => { e.currentTarget.style.background='#0066FF'; e.currentTarget.style.boxShadow='0 0 16px rgba(0,102,255,0.35)'; }}>
        Get started
      </a>
    </div>

  </nav>
</header>