<template>
<footer
  style="background-image: url('/images/cube.jpg')"
  class="relative bg-cover bg-center bg-no-repeat py-10"
>
  <div class="absolute inset-0 bg-black/40"></div>

  <div class="relative px-4 md:px-20">
    <div
      class="
        flex justify-between items-center
        px-5 py-6 md:px-10
        bg-white/10
        backdrop-blur-lg
        border border-white/20
        rounded-[1.5rem]
        shadow-[0_8px_32px_rgba(0,0,0,0.25)]
      "
    >
      <p class="font-archivo text-sm md:text-base text-neutral-100">
        <i class="fa-regular fa-copyright"></i>
        2026 Mitch Barcenilla.
      </p>

      <a
        href="#"
        class="
          text-sm md:text-base
          text-neutral-100
          hover:text-[#ED1B24]
          transition-colors duration-300
        "
      >
        Back to Top
      </a>
    </div>
  </div>
</footer>
</template>