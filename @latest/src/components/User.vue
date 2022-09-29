<template>
  <span className="user">
    <span className="name">{{ user.name }}</span>
    <span className="handle">{{ user.handle }}</span>
  </span>
</template>

<script setup>
defineProps({
  user: {
    Type: Object,
    default: () => ({
      name: "Snoop Dogg",
      handle: "@Snoopy",
    }),
  },
});
</script>
