<template>
  <div class="block-title">
    <div :class="`text-${align}`">
      <template v-if="title">
        <h1 v-if="tag === 'h1'" class="block-title__title">
          <slot>{{ title }}</slot>
        </h1>
        <h2 v-else-if="tag === 'h2'" class="block-title__title">
          <slot>{{ title }}</slot>
        </h2>
        <h3 v-else-if="tag === 'h3'" class="block-title__title">
          <slot>{{ title }}</slot>
        </h3>
        <h4 v-else-if="tag === 'h4'" class="block-title__title">
          <slot>{{ title }}</slot>
        </h4>
        <h4 v-else class="block-title__title">
          <slot>{{ title }}</slot>
        </h4>
      </template>

      <div v-if="subtitle" class="block-title__subtitle">
        {{ subtitle }}
      </div>
      <div class="block-title_line"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BlockTitle',
  props: {
    title: {
      type: String
    },
    subtitle: {
      type: String
    },
    tag: {
      type: String,
      default: 'h1'
    },
    align: {
      type: String,
      default: 'center'
    }
  }
}
</script>

<style lang="scss">
.block-title {

  &_line {
    height: 3px;
    width: 46px;
    background: #FF2D55;
    margin-top: 21px;

  }
}

.text-start {
  display: flex;
  flex-direction: column;
  align-items: start;
}

.text-center {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}
</style>
