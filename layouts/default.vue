<template>
    <div>
    
          <Header />
      <slot />
      <Footer />
    </div>
  </template>

<script setup>
definePageMeta({
    layout:"footer"
})
</script>
