# Estrutura de Componentes - Landing Page Psicologia

## 📁 Organização dos Componentes

A landing page foi refatorada para ser totalmente componentizável, facilitando manutenção e reutilização.

### 🧩 Componentes Criados

#### 1. **Header.vue**
- **Função**: Navegação principal do site
- **Props**: Nenhuma
- **Dados**: Menu items configuráveis
- **Características**: 
  - Navegação fixa com backdrop blur
  - Responsiva (menu oculto em mobile)
  - Links de âncora para seções

#### 2. **HeroSection.vue**
- **Função**: Seção principal com call-to-action
- **Props**: Nenhuma
- **Dados**: URL do WhatsApp configurável
- **Características**:
  - Headline emocional
  - CTA principal para WhatsApp
  - Elemento visual com animações
  - Layout responsivo em grid

#### 3. **AboutSection.vue**
- **Função**: Apresentação da psicóloga e suas especializações
- **Props**: Nenhuma
- **Dados**: Informações da psicóloga e especializações
- **Características**:
  - Foto profissional da psicóloga
  - Informações de credenciais (CRP, experiência)
  - Especializações em cards
  - Depoimento de cliente
  - Layout responsivo em grid

#### 4. **ServicesSection.vue**
- **Função**: Apresentação dos serviços oferecidos
- **Props**: Nenhuma
- **Dados**: Array de serviços configurável
- **Características**:
  - Cards interativos com hover effects
  - Ícones SVG dinâmicos
  - Cores personalizadas por serviço
  - Grid responsivo

#### 5. **BenefitsSection.vue**
- **Função**: Benefícios da terapia e depoimento
- **Props**: Nenhuma
- **Dados**: Array de benefícios e depoimento
- **Características**:
  - Cards de benefícios com gradientes
  - Depoimento destacado
  - Layout centrado e elegante

#### 6. **Footer.vue**
- **Função**: Informações de contato e redes sociais
- **Props**: Nenhuma
- **Dados**: Informações de contato e links sociais
- **Características**:
  - CTA secundário para WhatsApp
  - Links para redes sociais
  - Informações de contato
  - Design em verde sábio

## 🔧 Vantagens da Componentização

### ✅ **Manutenibilidade**
- Cada seção é independente
- Fácil localização de código
- Modificações isoladas

### ✅ **Reutilização**
- Componentes podem ser reutilizados
- Fácil criação de variações
- Lógica centralizada

### ✅ **Escalabilidade**
- Fácil adição de novas seções
- Estrutura organizada
- Código limpo e legível

### ✅ **Testabilidade**
- Componentes isolados
- Fácil criação de testes unitários
- Debugging simplificado

## 🎨 Personalização

### **Cores Personalizadas**
Cada componente usa as cores definidas no `tailwind.config.js`:
- `sage-green`: Verde sábio principal
- `soft-blue`: Azul suave
- `warm-green`: Verde quente
- `pastel-pink`: Rosa pastel
- `warm-beige`: Bege quente
- `calm-blue`: Azul calmo

### **Animações**
- Scroll animations em todos os componentes
- Hover effects nos cards
- Transições suaves
- Animações flutuantes

### **Responsividade**
- Mobile-first design
- Breakpoints do Tailwind CSS
- Layout adaptativo
- Tipografia escalável

## 📱 Como Usar

### **Importar Componentes**
```vue
<script setup>
import Header from './components/Header.vue'
import HeroSection from './components/HeroSection.vue'
// ... outros componentes
</script>
```

### **Usar no Template**
```vue
<template>
  <div id="app">
    <Header />
    <HeroSection />
    <ServicesSection />
    <BenefitsSection />
    <Footer />
  </div>
</template>
```

### **Personalizar Dados**
Cada componente tem seus dados configuráveis no script setup, facilitando a personalização sem modificar o template.

## 🚀 Próximos Passos

1. **Adicionar Props**: Transformar dados estáticos em props para maior flexibilidade
2. **Criar Slots**: Adicionar slots para conteúdo customizável
3. **Emitir Events**: Adicionar eventos para comunicação entre componentes
4. **Adicionar Validação**: Validar props com TypeScript ou validação de props do Vue
5. **Criar Storybook**: Documentar componentes visualmente
