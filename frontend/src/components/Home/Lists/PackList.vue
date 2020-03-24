<template>
  <v-container>
    <v-col
      cols="12"
    >
      <v-row>
        <v-col
          md="4"
          sm="12"
          xs="12"
          v-for="(cardData, i) in packListData"
          :key="i"
        >
          <NumberClassPackCard
            v-if="cardData.pack_alias == 'pack-10'"
            number="10"
            :data="cardData"
          />
          <NumberClassPackCard
            v-if="cardData.pack_alias == 'pack-20'"
            number="20"
            :data="cardData"
          />
          <NumberClassPackCard
            v-if="cardData.pack_alias == 'pack-30'"
            number="30"
            :data="cardData"
          />
          <SharePackCard
            v-if="cardData.pack_alias == 'share-pack-50'"
            number="50"
            :data="cardData"
          />
          <SingleClassPackCard
            v-if="cardData.pack_alias == 'single-pack'"
            :data="cardData"
          />
          <UnlimitedClassPackCard
            v-if="cardData.pack_alias == 'unlimited-pack'"
            :data="cardData"
          />
        </v-col>
      </v-row>
    </v-col>
  </v-container>
</template>

<script>
import NumberClassPackCard from '@/components/Home/Cards/NumberClassPackCard.vue';
import SingleClassPackCard from '@/components/Home/Cards/SingleClassPackCard.vue';
import UnlimitedClassPackCard from '@/components/Home/Cards/UnlimitedClassPackCard.vue';
import SharePackCard from '@/components/Home/Cards/SharePackCard.vue';

export default {
  name: 'PackList',

  components: {
    NumberClassPackCard,
    SingleClassPackCard,
    UnlimitedClassPackCard,
    SharePackCard,
  },

  props: {
    packListData: {
      type: Array,
      default: () => [],
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
