<template>
  <v-card
    class="mx-auto"
    max-width="344"
    width="300"
    height="350"
    outlined
  >
    <v-row
      class="ml-2 mt-2"
    >
      <v-chip
        v-if="data.tag_name != null"
        label
        dark
        small
        color="black"
      >
        {{ data.tag_name }}
      </v-chip>
    </v-row>
    <v-card-title>
      <v-row
        justify="center"
      >
        <span
          class="title"
        >
          {{ data.pack_name }}
        </span>
      </v-row>
    </v-card-title>
    <v-row
      justify="center"
    >
      <v-btn
        class="mx-2"
        fab
        dark
        large
        color="cyan"
      >
        S
      </v-btn>
    </v-row>
    <br>
    <v-row
      justify="center"
      class="overline"
    >
      Take your class any YM studio!<br>
      Choose from 250 weekly classes<br>
      7 day booking window
    </v-row>
    <br>
    <v-row
      justify="center"
    >
      <span class="title">
        $ {{ data.pack_price }}
      </span>
    </v-row>
  </v-card>
</template>

<script>

export default {
  name: 'PackListItem',

  components: {
  },

  props: {
    data: {
      type: Object,
      default: () => {},
    },
  },

  data: () => ({
  }),

  computed: {
  },

  mounted() {
  },

  methods: {
  },
};
</script>
