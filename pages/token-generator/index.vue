<script setup lang="ts">

const state = reactive({
  toggle: undefined,
  range: undefined
})

</script>

<template>
  <UCard>
    <h1>Token 生成器</h1>

    <p>使用您想要的字符、大写或小写字母、数字和/或符号生成随机字符串。</p>
    <template #header>
      <Placeholder class="h-8" />
    </template>

    <Placeholder class="h-32" />
  
    <UForm ref="form" :state="state">
      <UFormGroup name="toggle" label="大写 (ABC...)">
        <UToggle v-model="state.toggle" />
      </UFormGroup>

      <UFormGroup name="toggle" label="数字 (123...)">
        <UToggle v-model="state.toggle" />
      </UFormGroup>

      <UFormGroup name="toggle" label="小写 (abc...)">
        <UToggle v-model="state.toggle" />
      </UFormGroup>

      <UFormGroup name="toggle" label="符号 (!-;...)">
        <UToggle v-model="state.toggle" />
      </UFormGroup>

      <UFormGroup name="range" label="长度 (70)">
        <URange v-model="state.range" />
      </UFormGroup>
    </UForm>
  
    <template #footer>
      <Placeholder class="h-8" />
    </template>
  </UCard>
</template>
