<script setup>
const contacts = {
  address: '陕西西安',
  phone: '155563 55573',
  email: 'liukt@company.com',
  wechat: '15556355573'
}
</script>

<template>
  <div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow">
    <h2 class="text-2xl font-bold text-gray-800 mb-6">联系我们</h2>
    
    <div class="space-y-4 text-gray-600">
      <div class="flex items-center">
        <div class="w-5">
          <svg class="w-4 h-4 text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
          </svg>
        </div>
        <span class="text-sm text-gray-400 hover:text-gray-800 transition-colors">{{ contacts.address }}</span>
      </div>

      <div class="flex items-center">
        <div class="w-5">
          <svg class="w-4 h-4 text-green-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
          </svg>
        </div>
        <span class="text-gray-400 hover:text-gray-800 transition-colors">{{ contacts.phone }}</span>
      </div>

      <div class="flex items-center">
        <div class="w-5">
          <svg class="w-4 h-4 text-purple-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
          </svg>
        </div>
        <span class="text-gray-400 hover:text-gray-800 transition-colors">{{ contacts.email }}</span>
      </div>

      <div class="mt-6 border-t pt-4">
        <div class="flex items-center justify-center gap-3 space-x-4">
          <div class="text-center">
            <div class="w-16 h-16 bg-gray-50 hover:bg-gray-100 rounded-lg mb-2 transition-colors shadow-md"></div>
            <span class="text-xs text-gray-500">微信客服</span>
          </div>
          <div class="text-center">
            <div class="w-16 h-16 bg-gray-50 hover:bg-gray-100 rounded-lg mb-2 transition-colors shadow-md"></div>
            <span class="text-xs text-gray-500">公众号</span>
          </div>
        </div>
      </div>
    </div>
    <div class="mt-6 border-t pt-4">
      <div class="flex items-center justify-center gap-3 space-x-4">
        <div class="flex items-center gap-3">
          <div class="w-5">
            <svg class="w-4 h-4 text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <!-- 图标路径保持不变 -->
            </svg>
          </div>
          <span class="text-sm text-gray-400 hover:text-gray-800 transition-colors">{{ contacts.address }}</span>
        </div>
        
        <!-- 其他联系方式区块应用相同修改 -->
        
        <div class="w-16 h-16 bg-gray-50 hover:bg-gray-100 rounded-lg mb-2 transition-colors shadow-md"></div>
      </div>
    </div>
  </div>
</template>