<template>
  <div id="app">
    <section class="container">
      <div class="has-text-centered">
        <img src="./assets/logo.png">
        <hello></hello>
      </div>
      <hr>

      <h1 class="title">Buefy Customization Basic Setup</h1>
      <b-field>
        <b-checkbox>Checkbox</b-checkbox>
      </b-field>

      <b-field>
        <b-switch>Default</b-switch>
      </b-field>

      <b-field label="Name">
        <b-input placeholder="John Silver"></b-input>
      </b-field>

      <div class="block">
        <b-icon icon="person"></b-icon>
        <b-icon icon="home"></b-icon>
        <b-icon icon="dashboard"></b-icon>
    </div>

    <b-message title="Danger with icon" type="is-danger" has-icon>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce id fermentum quam. Proin sagittis, nibh id hendrerit imperdiet, elit sapien laoreet elit
    </b-message>

    </section>
  </div>
</template>

<script>
import Hello from './components/Hello'

export default {
  name: 'app',
  components: {
    Hello
  }
}
</script>

<style lang="scss">
  // Import Bulma's core
  @import "~bulma/sass/utilities/_all";

  // Set your colors
  $primary: #f1896f;
  $primary-invert: findColorInvert($primary);
  $twitter: #4099FF;
  $twitter-invert: findColorInvert($twitter);
  $facebook: #4267B2;
  $facebook-invert: findColorInvert($facebook);
  $google-plus: #DB4437;
  $google-plus-invert: findColorInvert($google-plus);

  // Setup $colors to use as bulma classes (e.g. 'is-twitter')
  $colors: (
      white: ($white, $black),
      black: ($black, $white),
      light: ($light, $light-invert),
      dark: ($dark, $dark-invert),
      primary: ($primary, $primary-invert),
      info: ($info, $info-invert),
      success: ($success, $success-invert),
      warning: ($warning, $warning-invert),
      danger: ($danger, $danger-invert),
      twitter: ($twitter, $twitter-invert),
      facebook: ($facebook, $facebook-invert),
      google-plus: ($google-plus, $google-plus-invert)
  );

  // Links
  $link: $primary;
  $link-invert: $primary-invert;
  $link-focus-border: $primary;

  @import "~bulma";
  @import "~buefy/src/scss/buefy";
</style>
