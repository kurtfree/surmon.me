<template>
  <div
    class="freelancer-page"
    :class="{ mobile: isMobile }"
  >
    <div class="banner">
      <div class="banner-content container">
        <h2 class="title">
          <i18n :lkey="LANGUAGE_KEYS.PAGE_FREELANCER_SLOGAN" />
        </h2>
        <div class="submit">
          <button
            class="email-me"
            title="email me"
            @click="handleSubmitEmail"
          >
            <i18n :lkey="LANGUAGE_KEYS.PAGE_FREELANCER_EMAIL_ME" />
          </button>
        </div>
        <desktop-only>
          <ulink class="upwork" :href="VALUABLE_LINKS.UPWORK">
            <span>(</span>
            <i18n :lkey="LANGUAGE_KEYS.PAGE_FREELANCER_HIRE_ME" />
            <i class="iconfont icon-upwork"></i>
            <span>)</span>
          </ulink>
        </desktop-only>
      </div>
    </div>
    <div class="module">
      <div class="container">
        <ul class="module-list">
          <li class="item">
            <p class="icon web">
              <i class="iconfont icon-html5"></i>
            </p>
            <h3 class="name">
              <i18n en="Web Client" zh="Web 客户端" />
            </h3>
            <p class="desc">
              <i18n en="Vue application" zh="Vue 应用开发" />
            </p>
            <p class="desc">
              <i18n en="React application" zh="React 应用开发" />
            </p>
            <p class="desc">
              <i18n en="Angular application" zh="Angular 应用开发" />
            </p>
          </li>
          <li class="item">
            <p class="icon nodejs">
              <i class="iconfont icon-nodejs"></i>
            </p>
            <h3 class="name">Node.js</h3>
            <p class="desc">
              <i18n en="Node.js application" zh="Node.js 整站建设" />
            </p>
            <p class="desc">
              <i18n en="Node.js Web 服务开发" zh="Node.js online bussniess" />
            </p>
            <p class="desc">
              <i18n en="Node.js 命令行工具开发" zh="Node.js CLI application" />
            </p>
          </li>
          <li class="item">
            <p class="icon app">
              <i class="iconfont icon-app"></i>
            </p>
            <h3 class="name">
              <i18n en="Hybrid App" zh="混合应用" />
            </h3>
            <p class="desc">
              <i18n en="Flutter application" zh="Flutter 应用开发" />
            </p>
            <p class="desc">
              <i18n en="React Native application" zh="React Native 应用开发" />
            </p>
            <p class="desc">
              <i18n en="Electron application" zh="Electron 应用开发" />
            </p>
          </li>
          <li class="item">
            <p class="icon wechat">
              <i class="iconfont icon-wechat"></i>
            </p>
            <h3 class="name">
              <i18n en="WeChat" zh="微信周边" />
            </h3>
            <p class="desc"><i18n en="HTML5 page" zh="H5 开发" /></p>
            <p class="desc"><i18n en="WeChat official account" zh="公众号开发" /></p>
            <p class="desc"><i18n en="WeChat mini program" zh="小程序开发" /></p>
          </li>
          <li class="item">
            <p class="icon consult">
              <i class="iconfont icon-tool"></i>
            </p>
            <h3 class="name"><i18n en="Consultant" zh="技术咨询" /></h3>
            <p class="desc"><i18n en="Everything about web" zh="语言、框架疑难杂症" /></p>
            <p class="desc"><i18n en="Business and technical" zh="业务与技术方案设计" /></p>
            <p class="desc"><i18n en="Technical consultant" zh="长期技术顾问指导" /></p>
          </li>
        </ul>
      </div>
    </div>
    <desktop-only>
      <client-only transition>
        <div class="mammon container">
          <adsense-responsive
            ins-style="display:inline-block;width:1050px;height:192px"
          />
        </div>
      </client-only>
    </desktop-only>
    <div class="step">
      <div class="step-content container">
        <ul class="step-list">
          <li class="item">
            <h3 class="name">
              <i18n zh="1. 提交需求" en="1. Consult" />
            </h3>
            <p class="desc">
              <i18n en="Product requirements document" zh="提供构思成熟的需求文档" />
            </p>
            <p class="desc">
              <i18n en="Prototype design document" zh="清晰可用的设计图或原型" />
            </p>
          </li>
          <li class="item">
            <h3 class="name">
              <i18n en="2. Confirm" zh="2. 确认需求" />
            </h3>
            <p class="desc">
              <i18n en="Price and schedule" zh="确认报价及开发周期" />
            </p>
            <p class="desc">
              <i18n en="Development cycle" zh="协商开发周期和要点" />
            </p>
          </li>
          <li class="item">
            <h3 class="name">
              <i18n en="3. Develop" zh="3. 预付开发" />
            </h3>
            <p class="desc">
              <i18n en="Payment the trust and deposit" zh="预付部分或全部" />
            </p>
            <p class="desc">
              <i18n en="Develop project" zh="进入开发流程" />
            </p>
          </li>
          <li class="item">
            <h3 class="name">
              <i18n en="4. Review" zh="4. 预收修正" />
            </h3>
            <p class="desc">
              <i18n en="Review and experience" zh="提供预览演示" />
            </p>
            <p class="desc">
              <i18n en="Fixbug and optimize" zh="细节修正调优" />
            </p>
          </li>
          <li class="item">
            <h3 class="name">
              <i18n en="5. Delivery" zh="5. 交付维护" />
            </h3>
            <p class="desc">
              <i18n en="Pay balance" zh="付清尾款，交付项目" />
            </p>
            <p class="desc">
              <i18n en="Maintenance cycle" zh="一定周期内持续维护" />
            </p>
          </li>
        </ul>
      </div>
    </div>
    <div class="rule">
      <div class="rule-content container">
        <i18n
          zh="如果你认为自己的能力足以支撑一位出色、省心、优秀、帅气、完美的的全栈工程师的生产力，请 EMail 我；非常优秀，没有之一"
          en="Any application that can be written in JavaScript, will eventually be written in JavaScript."
        />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
  import { defineComponent, computed } from 'vue'
  import { useEnhancer } from '/@/enhancer'
  import { GAEventActions, GAEventTags } from '/@/constants/gtag'
  import { LANGUAGE_KEYS } from '/@/language/key'
  import { META, VALUABLE_LINKS } from '/@/config/app.config'
  import AdsenseResponsive from '/@/components/adsense/responsive.vue'

  export default defineComponent({
    name: 'Freelancer',
    components: {
      AdsenseResponsive
    },
    setup() {
      const { i18n, helmet, gtag, isMobile, isZhLang } = useEnhancer()

      helmet(() => {
        const prefix = isZhLang.value
          ? `${i18n.t(LANGUAGE_KEYS.PAGE_FREELANCER)} | `
          : ''
        return { title: prefix + 'Freelancer' }
      })

      const handleSubmitEmail = () => {
        const subject = isZhLang.value
          ? `嗨！Surmon，久仰大名！`
          : `Technical consultant / ${META.title}`
        const body = isZhLang.value
          ? `我有一个需求：%0D%0A %0D%0A - 需求简述： %0D%0A %0D%0A - 需求文档：%0D%0A %0D%0A - 预算金额：%0D%0A %0D%0A - 预算周期：`
          : 'Hi Surmon, My name is '
        const mailAddress = `mailto:${META.email}` + (
          isMobile.value
            ? ''
            : `?subject=${subject}&body=${body}`
          )

        window.open(mailAddress)
        gtag?.event('咨询邮件', {
          event_category: GAEventActions.Click,
          event_label: GAEventTags.FreelancerPage
        })
      }

      return {
        META,
        VALUABLE_LINKS,
        LANGUAGE_KEYS,
        isMobile,
        handleSubmitEmail
      }
    }
  })
</script>

<style lang="scss" scoped>
  @import 'src/assets/styles/init.scss';

  .freelancer-page {
    width: 100%;

    .banner {
      height: $full-column-page-banner-height;
      background: $module-bg-hover cdn-url('/images/page-feeelancer/banner.jpg');
      background-size: cover;
      background-position: center 60%;

      .banner-content {
        height: 100%;
        overflow: hidden;
        text-align: center;

        .title {
          color: $white;
          margin-top: 7rem;
          margin-bottom: 4rem;
          font-weight: bold;
          font-size: $font-size-h2 * 2;
          font-family: 'webfont-normal', DINRegular;
        }

        .submit {
          margin-bottom: 2rem;

          .email-me {
            width: 10rem;
            border: 1px solid;
            border-color: $white;
            line-height: 3.8rem;
            text-align: center;
            letter-spacing: 1px;
            font-weight: bold;
            text-transform: uppercase;
            color: $white;
            transition: color $transition-time-fast, border-color $transition-time-fast;
            @include radius-box($xs-radius);

            &:hover {
              color: $primary;
              border-color: $primary;
            }
          }
        }

        .upwork {
          color: $white;
          border-bottom: 1px solid;
          border-color: transparent;
          transition:
            color $transition-time-fast,
            border-color $transition-time-fast;

          .iconfont {
            margin-left: $xs-gap;
          }

          &:hover {
            color: $primary;
            border-color: $primary;
          }
        }
      }
    }

    .module {
      margin: ($gap * 2) auto;

      .module-list {
        margin: 0;
        padding: 0;
        list-style-type: none;
        display: flex;
        justify-content: space-between;

        > .item {
          flex: 1;
          width: auto;
          height: auto;
          padding-top: $lg-gap;
          padding-bottom: $gap;
          overflow: hidden;
          text-align: center;
          margin-right: $gap * 2;
          @include radius-box($sm-radius);
          @include common-bg-module($transition-time-fast);

          &:last-child {
            margin-right: 0;
          }

          &:hover {
            background-color: $module-bg-opaque;

            .icon {
              &.web {
                color: $html5-primary;
              }
              &.nodejs {
                color: $nodejs-primary;
              }
              &.app {
                color: $primary;
              }
              &.wechat {
                color: $wechat-primary;
              }
              &.consult {
                color: #CD7F32;
              }
            }

            .desc {
              color: $text;
            }
          }

          > .icon {
            @include color-transition($transition-time-fast);

            > .iconfont {
              font-size: $font-size-h3 * 3;
            }
          }

          > .desc {
            @include color-transition($transition-time-fast);
            color: $text-disabled;
            margin-bottom: 1.2em;
          }
        }
      }
    }

    .mammon {
      height: 192px;
      margin-bottom: $gap * 2;
      @include common-bg-module();
    }

    .step {
      @include common-bg-module();

      > .step-content {
        > .step-list {
          margin: 0;
          padding: 0;
          list-style-type: none;
          display: flex;
          justify-content: space-between;

          > .item {
            width: 20%;
            height: auto;
            padding-top: $xs-gap;
            padding-bottom: $lg-gap;
            text-align: center;

            > .desc {
              color: $text-disabled;
            }
          }
        }
      }
    }

    .rule {
      height: 5rem;
      line-height: 5rem;
      background-color: $primary;

      .rule-content {
        color: $text-reversal;
        margin: 0 auto;
        text-align: center;
      }
    }


    &.mobile {
      .container {
        width: 100%;
      }
      .banner {
        height: 14rem;
        @include radius-box($sm-radius);

        .banner-content {
          .title {
            margin-top: 3rem;
            margin-bottom: 2rem;
            font-size: $font-size-h1;
          }

          .email-me {
            width: 8rem;
            line-height: 3rem;
          }
        }
      }

      .module {
        margin: 0 auto;
        margin-top: 1rem;

        .module-list {
          flex-direction: column;

          > .item {
            width: 100%;
            height: auto;
            margin-right: 0;
            margin-bottom: 1rem;

            > .icon {
              margin-bottom: -0.5em;
            }
          }
        }
      }

      .step {
        padding: 0;
        background-color: transparent;

        .step-content {
          width: 100%;

          .step-list {
            padding: 0;
            flex-direction: column;

            .item {
              width: 100%;
              height: auto;
              margin-bottom: 1rem;
              padding-bottom: 0;
              background-color: $module-bg;
            }
          }
        }
      }

      .rule {
        height: auto;
        line-height: 3rem;
        @include radius-box($sm-radius);

        .rule-content {
          width: 100%;
          padding: 1rem;
          text-align: left;
          text-indent: 2em;

          > .text {
            margin: 0;
          }
        }
      }
    }
  }
</style>
