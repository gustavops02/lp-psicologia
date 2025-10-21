<template>
  <section id="sobre" class="py-16 px-6 bg-gradient-to-br from-soft-gray to-warm-beige">
    <div class="container mx-auto max-w-6xl">
      <div class="text-center mb-16 scroll-animate">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-6">
          Conheça a Dra. Ana Beatriz
        </h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto">
          Psicóloga clínica especializada em terapia cognitivo-comportamental e desenvolvimento pessoal
        </p>
      </div>

      <div class="grid lg:grid-cols-2 gap-12 items-center">
        <!-- Foto e informações básicas -->
        <div class="scroll-animate">
          <div class="relative">
            <div class="w-80 h-80 mx-auto mb-8 relative">
              <img 
                src="https://images.unsplash.com/photo-1559839734-2b71ea197ec2?w=400&h=400&fit=crop&crop=face&auto=format&q=80"
                alt="Dra. Ana Beatriz - Psicóloga"
                class="w-full h-full object-cover rounded-3xl shadow-2xl"
              />
              <div class="absolute -bottom-4 -right-4 w-16 h-16 bg-sage-green rounded-full flex items-center justify-center shadow-lg">
                <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
                </svg>
              </div>
            </div>
            
            <!-- Informações profissionais -->
            <div class="bg-white rounded-2xl p-6 shadow-lg">
              <h3 class="text-2xl font-bold text-gray-800 mb-4">Dra. Ana Beatriz Silva</h3>
              <div class="space-y-3">
                <div class="flex items-center">
                  <svg class="w-5 h-5 text-sage-green mr-3" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/>
                  </svg>
                  <span class="text-gray-700">CRP 06/123456</span>
                </div>
                <div class="flex items-center">
                  <svg class="w-5 h-5 text-sage-green mr-3" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
                  </svg>
                  <span class="text-gray-700">8 anos de experiência</span>
                </div>
                <div class="flex items-center">
                  <svg class="w-5 h-5 text-sage-green mr-3" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/>
                  </svg>
                  <span class="text-gray-700">Terapia Online e Presencial</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Texto sobre a psicóloga -->
        <div class="scroll-animate space-y-6">
          <div class="bg-white rounded-2xl p-8 shadow-lg">
            <h3 class="text-2xl font-bold text-gray-800 mb-4">Minha História</h3>
            <p class="text-gray-600 leading-relaxed mb-4">
              Sou formada em Psicologia pela Universidade de São Paulo (USP) e especializada em 
              Terapia Cognitivo-Comportamental. Ao longo dos meus 8 anos de carreira, tenho 
              dedicado minha vida a ajudar pessoas a encontrarem seu caminho para o bem-estar 
              emocional e o crescimento pessoal.
            </p>
            <p class="text-gray-600 leading-relaxed">
              Acredito profundamente que cada pessoa tem dentro de si a capacidade de superar 
              desafios e construir uma vida mais plena e significativa. Meu trabalho é guiá-las 
              nessa jornada de autoconhecimento e transformação.
            </p>
          </div>

          <!-- Especializações -->
          <div class="bg-white rounded-2xl p-8 shadow-lg">
            <h3 class="text-2xl font-bold text-gray-800 mb-6">Especializações</h3>
            <div class="grid md:grid-cols-2 gap-4">
              <div 
                v-for="specialty in specialties" 
                :key="specialty.id"
                class="flex items-center p-3 bg-soft-blue rounded-lg"
              >
                <div :class="specialty.iconBg" class="w-10 h-10 rounded-full flex items-center justify-center mr-3">
                  <svg :class="specialty.iconColor" class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24" v-html="specialty.iconPath"></svg>
                </div>
                <span class="text-gray-700 font-medium">{{ specialty.name }}</span>
              </div>
            </div>
          </div>

          <!-- Depoimento -->
          <div class="bg-gradient-to-r from-sage-green to-calm-blue rounded-2xl p-8 text-white">
            <div class="flex items-start">
              <img 
                src="https://images.unsplash.com/photo-1494790108755-2616b612b786?w=60&h=60&fit=crop&crop=face&auto=format&q=80"
                alt="Cliente"
                class="w-12 h-12 rounded-full mr-4 flex-shrink-0"
              />
              <div>
                <blockquote class="text-lg italic mb-2">
                  "A Dra. Ana me ajudou a entender e superar minha ansiedade de uma forma que 
                  eu nunca imaginei ser possível. Sua abordagem acolhedora e profissional 
                  transformou minha vida."
                </blockquote>
                <cite class="text-sm opacity-90">- Maria, 28 anos</cite>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const specialties = [
  {
    id: 'tcc',
    name: 'TCC - Terapia Cognitivo-Comportamental',
    iconBg: 'bg-soft-blue',
    iconColor: 'text-calm-blue',
    iconPath: '<path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/>'
  },
  {
    id: 'ansiedade',
    name: 'Transtornos de Ansiedade',
    iconBg: 'bg-warm-green',
    iconColor: 'text-sage-green',
    iconPath: '<path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>'
  },
  {
    id: 'depressao',
    name: 'Depressão e Humor',
    iconBg: 'bg-pastel-pink',
    iconColor: 'text-pink-400',
    iconPath: '<path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.94-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/>'
  },
  {
    id: 'relacionamentos',
    name: 'Relacionamentos Interpessoais',
    iconBg: 'bg-warm-beige',
    iconColor: 'text-yellow-600',
    iconPath: '<path d="M16 4c0-1.11.89-2 2-2s2 .89 2 2-.89 2-2 2-2-.89-2-2zm4 18v-6h2.5l-2.54-7.63A1.5 1.5 0 0 0 18.54 8H16c-.8 0-1.54.37-2.01.99L12 11l-1.99-2.01A2.5 2.5 0 0 0 8 8H5.46c-.8 0-1.54.37-2.01.99L1 18.5H3.5V22h3v-6h2v6h3v-6h2v6h3z"/>'
  }
]
</script>
