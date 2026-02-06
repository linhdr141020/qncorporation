<template>
    <div class="space-y-6">
      <div v-for="item in contactInfo" :key="item.title" class="flex items-start gap-4">
        <div class="p-3 bg-blue-50 rounded-lg">
          <i :class="item.icon + ' text-xl text-blue-600'"></i>
        </div>
        <div>
          <h3 class="font-semibold text-lg mb-1">{{ item.title }}</h3>
          <p class="text-gray-600">{{ item.content }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  const contactInfo = [
    {
      icon: 'pi pi-map-marker',
      title: 'Visit Us',
      content: 'No. 44, Alley 445 Lac Long Quan Street, Xuan La Ward, Tay Ho District, Hanoi City, Vietnam'
    },
    {
      icon: 'pi pi-envelope',
      title: 'Email Us',
      content: 'support@gravityhubs.com'
    },
    {
      icon: 'pi pi-phone',
      title: 'Call Us',
      content: '+84 974848363'
    },
    {
      icon: 'pi pi-clock',
      title: 'Working Hours',
      content: 'Monday - Friday: 9:00 AM - 6:00 PM'
    }
  ];
  </script>