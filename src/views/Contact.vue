<template>
    <main>
      <PageHeader
        title="Contact Us"
        description="Get in touch with our team. We'd love to hear from you!"
      />
      
      <section class="py-16 bg-white">
        <div class="container mx-auto px-4">
          <div class="grid grid-cols-1 lg:grid-cols-2 gap-16">
            <!-- Contact Form -->
            <div class="bg-white p-8 rounded-2xl shadow-lg">
              <h2 class="text-2xl font-bold mb-6">Send Us a Message</h2>
              <ContactForm />
            </div>
            
            <!-- Contact Information -->
            <div class="lg:pl-8">
              <h2 class="text-2xl font-bold mb-6">Get in Touch</h2>
              <ContactInfo />
            </div>
          </div>
        </div>
      </section>
    </main>
  </template>
  
  <script setup>
  import PageHeader from '@/components/shared/PageHeader.vue';
  import ContactForm from '@/components/contact/ContactForm.vue';
  import ContactInfo from '@/components/contact/ContactInfo.vue';
  
  const socialLinks = [
    { icon: 'pi pi-facebook' },
    { icon: 'pi pi-twitter' },
    { icon: 'pi pi-instagram' },
    { icon: 'pi pi-linkedin' }
  ];
  </script>