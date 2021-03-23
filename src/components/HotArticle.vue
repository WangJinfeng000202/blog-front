<template>
  <Card class="hot-article">
    <span class="title">热文排行</span>
    <divider/>
    <Row class="article-item" type="flex" justify="space-between" v-for="(item,index) in hotArticle" :key="index">
      <i-col class="item-title" span="18">
        <Tag color="error" v-if="index<2">{{ index + 1 }}</Tag>
        <Tag color="primary" v-else>{{ index + 1 }}</Tag>
        {{ item.title }}
      </i-col>
      <i-col class="check-praise" span="6">
        {{ item.check }}阅/{{ item.praise }}赞
      </i-col>
    </Row>
  </Card>
</template>

<script>
export default {
  name: 'HotArticle',
  data () {
    return {
      hotArticle: [
        {
          title: 'SpringBoot自动装配原理',
          check: 1000,
          praise: 10
        }, {
          title: 'SpringBoot自动装配原理',
          check: 1000,
          praise: 10
        }, {
          title: 'SpringBoot自动装配原理',
          check: 1000,
          praise: 10
        }, {
          title: 'SpringBoot自动装配原理',
          check: 1000,
          praise: 10
        }, {
          title: 'SpringBoot自动装配原理',
          check: 1000,
          praise: 10
        }, {
          title: 'SpringBoot自动装配原理',
          check: 1000,
          praise: 10
        }, {
          title: 'SpringBoot自动装配原理',
          check: 1000,
          praise: 10
        }, {
          title: 'SpringBoot自动装配原理',
          check: 1000,
          praise: 10
        }
      ]
    }
  },
  created () {
    this.getHotArticle()
  },
  methods: {
    // 根据用户id查询热门文章
    getHotArticle () {
    }
  }
}
</script>

<style lang="less">
.hot-article {
  margin-top: 10px;

  .title {
    color: #01AAED;
  }

  .item-title {
    font-size: 16px;
  }

  .item-title:hover {
    color: #01AAED;
  }

  .check-praise {
    font-size: 13px;
  }
}

</style>
