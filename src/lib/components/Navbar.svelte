<script>
  import { onMount } from 'svelte';
  
  let isScrolled = false;

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 10;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<nav class="fixed top-0 left-0 right-0 z-50 transition-all duration-300 {isScrolled ? 'bg-white/90 backdrop-blur-md border-b border-gray-100 py-3' : 'bg-transparent py-5'}">
  <div class="container-custom flex items-center justify-between">
    <div class="flex items-center gap-8">
      <a href="/" class="flex items-center gap-2 text-xl font-bold tracking-tight text-gray-900">
        <!-- Logo Icon -->
        <svg width="28" height="28" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" class="text-plain-green">
          <path d="M64.62 430.04c0 15.95-12.93 28.89-28.87 28.89-15.96 0-28.89-12.94-28.89-28.89 0-15.94 12.93-28.87 28.89-28.87 15.94 0 28.87 12.93 28.87 28.87z" fill="#f8cb70"/>
          <path d="M218.84 304.07c-22.49 0-44.94 4.55-65.62 13.44-20.03 8.59-38.31 21.19-53.53 36.8-15.25 15.63-27.39 34.25-35.49 54.53-2.92 7.24-5.3 14.67-7.14 22.21-.93 3.82-1.74 7.7-2.38 11.59-2.39 13.99-3.61 28.86 6.76 39.98 6.2 6.67 15.02 10.52 24.14 10.52h169.48V308.12c-11.66-2.59-23.76-4.05-36.22-4.05z" fill="#f8cb70"/>
          <path d="M339.53 480.65c0 6.86-5.63 12.5-12.49 12.5H204.26c-6.87 0-12.48-5.64-12.48-12.5V320.36c0-6.87 5.61-12.49 12.48-12.49h122.78c6.86 0 12.49 5.62 12.49 12.49v160.29z" fill="#ffffff"/>
          <path d="M341.82 476.76c0 6.15-5.03 11.21-11.21 11.21l-110.21 4.5c-6.16 0-11.21-1.49-11.21-7.66V328.49c0-6.17 2.3-6.8 8.46-6.8H330.6c6.18 0 11.21 5.04 11.21 11.21v143.86z" fill="#B6DCFD"/>
        </svg>
        Clipboard Health
      </a>
      
      <div class="hidden md:flex items-center gap-6 text-sm font-medium text-gray-600">
        <a href="#" class="hover:text-gray-900 transition-colors">For Workers</a>
        <a href="#" class="hover:text-gray-900 transition-colors">For Facilities</a>
        <a href="#" class="hover:text-gray-900 transition-colors">About</a>
        <a href="#" class="hover:text-gray-900 transition-colors">Careers</a>
      </div>
    </div>

    <div class="flex items-center gap-3">
      <a href="#" class="px-3 py-1.5 text-xs font-semibold border border-gray-200 rounded text-gray-700 hover:border-gray-400 transition-colors uppercase tracking-wide">
        Sign In
      </a>
      <a href="#" class="px-3 py-1.5 text-xs font-semibold bg-plain-green text-white rounded hover:bg-green-400 transition-colors uppercase tracking-wide">
        Get Started
      </a>
    </div>
  </div>
</nav>
