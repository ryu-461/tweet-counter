<template>
  <v-app>
    <v-container fill-height>
    <v-main>
      <h1 class="white--text my-8">文字カウンター for Twitter</h1>
      <p class="white--text my-4">文字数をカウントします。ツイート前の文字数確認に便利です。</p>
      <v-textarea
        dense
        single-line
        v-model.trim="tweet"
        background-color="white"
        rounded
        outlined
        rows="10"
        required
        label="いまどうしてる？"
        maxlength="140"
        class="mx-10"
      ></v-textarea>
      <h2 class="white--text mb-4">あと{{ 140 - tweet.length}}文字入力できます</h2>
      <v-btn
        elevation="6"
        color="white"
        x-large href="https://twitter.com/"
        target="blank"
        class="mt-4">ツイートしてみる？</v-btn>
    </v-main>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {},

  data: () => ({
    tweet: ""
  }),
};
</script>

<style>
#app {
  text-align: center;
  background-color: #00aced;
}
</style>