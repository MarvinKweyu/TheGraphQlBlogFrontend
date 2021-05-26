<template>
  <router-link :to="`/author/${author.user.username}`">
    {{ displayName }}
  </router-link>
</template>

<script>
export default {
  name: "AuthorLink",
  props: {
    author: {
      type: Object,
      required: true,
    },
  },
  computed: {
    displayName() {
      //  show user first and second name if provided else default to username
      return (
        (this.author.user.firstName &&
          this.author.user.lastName &&
          `${this.author.user.firstName} ${this.author.user.lastName}`) ||
        `${this.author.user.username}`
      );
    },
  },
};
</script>