<template>
  <Card class="tag-cloud">
    <span class="title">标签云</span>
    <divider/>
    <Tag class="tag-item" :color="tagColors[getRandomNumber()]" v-for="(item,index) in tags" :key="index">
      {{ item.name }}
    </Tag>
  </Card>
</template>

<script>
export default {
  name: 'TagCloud',
  data () {
    return {
      tagColors: ['primary', 'success', 'error', 'warning', 'magenta', 'red',
        'volcano', 'orange', 'gold', 'yellow', 'lime', 'green', 'cyan', 'blue', 'geekblue', 'purple'],
      tags: [{
        id: '1',
        name: 'Spring'
      }, {
        id: '2',
        name: 'SpringMVC'
      }, {
        id: '3',
        name: 'SpringBoot'
      }, {
        id: '4',
        name: 'SpringCloud'
      }, {
        id: '5',
        name: 'SpringSecurity'
      }, {
        id: '6',
        name: 'MySQL'
      }, {
        id: '7',
        name: 'Redis'
      }]
    }
  },
  methods: {
    getAllTags () {
    },
    getRandomNumber () {
      const length = this.tagColors.length
      return Math.floor(Math.random() * length)
    }
  }
}
</script>

<style lang="less">
.tag-cloud {
  margin-top: 10px;

  .title {
    color: #01AAED;
  }

  .tag-item {
    margin-bottom: 10px;
  }
}
</style>
