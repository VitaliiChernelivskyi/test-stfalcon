<template>
  <footer class="footer">
  <div class="footer-wrapper container">

    <NuxtLink to="/">
      <div class="logo">logo</div>
    </NuxtLink>

    <div class="footer-items">
      <NuxtLink> About Us</NuxtLink>
      <NuxtLink> Blog</NuxtLink>
      <NuxtLink> Support</NuxtLink>
    </div>

    <div class="footer-items">
      <NuxtLink> Terms & Conditions</NuxtLink>
      <NuxtLink> Privacy Policy</NuxtLink>
      <NuxtLink> Cookies</NuxtLink>
    </div>

    <div class="footer-social_media-icons">
      <NuxtLink>
        <img src="../public/images/social_media_icon/facebook-negative.svg" alt="facebook">
      </NuxtLink>
      <NuxtLink>
        <img src="../public/images/social_media_icon/instagram-negative.svg" alt="instagram">
      </NuxtLink>
      <NuxtLink>
        <img src="../public/images/social_media_icon/youTube-negative.svg" alt="youTube">
      </NuxtLink>
      <NuxtLink>
        <img src="../public/images/social_media_icon/pinterest-negative.svg" alt="pinterest">
      </NuxtLink>
    </div>
  </div>
  </footer>
</template>

<script>
export default {
  name: "TheFooter"
}
</script>

<style lang="scss" scoped>
// Footer styles
.footer {
  width: 100%;
  background: #423C4E;
  color: #FFFFFF;
  &-wrapper{
    padding: 74px 50px 78px;
    display: flex;
  }
  .logo {
    font-weight: 700;
    font-size: 40px;
    line-height: 49px;
    text-transform: uppercase;
    margin-right: 92px;

  }

  .footer-items {
    line-height: 50px;
    display: flex;
    flex-direction: column;
    min-width: 286px;
    margin-right: 36px;
  }

  .footer-social_media-icons {
    gap: 20px;
    display: flex;

    img {
      width: 32px;
      height: 32px;
    }
  }
}

</style>
