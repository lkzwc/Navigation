<script setup>
import { ref } from 'vue'
const showMenu = ref(false)
</script>

<template>
  <div class="grid h-screen grid-rows-[100px_auto_100px] bg-gray-50 overflow-hidden">
    <!-- 顶部导航 -->
    <header class="bg-white shadow-md">
      <nav class="container mx-auto flex justify-between items-center py-4 px-4 md:px-0">
        <div class="text-xl font-bold text-gray-800">流客科技</div>
        <ul class="hidden md:flex space-x-8 text-gray-700 font-medium">
          <li><a href="#official" class="hover:text-blue-500 transition-colors">官网</a></li>
          <li><a href="#simcard" class="hover:text-blue-500 transition-colors">流量卡</a></li>
          <li><a href="#numbercard" class="hover:text-blue-500 transition-colors">号卡</a></li>
          <li><a href="#wifi" class="hover:text-blue-500 transition-colors">WiFi</a></li>
        </ul>
        <button class="md:hidden flex items-center px-2 py-1 border rounded text-gray-700 border-gray-400" @click="showMenu = !showMenu">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/></svg>
        </button>
      </nav>
      <!-- 移动端菜单 -->
      <div v-if="showMenu" class="md:hidden bg-white border-t">
        <ul class="flex flex-col px-4 py-2 space-y-2">
          <li><a href="#official" class="block py-2 hover:text-blue-500 transition-colors">官网</a></li>
          <li><a href="#simcard" class="block py-2 hover:text-blue-500 transition-colors">流量卡</a></li>
          <li><a href="#numbercard" class="block py-2 hover:text-blue-500 transition-colors">号卡</a></li>
          <li><a href="#wifi" class="block py-2 hover:text-blue-500 transition-colors">WiFi</a></li>
        </ul>
      </div>
    </header>

    <!-- 内容区块 -->
    <main class="container mx-auto px-4 py-6 overflow-y-auto">
      <div class="grid gap-6 md:grid-cols-2 lg:grid-cols-4">
        <section id="official" class="bg-white rounded-xl shadow-md p-6 flex flex-col items-center transform transition-all duration-300 hover:shadow-lg hover:-translate-y-1">
          <div class="text-2xl font-semibold mb-3">官网</div>
          <a href="https://your-official-site.com" target="_blank" class="text-blue-500 hover:text-blue-700 transition-colors">
            <i class="fa-solid fa-globe mr-1"></i> 访问官网
          </a>
        </section>
        <section id="simcard" class="bg-white rounded-xl shadow-md p-6 flex flex-col items-center transform transition-all duration-300 hover:shadow-lg hover:-translate-y-1">
          <div class="text-2xl font-semibold mb-3">流量卡</div>
          <a href="https://your-simcard-link.com" target="_blank" class="text-blue-500 hover:text-blue-700 transition-colors">
            <i class="fa-solid fa-sim-card mr-1"></i> 查看流量卡
          </a>
        </section>
        <section id="numbercard" class="bg-white rounded-xl shadow-md p-6 flex flex-col items-center transform transition-all duration-300 hover:shadow-lg hover:-translate-y-1">
          <div class="text-2xl font-semibold mb-3">号卡</div>
          <a href="https://your-numbercard-link.com" target="_blank" class="text-blue-500 hover:text-blue-700 transition-colors">
            <i class="fa-solid fa-phone mr-1"></i> 查看号卡
          </a>
        </section>
        <section id="wifi" class="bg-white rounded-xl shadow-md p-6 flex flex-col items-center transform transition-all duration-300 hover:shadow-lg hover:-translate-y-1">
          <div class="text-2xl font-semibold mb-3">WiFi</div>
          <a href="https://your-wifi-link.com" target="_blank" class="text-blue-500 hover:text-blue-700 transition-colors">
            <i class="fa-solid fa-wifi mr-1"></i> 查看WiFi
          </a>
        </section>
      </div>
    </main>

    <!-- 联系方式 -->
    <footer class="bg-white border-t py-6">
      <div class="container mx-auto text-center text-gray-600">
        <div class="flex flex-wrap justify-center gap-4">
          <span><i class="fa-brands fa-weixin mr-1"></i> 微信 15556355573</span>
          <span>|</span>
          <span><i class="fa-brands fa-qq mr-1"></i> QQ 15556355573</span>
          <span>|</span>
          <span><i class="fa-solid fa-envelope mr-1"></i> 邮箱 your@email.com</span>
        </div>
      </div>
    </footer>
  </div>
</template>

<style>
body {
  font-family: 'Inter', 'Helvetica Neue', Arial, 'PingFang SC', 'Hiragino Sans GB', 'Microsoft YaHei', sans-serif;
}
</style>