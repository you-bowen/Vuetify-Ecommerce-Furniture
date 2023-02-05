<script setup>

</script>

<template>
  <v-app-bar app dark flat>
    <v-btn>
      <v-icon left class="mr-2">fas fa-bars</v-icon>
    </v-btn>
    <v-toolbar-title>CATALOG</v-toolbar-title>
    <!-- <div style="position: absolute;left: 0; right: 0;text-align: center;"> -->
    <v-col cols="6" class="flex-grow-0">
    <!-- <div style="position: absolute;margin-left: auto;margin-right: auto;text-align: center;"> -->
      <!-- 这里设置margin: auto对abslute元素无效，所以我们用left和right进行居中 -->
      <h4 class="text-center">furniture</h4>
    </v-col>
    <!-- <v-spacer></v-spacer> -->
    <v-col cols="3">
      <v-text-field density="compact" variant="outlined" label="Search" append-inner-icon="fas fa-search" single-line hide-details class="mr-2"></v-text-field>
    </v-col>
  </v-app-bar>
</template>

<style scoped></style>
