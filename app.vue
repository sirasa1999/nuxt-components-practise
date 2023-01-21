<template>
  <div>
    <AlertsAlert />
    <AlertsAlert name="lime" />
  </div>
</template>

<script lang="ts" setup>
  import { defineProps } from 'vue';
  const props = defineProps({
  color: {type: String, default:"teal"}
})
</script>

