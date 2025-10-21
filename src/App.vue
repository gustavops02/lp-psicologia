<script setup>
import { onMounted } from 'vue'
import Header from './components/Header.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import ServicesSection from './components/ServicesSection.vue'
import BenefitsSection from './components/BenefitsSection.vue'
import Footer from './components/Footer.vue'

onMounted(() => {
  // Aguardar um pouco para garantir que os componentes foram renderizados
  setTimeout(() => {
    // Adicionar animações de scroll
    const observerOptions = {
      threshold: 0.1,
      rootMargin: '0px 0px -50px 0px'
    }

    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('animate-fade-in')
        }
      })
    }, observerOptions)

    // Observar elementos com a classe 'scroll-animate'
    const elements = document.querySelectorAll('.scroll-animate')
    elements.forEach(el => {
      observer.observe(el)
    })
  }, 100)
})
</script>

<template>
  <div id="app" class="min-h-screen bg-gradient-to-br from-soft-blue via-warm-beige to-pastel-pink">
    <Header></Header>
    <HeroSection />
    <AboutSection />
    <ServicesSection />
    <BenefitsSection />
    <Footer></Footer>
  </div>
</template>

<style scoped>
.scroll-animate {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.6s ease-out;
}

.scroll-animate.animate-fade-in {
  opacity: 1;
  transform: translateY(0);
}
</style>
