<template>
  <div>
    <div class="about-page max-w-5xl mx-auto my-10 p-6 bg-blue-50 rounded-xl shadow-md text-slate-800 space-y-10">
      <section class="company-overview">
        <h2 class="text-3xl font-bold text-blue-900 mb-3">About Our Company</h2>
        <p class="text-base"><!-- Company Overview: Who you are, when established, what you do --></p>
      </section>

      <section class="mission-vision">
        <h3 class="text-2xl font-semibold text-blue-800 mb-2">Our Mission</h3>
        <p class="text-base mb-4"><!-- Your mission statement here --></p>

        <h3 class="text-2xl font-semibold text-blue-800 mb-2">Our Vision</h3>
        <p class="text-base"><!-- Your vision statement here --></p>
      </section>

      <section class="core-values">
        <h3 class="text-2xl font-semibold text-blue-800 mb-3">Core Values</h3>
        <ul class="list-disc list-inside space-y-1">
          <li><!-- Value 1 --></li>
          <li><!-- Value 2 --></li>
          <li><!-- Value 3 --></li>
        </ul>
      </section>

      <section class="products-services">
        <h3 class="text-2xl font-semibold text-blue-800 mb-3">What We Offer</h3>
        <p class="text-base"><!-- Overview of your products (e.g., iron rods, sheets, tools) and services --></p>
      </section>

      <section class="infrastructure">
        <h3 class="text-2xl font-semibold text-blue-800 mb-3">Our Infrastructure</h3>
        <p class="text-base"><!-- Details about your factories, warehouses, equipment, etc. --></p>
      </section>

      <section class="team">
        <h3 class="text-2xl font-semibold text-blue-800 mb-3">Meet Our Team</h3>
        <p class="text-base"><!-- Introduction to your leadership team or key employees --></p>
      </section>

      <section class="quality-policy">
        <h3 class="text-2xl font-semibold text-blue-800 mb-3">Quality Policy</h3>
        <p class="text-base"><!-- Commitment to quality, certifications, standards followed (e.g., ISO) --></p>
      </section>

      <section class="clients-partners">
        <h3 class="text-2xl font-semibold text-blue-800 mb-3">Our Clients & Partners</h3>
        <p class="text-base"><!-- Industries or major partners/clients you serve --></p>
      </section>

      <section class="sustainability">
        <h3 class="text-2xl font-semibold text-blue-800 mb-3">Sustainability & Responsibility</h3>
        <p class="text-base"><!-- Environmental efforts, community engagement, sustainability practices --></p>
      </section>

      <section class="contact-info">
        <h3 class="text-2xl font-semibold text-blue-800 mb-3">Contact Information</h3>
        <p class="text-base"><!-- Company address, phone, email, business hours --></p>
      </section>
    </div >
    <div class="button flex justify-center p-3 mb-2">

      <UButton class="bg-red-600 " to="/">go home</UButton>
    </div>

  </div>
</template>

<script setup lang="ts">
definePageMeta({
  layout: 'custom'
})
</script>