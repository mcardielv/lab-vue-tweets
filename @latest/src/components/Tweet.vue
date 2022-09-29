<template>
  <div className="tweet">
    <ProfileImage
      :image="imageFather"
      :imageAlt="`${userFather.name} - profile image`"
    />
    <!-- <img
      referrerpolicy="no-referrer"
      src="https://i.imgur.com/9yw1Fyw.jpg"
      className="profile"
      alt="profile"
    /> -->

    <div className="body">
      <div className="top">
        <User />
        <Timestamp v-bind:timestamp="TimestampFather" />
        <!-- <span className="timestamp">Nov 30, 2020</span> -->
      </div>
      <Message v-bind:message="MessageFather" />
      <!-- <p className="message">
        On December 7th, we will be hosting a #webinar that will introduce you
        to #SQL! Are you ready? 🚀
      </p> -->
      <Actions />
      <!-- <div className="actions">
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div> -->
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Actions from "./Actions.vue";
import Message from "./Message.vue";
import Timestamp from "./Timestamp.vue";
import User from "./User.vue";
import ProfileImage from "./ProfileImage.vue";

defineProps({
  MessageFather: {
    type: String,
  },
  TimestampFather: {
    type: String,
  },
  userFather: {
    type: String,
  },
  imageFather: {
    type: String,
  },
});
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
