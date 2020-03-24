<template>
  <div>
    <PackList
      v-if="packListData"
      :pack-list-data="packListData"
    />
  </div>
</template>

<script>
import resData from '@/assets/data/res_data';
import PackList from '@/components/Home/Lists/PackList.vue';

export default {
  name: 'Home',
  components: {
    PackList,
  },
  data: () => ({
    packListData: resData.data.pack_list,
  }),
  mounted() {
    console.log({ resData });
  },
};
</script>
