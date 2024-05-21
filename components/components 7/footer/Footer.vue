<script setup>

import IconFacebook from "@/components/icons/IconFacebook.vue";
import IconInstagram from "@/components/icons/IconInstagram.vue";
import IconTwitterX from "@/components/icons/IconTwitterX.vue";
</script>

<template>
  <footer class="my-footer">
    <img class="footer-logo" src="../../assets/cbsnews.jpg" alt="CBS News Logo">
    <p class="footer-p">Copyright ©2024 CBS Interactive Inc. All rights reserved.</p>
    <ul class="footer-links">
      <li><a href="#">Privacy Policy</a></li>
      <li><a href="#">manage cookies</a></li>
      <li><a href="#">terms of use</a></li>
      <li><a href="#">about</a></li>
      <li><a href="#">Advertise</a></li>
      <li><a href="#">closed captioning</a></li>
      <li><a href="#">CBS News Store</a></li>
      <li><a href="#">site map</a></li>
      <li><a href="#">contact us</a></li>
      <li><a href="#">help</a></li>
    </ul>
    <ul class="footer-icons">
      <li><a href="https://www.facebook.com/CBSNews"><IconFacebook /></a></li>
      <li><a href="https://twitter.com/CBSNews"><IconTwitterX /></a></li>
      <li><a href="https://www.instagram.com/CBSNews/"><<IconInstagram /></a></li>
      <li><a href="https://www.youtube.com/user/CBSNews"><IconFacebook /></a></li>
    </ul>
  </footer>

</template>

<style scoped>

footer {
  display: block;
  unicode-bidi: isolate;
  background-color: #101010;
  color: #F2F2F2;
}

p {
  display: block;
  margin-block-start: 1em;
  margin-block-end: 1em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  unicode-bidi: isolate;
}

ul {
  display: block;
  list-style: none;
  margin-block-start: 1em;
  margin-block-end: 1em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  padding-inline-start: 40px;
  unicode-bidi: isolate;
}

a {
  color: white;
}



@media (min-width: 1020px) {

  .my-footer {
    column-count: 1;
    text-align: center;
    padding: 80px 20px 50px;
  }

  .my-footer .footer-logo {
    width: 150px;
  }

  .my-footer > p {
    font-size: .75rem;
  }

  .footer-links {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .footer-links li {
    margin-right: 15px;
  }

  .footer-icons {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .footer-icons li {
    margin-right: 15px;
  }
}

</style>
