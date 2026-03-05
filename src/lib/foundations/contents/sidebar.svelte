<script>
  import { onMount } from 'svelte';

  let scrollProgress = $state(0);
  let activeDot = $state(0);

  const DOTS = 6;

  onMount(() => {
    const onScroll = () => {
      const scrollTop = window.scrollY;
      const docHeight = document.documentElement.scrollHeight - window.innerHeight;
      scrollProgress = docHeight > 0 ? scrollTop / docHeight : 0;
      activeDot = Math.min(DOTS - 1, Math.floor(scrollProgress * DOTS));
    };
    window.addEventListener('scroll', onScroll, { passive: true });
    return () => window.removeEventListener('scroll', onScroll);
  });

  // @ts-ignore
  const scrollToSection = (index) => {
    const target = (index / (DOTS - 1)) * (document.documentElement.scrollHeight - window.innerHeight);
    window.scrollTo({ top: target, behavior: 'smooth' });
  };
</script>

<aside class="fixed left-4 top-0 h-screen z-50 flex flex-col items-center justify-center gap-3">
  {#each Array(DOTS) as _, i}
    <button
      onclick={() => scrollToSection(i)}
      aria-label="Scroll to section {i + 1}"
      class="transition-all duration-300 rounded-sm cursor-pointer border-0 p-0
             {activeDot === i ? 'w-2.5 h-2.5 rotate-45' : 'w-1.5 h-1.5'}"
      style="
        background: {activeDot === i ? '#0066FF' : '#2a2d35'};
        box-shadow: {activeDot === i ? '0 0 10px rgba(0,102,255,0.7)' : 'none'};
        outline: none;
      "
    ></button>
  {/each}
</aside>