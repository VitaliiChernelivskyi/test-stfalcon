<template>
  <nav class="nav">
    <NuxtLink to="/" class="logo">LOGO</NuxtLink>
    <div class="nav-link_items">
      <NuxtLink class="nav-link">Home</NuxtLink>
      <NuxtLink class="nav-link"> About</NuxtLink>
      <NuxtLink class="nav-link"> Pricing</NuxtLink>
      <NuxtLink class="nav-link"> Facts</NuxtLink>
      <NuxtLink class="nav-link"> Blog</NuxtLink>
      <NuxtLink class="nav-link"> Support</NuxtLink>
      <tooltip>
        <button class="tooltip-btn">Download</button>
      </tooltip>
      <language-switch/>
    </div>
  </nav>
</template>

<script>
export default {
  name: "TheHeader",
}

</script>

<style lang="scss">
.nav {
  padding-top: 28px;
  padding-bottom: 28px;
  display: flex;
  align-items: center;
  justify-content: space-between;

  .logo {
    font-weight: 700;
    font-size: 40px;
    line-height: 49px;
    color: #6750A4;
  }

  .nav-link_items {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    align-items: center;
    gap: 24px;

    .nav-link {
      font-weight: 400;
      font-size: 18px;
      line-height: 28px;
      color: #23153E;
      text-decoration: none;

      &:hover {
        cursor: pointer;
      }
    }
  }

  .tooltip-btn {
    padding-left: 40px;
    padding-right: 40px;
  }
}

</style>
