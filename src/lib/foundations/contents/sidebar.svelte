<script>
// @ts-nocheck

  import { onMount } from 'svelte';

  let scrollProgress = 0;
  let activeDot = 0;

  const DOTS = 6;
  const dots = Array.from({ length: DOTS }, (_, i) => i);

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

  const scrollToSection = (index) => {
    const target = (index / (DOTS - 1)) * (document.documentElement.scrollHeight - window.innerHeight);
    window.scrollTo({ top: target, behavior: 'smooth' });
  };
</script>

<aside class="fixed left-5 top-0 h-screen z-50 flex flex-col items-center justify-center gap-4">
  {#each dots as i (i)}
    <button
      on:click={() => scrollToSection(i)}
      aria-label="Scroll to section {i + 1}"
      class="dot-btn transition-all duration-300 cursor-pointer border-0 p-0"
      class:dot-active={activeDot === i}
      style="outline: none;"
    ></button>
  {/each}
</aside>

<style>
  .dot-btn {
    width: 6px;
    height: 6px;
    background: #2a2d35;
    border-radius: 1px;
    transform: rotate(0deg);
    transition: all 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
    box-shadow: none;
  }
  .dot-btn:hover {
    background: #4b5263;
    transform: rotate(45deg);
  }
  .dot-active {
    width: 8px;
    height: 8px;
    background: #0066FF;
    transform: rotate(45deg);
    box-shadow: 0 0 10px rgba(0, 102, 255, 0.6);
  }
</style>