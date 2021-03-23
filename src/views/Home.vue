<template>
  <div class="home">
    <Layout class="layout-wrapper">
      <Header class="nav">
        <Row type="flex">
          <i-col span="9">
          </i-col>
          <i-col span="15">
            <Menu mode="horizontal" active-name="0">
            <MenuItem name="0">
              <Icon type="ios-home"/>
              首页
            </MenuItem>
            <MenuItem name="1">
              <Icon type="ios-paper"/>
              文章精选
            </MenuItem>
              <MenuItem name="1-1">
              <Icon type="ios-paper"/>
              文章归档
            </MenuItem>
            <MenuItem name="2">
              <Icon type="ios-people"/>
              项目
            </MenuItem>
            <MenuItem name="3">
              <Icon type="ios-people"/>
              时间轴
            </MenuItem>
            <MenuItem name="4">
              <Icon type="ios-construct"/>
              关于本站
            </MenuItem>
            <Submenu name="5">
              <template slot="title">
                <Icon type="ios-stats"/>
                联系我
              </template>
              <MenuItem name="5-1">GitHub</MenuItem>
            </Submenu>
          </Menu></i-col>
        </Row>
      </Header>
      <Content class="content-con">
        <Row class="con-main" :md="24" :lg="18" :gutter="20" type="flex" justify="center">
          <!--首页内容左边部分-->
          <i-col class="con-left" :md="12" :sm="24" :xs="24">
            <!--轮播图-->
            <Carousel
              class="rotate"
              autoplay
              dots="inside"
              radius-dot
              trigger="click"
              arrow="hover"
              loop>
              <CarouselItem>
                <div class="demo-carousel">1</div>
              </CarouselItem>
              <CarouselItem>
                <div class="demo-carousel">2</div>
              </CarouselItem>
              <CarouselItem>
                <div class="demo-carousel">3</div>
              </CarouselItem>
              <CarouselItem>
                <div class="demo-carousel">4</div>
              </CarouselItem>
            </Carousel>
            <!--最近文章-->
            <template>
              <p>最新文章</p>
              <card class="article" v-for="index of 10" :key="index">
                <Row type="flex" :gutter="10">
                  <i-col span="6"><img class="article-cover" src="../assets/java.jpg" alt=""/></i-col>
                  <i-col span="18">
                    <h3 class="article-title">SpringBoot启动原理</h3>
                    <p class="article-content">
                      不购物券和文化或物权法黑切哦佛我哈佛我外通过外高桥我发给我它为股权偶老公吧红文化馆后杠喷漆我会过去恢复供气文化我还给我回文该服务我去服务器而非婆凤凰网文化服务头发呜呜哦if我去过8地放弃我国8委员会为访问火凤凰一份我发觉啊爱爱划分为Pro我宏伟环绕屏我认为我就让我拍我排污染物排入我维普网好维护工委品日晚间今天评委会我放假我脾气
                    </p>
                  </i-col>
                </Row>
                <Row class="basic-info" type="flex" :gutter="20">
                  <i-col>
                    <Icon type="md-time"/>&nbsp;
                    <span>2021-01-19 09:35</span>
                  </i-col>
                  <i-col>
                    <Icon type="md-person"/>&nbsp;
                    <span>Adela</span>
                  </i-col>
                  <i-col>
                    <Icon type="md-folder"/>&nbsp;
                    <span>SpringBoot</span>
                  </i-col>
                  <i-col>
                    <Icon type="md-pricetag"/>&nbsp;
                    <span>SpringBoot &nbsp;源码</span>
                  </i-col>
                </Row>
              </card>
              <Page class="page" :total="100"/>
            </template>
          </i-col>
          <!--首页内容右边部分-->
          <i-col class="con-right" :md="6" :sm="0" :xs="0">
            <!--author-->
            <Card class="author">
              <img class="avatar-my" src="../assets/avatar.jpg" alt=""/>
              <div class="name"><span>Adela</span></div>
              <div>
                <span class="motto">有志者，事竟成！</span>
              </div>
              <div><span class="address">山东 — 菏泽</span></div>
              <!--联系我-->
              <divider>联系我</divider>
              <span class="contact-me"><i>QQ</i><i>微信</i><i>留言</i><i>微博</i></span>
            </Card>
            <!--搜索-->
            <Card class="search">
              <Row :gutter="10">
                <i-col span="18">
                  <label>
                    <Input v-model="keyWords" placeholder="输入关键字"></Input>
                  </label></i-col>
                <i-col span="6">
                  <Button type="primary">搜索</Button>
                </i-col>
              </Row>
            </Card>
            <!--热门文章-->
            <HotArticle/>
            <!--标签云-->
            <TagCloud/>
            <!--友情链接-->
            <Card></Card>
            <!--时间简记-->
            <!--最新评论-->
            <!--归档-->
          </i-col>
        </Row>
      </Content>
      <Footer>footer</Footer>
    </Layout>
  </div>
</template>

<script>
import HotArticle from '@/components/HotArticle'
import TagCloud from '@/components/TagCloud'

export default {
  name: 'Home',
  components: {
    HotArticle,
    TagCloud
  },
  data () {
    return {
      keyWords: ''
    }
  }
}
</script>

<style lang="less">
.ivu-divider-horizontal {
  margin: 10px 0
}

.home {
  height: 100%;

  .layout-wrapper {
    .nav {
      background-color: #fff;
      box-shadow: 0 1px 1px 1px #e0e0e0;
    }
  }

  .content-con {
    margin-top: 10px;
    width: 100%;
    height: 100%;
    padding: 0;
    background: url(http://api.3ewl.cc/acg/img.php) no-repeat top
    center fixed;
    background-size: cover;
    .con-main {
      .ivu-col {
        background-clip: content-box;
      }

      .con-left {

        .rotate {
          height: 300px;
          margin-bottom: 10px;
          background-color: #580d0d;
        }

        .article {
          height: 180px;
          margin-bottom: 10px;

          .article-cover {
            height: 110px;
          }

          .ivu-card-body {
            height: 100%;
          }

          .article-title:hover {
            text-decoration: #01AAED solid underline;
          }

          .article-content {
            display: block;
            display: -webkit-box;
            line-height: 1.8;
            font-size: 14px;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
            text-overflow: ellipsis;
            text-indent: 28px;
            margin-top: 10px;
          }

          .basic-info {
            color: grey;
          }
        }

        .article:hover .article-title {
          color: #01AAED;
        }

        .page {
          display: flex;
          justify-content: center;
        }
      }

      .con-right {
        .author .ivu-card-body {
          width: 100%;
          height: 100%;
          display: flex;
          flex-direction: column;
          text-align: center;
          align-items: center;

          .avatar-my {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            display: block;
          }

          .name {
            font-size: 16px;
            text-align: center;
            margin-top: 20px;
          }

          .motto {
            font-size: 20px;
          }

          .address {
            font-size: 16px;
            color: #808080;
          }

          .contact-me {
            margin-top: 20px;
          }
        }

        .search {
          margin-top: 10px;
        }

        .hot-article {

        }
      }
    }

  }
}
</style>
