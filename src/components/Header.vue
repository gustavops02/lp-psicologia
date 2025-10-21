<template>
  <header class="fixed top-0 w-full z-50 bg-white/80 backdrop-blur-sm shadow-sm">
    <nav class="container mx-auto px-6 py-4">
      <div class="flex items-center justify-between">
        <div class="text-2xl font-semibold text-sage-green">
          Psicologia & Bem-Estar
        </div>
        <div class="hidden md:flex space-x-8">
          <a 
            v-for="item in menuItems" 
            :key="item.id"
            :href="item.href" 
            class="text-gray-700 hover:text-sage-green transition-colors cursor-pointer"
            @click="scrollToSection($event, item.href)"
          >
            {{ item.label }}
          </a>
        </div>
      </div>
    </nav>
  </header>
</template>

<script setup>
const menuItems = [
  { id: 'inicio', label: 'Início', href: '#inicio' },
  { id: 'sobre', label: 'Sobre', href: '#sobre' },
  { id: 'servicos', label: 'Serviços', href: '#servicos' },
  { id: 'beneficios', label: 'Benefícios', href: '#beneficios' },
  { id: 'contato', label: 'Contato', href: '#contato' }
]

const scrollToSection = (event, href) => {
  event.preventDefault()
  const targetId = href.replace('#', '')
  const targetElement = document.getElementById(targetId)
  
  if (targetElement) {
    const headerHeight = 80 // Altura aproximada do header fixo
    const targetPosition = targetElement.offsetTop - headerHeight
    
    window.scrollTo({
      top: targetPosition,
      behavior: 'smooth'
    })
  }
}
</script>
