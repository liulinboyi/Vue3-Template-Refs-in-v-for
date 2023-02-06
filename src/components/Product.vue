<script lang="ts" setup>
interface Props {
  externalId: string;
}

const { externalId } = defineProps<Props>();

defineExpose({
  externalId,
});
</script>
<template>
  <div>Item: {{ externalId }}</div>
</template>
