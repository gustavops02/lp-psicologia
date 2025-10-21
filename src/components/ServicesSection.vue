<template>
  <section id="servicos" class="py-16 px-6 bg-white/50">
    <div class="container mx-auto max-w-6xl">
      <div class="text-center mb-16 scroll-animate">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-6">
          Como posso te ajudar?
        </h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto">
          Ofereço acompanhamento psicológico especializado em diferentes áreas, 
          sempre com foco no seu bem-estar e crescimento pessoal.
        </p>
      </div>

      <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
        <div 
          v-for="service in services" 
          :key="service.id"
          class="scroll-animate bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2"
        >
          <div :class="service.iconBg" class="w-16 h-16 rounded-full flex items-center justify-center mb-6">
            <svg :class="service.iconColor" class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24" v-html="service.iconPath"></svg>
          </div>
          <h3 class="text-xl font-semibold text-gray-800 mb-4">{{ service.title }}</h3>
          <p class="text-gray-600">
            {{ service.description }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    id: 'ansiedade',
    title: 'Ansiedade',
    description: 'Aprenda técnicas para gerenciar a ansiedade e recuperar a tranquilidade em sua vida.',
    iconBg: 'bg-soft-blue',
    iconColor: 'text-calm-blue',
    iconPath: '<path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.94-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/>'
  },
  {
    id: 'autoestima',
    title: 'Autoestima',
    description: 'Desenvolva uma relação mais positiva consigo mesmo e construa sua confiança.',
    iconBg: 'bg-warm-green',
    iconColor: 'text-sage-green',
    iconPath: '<path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>'
  },
  {
    id: 'relacionamentos',
    title: 'Relacionamentos',
    description: 'Melhore suas conexões interpessoais e construa relacionamentos mais saudáveis.',
    iconBg: 'bg-pastel-pink',
    iconColor: 'text-pink-400',
    iconPath: '<path d="M16 4c0-1.11.89-2 2-2s2 .89 2 2-.89 2-2 2-2-.89-2-2zm4 18v-6h2.5l-2.54-7.63A1.5 1.5 0 0 0 18.54 8H16c-.8 0-1.54.37-2.01.99L12 11l-1.99-2.01A2.5 2.5 0 0 0 8 8H5.46c-.8 0-1.54.37-2.01.99L1 18.5H3.5V22h3v-6h2v6h3v-6h2v6h3z"/>'
  },
  {
    id: 'equilibrio',
    title: 'Equilíbrio Emocional',
    description: 'Encontre harmonia entre suas emoções e viva com mais serenidade e clareza.',
    iconBg: 'bg-warm-beige',
    iconColor: 'text-yellow-600',
    iconPath: '<path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/>'
  }
]
</script>
