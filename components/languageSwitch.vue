<template>
  <div class="custom-select-wrapper" @click="toggleDropdown">
    <div class="custom-select">
      <div class="custom-select__selected">{{ selected }}</div>
      <div class="custom-select__arrow"></div>
    </div>
    <ul class="custom-select__dropdown" v-show="showDropdown">
      <li v-for="option in options" :key="option.value" @click="selectOption(option)">
        <img :src="option.img" alt="">
        {{ option.label }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      options: [
        {label: 'Sweden', value: 1, img: '/images/flags/sweden.svg'},
        {label: 'England', value: 2, img: '/images/flags/united-kingdom.svg'},
      ],
      selected: 'lang',
      showDropdown: false,
    };
  },
  methods: {
    toggleDropdown() {
      this.showDropdown = !this.showDropdown;
    },
    selectOption(option) {
      this.selected = option.label;
      this.showDropdown = false;
    },
  },
};
</script>

<style>
.custom-select-wrapper {
  position: relative;
  width: 100px;
}

.custom-select {
  position: relative;
  display: flex;
  align-items: center;
  width: 100%;
  height: 100%;
  border-radius: 4px;
  font-size: 16px;
  cursor: pointer;
}

.custom-select__selected {
  display: inline-block;
  width: calc(100% - 24px);
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

.custom-select__arrow {
  position: absolute;
  top: 50%;
  right: 8px;
  transform: translateY(-50%);
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 6px 6px 0 6px;
  border-color: #6750A4 transparent transparent transparent;
}

.custom-select__dropdown {
  position: absolute;
  top: 100%;
  left: 0;
  min-width: 145px;
  max-height: 120px;
  overflow-y: auto;
  margin: 0;
  padding: 0;
  list-style: none;
  background: #FFFFFF;
  box-shadow: 0 6px 10px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  font-size: 16px;
}

.custom-select__dropdown li {
  display: flex;
  align-items: center;
  width: 100%;
  height: 40px;
  line-height: 40px;
  padding: 0 8px;
  cursor: pointer;

  img {
    margin-right: 10px;
  }
}

.custom-select__dropdown li:hover {
  background-color: #eee;
}
</style>
