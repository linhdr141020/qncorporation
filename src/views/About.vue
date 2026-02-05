<template>
  <main>
    <PageHeader
      title="About Us"
      description="We're a team of passionate creators and innovators"
    />
    
    <section class="py-16 bg-white">
      <div class="container mx-auto px-20">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
          <div>
            <h2 class="text-3xl font-bold mb-6">Our Story</h2>
            <p class="text-gray-600 mb-4">
              Founded in 2019, we have been building mobile applications and software solutions that enable businesses to digitize their operations and grow sustainably. Our team blends creativity with strong technical expertise to deliver products that are both visually compelling and highly effective in driving business results.
            </p>
            <div class="grid grid-cols-2 gap-8">
              <div v-for="stat in stats" :key="stat.label" class="text-center">
                <div class="text-4xl font-bold text-blue-600 mb-2">{{ stat.value }}</div>
                <div class="text-gray-600">{{ stat.label }}</div>
              </div>
            </div>
          </div>
          <div class="relative">
            <img
              src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?auto=format&fit=crop&q=80&w=800"
              alt="Team meeting"
              class="rounded-lg shadow-xl"
            />
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script setup>
import PageHeader from '@/components/shared/PageHeader.vue';

const stats = [
  { value: '2+', label: 'Projects Completed' },
  { value: '50+', label: 'Happy Clients' },
  { value: '10+', label: 'Team Members' },
  { value: '2+', label: 'Years Experience' }
];
</script>