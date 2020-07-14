<template>
  <div class="author">
    <h1 v-if="showTitle" class="author__site-title">{{ $static.metadata.siteName }}</h1>

    <p class="author__intro">
      Hi there! I'm Natasha, a japanese woman currently studying abroad at Sciences Po, Paris. On this blog, I shared advices for japanese students willing to study abroad.
      <img
      src="/images/uploads/author.png"
      alt="Author_Picture"
      width:="64"
      height="64"
      />
    </p>

    <p class="author__links">
      <a href="#">Follow on Instagram</a>
      <a href="#">Contact me</a>
    </p>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
  props: ["showTitle"]
};
</script>

<style lang="scss">
.author {
  margin: 0 auto;
  max-width: 500px;
  text-align: center;
  padding-bottom: calc(var(--space) / 2);

  &__image {
    border-radius: 100%;
    width: 90px;
    height: 90px;
    margin-bottom: 1em;
  }

  &__intro {
    display: flex;
    align-items: center;
    opacity: 0.8;
    margin-top: 0.5em;
    text-align: left;
    img {
      margin-left: 0.5em;
    }
  }

  &__site-title {
    margin: 0 auto;
    font-size: 1.5em;
    max-width: 400px;
  }

  &__links {
    margin-top: -0.5em;
    a {
      margin: 0 0.5em;
    }
  }
}
</style>
