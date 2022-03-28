<script setup>
import {
  IconFacebook,
  IconTwitter,
  IconInstagram,
} from "@/components/icons/index.vue";
import { FooterLinks } from "@/components/containers/links/index.vue";
</script>

<template>
  <footer class="footer">
    <div class="footer__up">
      <div class="footer__upContainer">
        <div class="footer__form">
          <h4 class="footer__keep">Keep in touch</h4>
          <input
            type="email"
            class="footer__email"
            placeholder="Email Address"
          />
          <p class="footer__follow">Follow us</p>
          <div class="footer__socials">
            <a class="footer__social" href="#"><IconFacebook /></a>
            <a class="footer__social" href="#"><IconTwitter /></a>
            <a class="footer__social" href="#"><IconInstagram /></a>
          </div>
        </div>
        <FooterLinks />
      </div>
    </div>
    <div class="footer__black">
      <div class="footer__blackContainer">
        <p class="footer__copyright">&copy; Copyright Okra &amp; CO. 2022</p>
        <p class="footer__author">Developed by Alexis</p>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/abstracts/variables" as *;

.footer {
  margin-top: 4rem;

  &__up {
    background-color: $primary6;
  }

  &__upContainer {
    margin-inline: auto;
    max-width: 1000px;
    padding: 5rem 0;
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  &__keep {
    font-size: 2rem;
    font-weight: bold;
  }

  &__email {
    margin-top: 1rem;
    background-color: transparent;
    border: none;
    border-bottom: 1px solid $gray12;

    &::placeholder {
      font-size: 0.9rem;
      text-transform: uppercase;
    }
  }

  &__follow {
    margin: 2rem 0 0.5rem;
  }

  &__socials {
    display: grid;
    grid-auto-flow: column;
    grid-column-gap: 1rem;
    justify-content: start;
  }

  &__social {
    padding: 0.5rem;
    border: 1px solid $gray12;
    border-radius: 2rem;
    transition: 0.2s ease-in;

    &:hover {
      color: $primary6;
      background-color: $gray12;
    }
  }

  &__black {
    color: $gray1;
    font-size: 0.9rem;
    background-color: $gray12;
  }

  &__blackContainer {
    padding: 0.5rem 0;
    margin-inline: auto;
    max-width: 1000px;
    display: flex;
    justify-content: space-between;
  }
}
</style>
