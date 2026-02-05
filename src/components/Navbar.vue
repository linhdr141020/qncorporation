<template>
  <Menubar :model="items" class="border-none shadow-sm backdrop-blur-sm fixed w-full z-50">
    <template #start>
      <router-link to="/" class="flex items-center gap-2 mr-4">
        <img 
          src="/logo.png"
          alt="Creative workspace"
          class="w-[150px] h-[100px] rounded-2xl transform hover:scale-105 transition-transform duration-300"
        />
      </router-link>
    </template>
  </Menubar>
</template>

<script setup>
import { useRoute, useRouter } from 'vue-router';

const route = useRoute();
const router = useRouter();

const handleNavigation = (id) => {
  if (route.path === '/') {
    // On homepage - scroll to section
    const element = document.getElementById(id);
    if (element) {
      element.scrollIntoView({ behavior: 'smooth' });
    }
  } else {
    // On other pages - navigate to homepage then scroll
    router.push({
      path: '/',
      hash: `#${id}`
    });
  }
};

const items = [
  {
    label: 'Home',
    command: () => router.push('/'),
    class: 'relative after:content-[""] after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[3px] after:bg-[#5A58E9] after:transition-all hover:after:w-full'
  },
  {
    label: 'Services',
    command: () => router.push('/services'),
    class: 'relative after:content-[""] after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[3px] after:bg-[#5A58E9] after:transition-all hover:after:w-full'
  },
  {
    label: 'Contact us',
    command: () => router.push('/contact'),
    class: 'relative after:content-[""] after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[3px] after:bg-[#5A58E9] after:transition-all hover:after:w-full'
  },
  {
    label: 'About us',
    command: () => router.push('/about'),
    class: 'relative after:content-[""] after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[3px] after:bg-[#5A58E9] after:transition-all hover:after:w-full'
  }
];
</script>
