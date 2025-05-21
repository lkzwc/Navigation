<script setup>
import ContactInfo from './components/ContactInfo.vue'

const navLinks = [
  { name: '首页', url: '#' },
  { name: '产品服务', url: '#' },
  { name: '关于我们', url: '#' },
]

const cardLinks = [
  { title: '业务系统', url: '#', color: 'bg-blue-600' },
  { title: '客户门户', url: '#', color: 'bg-emerald-600' },
  { title: '管理后台', url: '#', color: 'bg-violet-600' },
  { title: '文档中心', url: '#', color: 'bg-amber-600' },
]
</script>

<template>
  <div class="min-h-screen bg-gray-50">
    <nav class="bg-white shadow-sm">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between items-center h-16">
          <h1 class="text-2xl font-bold text-gray-900 tracking-tight">
            <span class="text-blue-600">企业</span>导航
          </h1>
          <div class="hidden md:flex space-x-8">
            <a 
              v-for="link in navLinks"
              :key="link.name"
              :href="link.url"
              class="text-gray-500 hover:text-blue-600 px-3 py-2 rounded-md transition-colors"
            >
              {{ link.name }}
            </a>
          </div>
        </div>
      </div>
    </nav>

    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
        <a
          v-for="(card, index) in cardLinks"
          :key="card.title"
          :href="card.url"
          class="group relative flex items-center justify-center h-48 rounded-xl shadow-lg hover:shadow-xl transition-shadow overflow-hidden"
          :class="card.color"
        >
          <div class="absolute inset-0 bg-black/20 group-hover:bg-black/30 transition-colors"></div>
          <h3 class="text-xl font-semibold text-white relative z-10">
            {{ card.title }}
          </h3>
        </a>
      </div>
    </main>

    <ContactInfo class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12" />
  </div>
</template>

<style scoped>
/* 自定义渐变动画 */
.hover-gradient {
  background-size: 200% auto;
  background-image: linear-gradient(
    to right,
    #3b82f6 0%,
    #6366f1 50%,
    #3b82f6 100%
  );
  transition: background-position 0.5s ease;
}

.hover-gradient:hover {
  background-position: right center;
}
</style>
