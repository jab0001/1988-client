<template>
    <div class="theme-container">
        <notifications></notifications>
        <Navbar></Navbar>
        <div
                class="sidebar-mask"
                @click="toggleSidebar(false)"
        ></div>

        <Sidebar
                :items="sidebarItems"
                @toggle-sidebar="toggleSidebar"
        >
            <slot
                    name="sidebar-top"
                    slot="top"
            />
            <slot
                    name="sidebar-bottom"
                    slot="bottom"
            />
        </Sidebar>

        <div
                class="custom-layout"
                v-if="$page.frontmatter.layout"
        >
            <component :is="$page.frontmatter.layout"/>
        </div>

        <Home v-else-if="$page.frontmatter.home"/>

        <Page class="custom-page"
                v-else
                :sidebar-items="sidebarItems"
        >
            <slot
                    name="page-top"
                    slot="top"
            />
            <slot
                    name="page-bottom"
                    slot="bottom"
            />
        </Page>

    </div>
</template>
<script>
  import Navbar from './Navbar';
  import Sidebar from '../../node_modules/@vuepress/theme-default/components/Sidebar';
  import Home from '../../node_modules/@vuepress/theme-default/components/Home';
  import Page from '../../node_modules/@vuepress/theme-default/components/Page';
  import {resolveSidebarItems} from '../../node_modules/@vuepress/theme-default/util/index';
  import 'prismjs/themes/prism-tomorrow.css';
  import './styles/theme.styl';

  export default {
    components: {
      Navbar,
      Sidebar,
      Home,
      Page
    },
    data() {
      return {
        isSidebarOpen: false,
      }
    },
    computed: {
      sidebarItems () {
        return resolveSidebarItems(
          this.$page,
          this.$route,
          this.$site,
          this.$localePath
        )
      },
    },
    methods: {
      toggleSidebar (to) {
        this.isSidebarOpen = typeof to === 'boolean' ? to : !this.isSidebarOpen
      }
    }
  }
</script>
<style>
    .theme-content {
        margin-top: 100px;
    }
    .page.custom-page .content{
        margin: 60px 20px 20px;
        max-width: 100%;
    }
    .sidebar{
      font-size: 15px;
      background-color: #fff;
      width: 20rem;
      position: fixed;
      z-index: 10;
      margin: 0;
      top: 3.6rem;
      left: 0;
      bottom: 0;
      box-sizing: border-box;
      border-right: 1px solid #eaecef;
      overflow-y: auto;
    }
    .page{
      padding-left: 20rem;
    }
    .page .theme-default-content{
      margin: 60px 20px 20px;
      padding: 2rem 2.5rem;
      max-width: 100%;
    }
</style>
