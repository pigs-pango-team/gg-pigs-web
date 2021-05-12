<template>
  <v-container fluid pa-0>
    <v-row
      no-gutters
      justify="end"
      align="center"
      class="footer-area"
      :style="{ color: [dayMode ? 'var(--grey-9)' : 'var(--grey-4)'] }"
    >
      <v-col cols="auto">
        &copy; {{ new Date().getFullYear() }} Pig95team, Inc. All rights reserved
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { mapGetters } from 'vuex';

export default {
  computed: {
    ...mapGetters(['dayMode']),
  },
};
</script>

<style scoped>
.container {
  font: 14px 'Spoqa Han Sans Neo', sans-serif;
}

.footer-area {
  margin: 0 auto;
}

@media all and (min-width: 1264px) {
  .footer-area {
    max-width: 1200px;
    height: 124px;
  }
}

@media all and (min-width: 600px) and (max-width: 1263px) {
  .footer-area {
    max-width: 770px;
    height: 92px;
  }
}

@media all and (max-width: 599px) {
  .footer-area {
    max-width: 562px;
    height: 92px;
  }
}
</style>
