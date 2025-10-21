<template>
  <section id="beneficios" class="py-16 px-6">
    <div class="container mx-auto max-w-6xl">
      <div class="text-center mb-16 scroll-animate">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-6">
          Os benefícios da terapia
        </h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto">
          Descubra como o acompanhamento psicológico pode transformar sua vida
        </p>
      </div>

      <div class="grid md:grid-cols-3 gap-8">
        <div 
          v-for="benefit in benefits" 
          :key="benefit.id"
          class="scroll-animate text-center"
        >
          <div :class="benefit.iconBg" class="w-20 h-20 rounded-full flex items-center justify-center mx-auto mb-6">
            <svg class="w-10 h-10 text-white" fill="currentColor" viewBox="0 0 24 24" v-html="benefit.iconPath"></svg>
          </div>
          <h3 class="text-xl font-semibold text-gray-800 mb-4">{{ benefit.title }}</h3>
          <p class="text-gray-600">
            {{ benefit.description }}
          </p>
        </div>
      </div>

      <!-- Testimonial -->
      <div class="mt-16 scroll-animate">
        <div class="bg-white rounded-3xl p-8 md:p-12 shadow-xl max-w-4xl mx-auto">
          <div class="text-center">
            <div class="w-16 h-16 bg-sage-green rounded-full flex items-center justify-center mx-auto mb-6">
              <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 24 24">
                <path d="M14.017 21v-7.391c0-5.704 3.731-9.57 8.983-10.609l.995 2.151c-2.432.917-3.995 3.638-3.995 5.849h4v10h-9.983zm-14.017 0v-7.391c0-5.704 3.748-9.57 9-10.609l.996 2.151c-2.433.917-3.996 3.638-3.996 5.849h4v10h-10z"/>
              </svg>
            </div>
            <blockquote class="text-xl md:text-2xl text-gray-700 italic mb-6 leading-relaxed">
              "A terapia me ajudou a entender melhor meus sentimentos e a lidar com a ansiedade de forma mais saudável. Hoje me sinto mais confiante e em paz comigo mesma."
            </blockquote>
            <div class="text-sage-green font-semibold">Maria S., 32 anos</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const benefits = [
  {
    id: 'autoconhecimento',
    title: 'Melhorar o autoconhecimento',
    description: 'Entenda melhor seus padrões, emoções e comportamentos para tomar decisões mais conscientes.',
    iconBg: 'bg-gradient-to-br from-sage-green to-calm-blue',
    iconPath: '<path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>'
  },
  {
    id: 'ansiedade',
    title: 'Reduzir a ansiedade',
    description: 'Aprenda técnicas eficazes para gerenciar o estresse e viver com mais tranquilidade.',
    iconBg: 'bg-gradient-to-br from-pastel-pink to-warm-green',
    iconPath: '<path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/>'
  },
  {
    id: 'leveza',
    title: 'Viver com mais leveza',
    description: 'Encontre equilíbrio emocional e aprenda a lidar com os desafios da vida de forma mais serena.',
    iconBg: 'bg-gradient-to-br from-calm-blue to-sage-green',
    iconPath: '<path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.94-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/>'
  }
]
</script>
