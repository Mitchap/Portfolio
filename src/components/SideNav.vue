<template>
    <div>
        <nav class="bg-neutral-50 flex flex-row justify-between items-center px-10 py-7 fixed top-0 w-screen z-80">
            <a href="#"><img src="/images/Mitch-Logo.jpg" alt="Mitch Barcenilla Logo" class="w-40" /></a>
            <div class="icon z-82">
                <button type="button" @click="toggleSideNav"
                    class="relative w-10 h-10 flex items-center justify-center">
                    <transition name="icon-fade" mode="out-in">
                        <i v-if="mobileNav" key="xmark" class="fa-solid fa-xmark"></i>
                        <i v-else key="bars" class="fa-solid fa-bars"></i>
                    </transition>
                </button>
            </div>

            <!-- Sidebar with transition -->
            <transition name="slide">
                <div v-if="mobileNav"
                    class="fixed flex justify-start h-screen z-81 top-0 transition ease-in-out duration-150 w-screen pt-5 right-0 bg-neutral-300  overflow-x-hidden shadow-lg">
                    <ul class="flex flex-col gap-10 font-archivo font-medium mt-20 mx-auto">
                        <li><a @click="toggleSideNav" href="#" class="hover-slider">Home</a></li>
                        <li><a @click="toggleSideNav" href="#about" class="hover-slider">About Me</a></li>
                        <li><a @click="toggleSideNav" href="#experience" class="hover-slider">Experience</a></li>
                        <li><a @click="toggleSideNav" href="#contact" class="hover-slider">Contact</a></li>
                        <li>
                            <a href="#" class="hover-slider">Resume
                                <i class="fa-solid fa-arrow-up-right-from-square text-sm ms-1"></i></a>
                        </li>
                    </ul>
                </div>
            </transition>
        </nav>
    </div>
</template>

<script>
export default {
    name: "navigation",
    data() {
        return {
            scrollPostion: null,
            windowWidth: null,
            mobileNav: false,
        };
    },
    methods: {
        toggleSideNav() {
            this.mobileNav = !this.mobileNav;
        },

    },
};
</script>

<style>
/* Smooth transition for icon change */
.icon-fade-enter-active,
.icon-fade-leave-active {
    transition: opacity 0.3s ease, transform 0.3s ease;
}

.icon-fade-enter-from,
.icon-fade-leave-to {
    opacity: 0;
    transform: scale(0.8);
}

/* Slide animation */
.slide-enter-active,
.slide-leave-active {
    transition: transform 0.3s ease-in-out;
}

.slide-enter-from {
    transform: translateX(100%);
}

.slide-leave-to {
    transform: translateX(100%);
}
</style>