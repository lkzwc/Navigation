<script setup>
</script>

<template>
  <div class="min-h-screen flex flex-col bg-gray-50">
    <!-- 顶部导航 -->
    <header class="bg-white shadow-md">
      <nav class="container mx-auto flex justify-between items-center py-4 px-4 md:px-0">
        <div class="text-xl font-bold text-blue-600">导航站</div>
        <ul class="hidden md:flex space-x-8 text-gray-700 font-medium">
          <li><a href="#official" class="hover:text-blue-500">官网</a></li>
          <li><a href="#simcard" class="hover:text-blue-500">流量卡</a></li>
          <li><a href="#numbercard" class="hover:text-blue-500">号卡</a></li>
          <li><a href="#wifi" class="hover:text-blue-500">WiFi</a></li>
        </ul>
        <button class="md:hidden flex items-center px-2 py-1 border rounded text-gray-700 border-gray-400" @click="showMenu = !showMenu">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/></svg>
        </button>
      </nav>
      <!-- 移动端菜单 -->
      <div v-if="showMenu" class="md:hidden bg-white border-t">
        <ul class="flex flex-col px-4 py-2 space-y-2">
          <li><a href="#official" class="block py-2 hover:text-blue-500">官网</a></li>
          <li><a href="#simcard" class="block py-2 hover:text-blue-500">流量卡</a></li>
          <li><a href="#numbercard" class="block py-2 hover:text-blue-500">号卡</a></li>
          <li><a href="#wifi" class="block py-2 hover:text-blue-500">WiFi</a></li>
        </ul>
      </div>
    </header>

    <!-- 内容区块 -->
    <main class="flex-1 container mx-auto px-4 py-8 grid gap-8 md:grid-cols-2 lg:grid-cols-4">
      <section id="official" class="bg-white rounded-lg shadow p-6 flex flex-col items-center">
        <div class="text-2xl font-semibold mb-2">官网</div>
        <a href="https://your-official-site.com" target="_blank" class="text-blue-500 underline">访问官网</a>
      </section>
      <section id="simcard" class="bg-white rounded-lg shadow p-6 flex flex-col items-center">
        <div class="text-2xl font-semibold mb-2">流量卡</div>
        <a href="https://your-simcard-link.com" target="_blank" class="text-blue-500 underline">查看流量卡</a>
      </section>
      <section id="numbercard" class="bg-white rounded-lg shadow p-6 flex flex-col items-center">
        <div class="text-2xl font-semibold mb-2">号卡</div>
        <a href="https://your-numbercard-link.com" target="_blank" class="text-blue-500 underline">查看号卡</a>
      </section>
      <section id="wifi" class="bg-white rounded-lg shadow p-6 flex flex-col items-center">
        <div class="text-2xl font-semibold mb-2">WiFi</div>
        <a href="https://your-wifi-link.com" target="_blank" class="text-blue-500 underline">查看WiFi</a>
      </section>
    </main>

    <!-- 联系方式 -->
    <footer class="bg-white border-t py-6 mt-8">
      <div class="container mx-auto text-center text-gray-600">
        联系方式：微信 15556355573 &nbsp;|&nbsp; QQ 15556355573 &nbsp;|&nbsp; 邮箱 your@email.com
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const showMenu = ref(false)
</script>

<style>
body {
  font-family: 'Inter', 'Helvetica Neue', Arial, 'PingFang SC', 'Hiragino Sans GB', 'Microsoft YaHei', sans-serif;
}
</style>
