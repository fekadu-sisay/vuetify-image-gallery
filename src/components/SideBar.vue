<script setup>
import { defineEmits } from "vue";

const emits = defineEmits(["select-option"]);

const selectOption = (isColor) => {
  emits("select-option", isColor);
};
</script>

<template>
  <v-navigation-drawer expand-on-hover rail>
    <v-list>
      <v-list-item
        prepend-avatar="https://randomuser.me/api/portraits/women/75.jpg"
        title="Jane Doe"
        subtitle="jane.doe@example.com"
      ></v-list-item>
    </v-list>

    <v-list>
      <v-list-item
        prepend-icon="mdi-image"
        title="Color Gallery"
        value="color"
        @click="selectOption(true)"
      >
      </v-list-item>
      <v-list-item
        prepend-icon="mdi-dialpad"
        title="Grayspace Gallery"
        value="color"
        @click="selectOption(false)"
      ></v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>
