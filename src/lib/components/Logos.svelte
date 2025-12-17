<script>
  const logos = [
    { name: "Sunrise Senior Living", font: "font-sans font-bold" },
    { name: "Brookdale", font: "font-serif font-bold tracking-tight" },
    { name: "ATRIA", font: "font-sans font-black tracking-widest" },
    { name: "Brightview", font: "font-sans font-bold" },
    { name: "Five Star", font: "font-sans font-bold" },
    { name: "Emeritus", font: "font-serif font-bold italic" },
    { name: "BELMONT VILLAGE", font: "font-sans font-light uppercase tracking-widest text-sm" },
    { name: "Aegis Living", font: "font-sans font-bold tracking-tight" },
    { name: "Silverado", font: "font-sans font-bold" },
    { name: "OAKMONT", font: "font-sans font-black tracking-wider" },
    { name: "Meridian", font: "font-serif font-bold" },
    { name: "Pacifica", font: "font-sans font-bold italic" },
  ];
</script>

<section class="py-16 border-b border-gray-100">
  <div class="container-custom text-center">
    <p class="text-[10px] font-bold tracking-[0.2em] text-gray-400 uppercase mb-10">
      Trusted by leading healthcare facilities across 50 states
    </p>
    
    <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-x-8 gap-y-12 items-center justify-items-center opacity-60 grayscale hover:grayscale-0 transition-all duration-500">
      {#each logos as logo}
        <div class="text-xl md:text-2xl text-gray-800 flex items-center justify-center w-full">
           <!-- Placeholder for actual SVG logos -->
           <span class="{logo.font}">{logo.name}</span>
        </div>
      {/each}
    </div>
  </div>
</section>
