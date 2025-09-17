<template>
  <el-config-provider :locale="zhCn"> Hello Vue.js! </el-config-provider>
</template>

<script lang="ts" setup>
import zhCn from 'element-plus/es/locale/lang/zh-cn'

import axios from 'axios'

const login = async () => {
  const { data } = await axios.post('/api/user/login', {
    username: 'admin',
    password: '123456',
  })
  console.log(data)
}

login()
</script>