<template>
  <div className="tweet">
    <img
      referrerpolicy="no-referrer"
      src="https://i.imgur.com/b0EdHVV.jpg"
      className="profile"
      alt="profile"
    />
  </div>
</template>

<script setup>
defineProps({
  image: {
    type: String,
    default: "https://i.imgur.com/b0EdHVV.jpg",
  },
  imageAlt: {
    type: String,
    default: "Profile picture of a dog",
  },
});
</script>
