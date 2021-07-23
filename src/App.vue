<template>
  <a-layout id="components-layout-demo-custom-trigger">
    <a-layout-sider v-model="collapsed" :trigger="null" collapsible>
      <div class="logo" />
      <a-menu theme="dark" mode="inline" :default-selected-keys="['1']">
        <a-menu-item key="1">
          <a-icon type="user" />
          <span>nav 1</span>
        </a-menu-item>
        <a-menu-item key="2">
          <a-icon type="video-camera" />
          <span>nav 2</span>
        </a-menu-item>
        <a-menu-item key="3">
          <a-icon type="upload" />
          <span>nav 3</span>
        </a-menu-item>
      </a-menu>
    </a-layout-sider>
    <a-layout>
      <a-layout-header style="background: #fff; padding: 0">
        <a-icon
            class="trigger"
            :type="collapsed ? 'menu-unfold' : 'menu-fold'"
            @click="() => (collapsed = !collapsed)"
        />
      </a-layout-header>
      <a-layout-content
          :style="{ margin: '24px 16px', padding: '24px', background: '#fff', minHeight: '280px' }"
      >
        Content
        <div>
          <a-avatar icon="user" />
          <a-avatar>
            <a-icon slot="icon" type="user" />
          </a-avatar>
          <a-avatar>U</a-avatar>
          <a-avatar>USER</a-avatar>
          <a-avatar src="https://zos.alipayobjects.com/rmsportal/ODTLcjxAfvqbxHnVXCYX.png" />
          <a-avatar style="color: #f56a00; backgroundColor: #fde3cf">
            U
          </a-avatar>
          <a-avatar style="backgroundColor:#87d068" icon="user" />
        </div>
        <div>
          <a-badge :count="99">
            <a href="#" class="head-example" />
          </a-badge>
          <a-badge :count="100">
            <a href="#" class="head-example" />
          </a-badge>
          <a-badge :count="99" :overflow-count="10">
            <a href="#" class="head-example" />
          </a-badge>
          <a-badge :count="1000" :overflow-count="999">
            <a href="#" class="head-example" />
          </a-badge>
        </div>
        <a-skeleton avatar :paragraph="{ rows: 4 }" />
        <div>
          <a-spin size="small" />
          <a-spin />
          <a-spin size="large" />
        </div>
      </a-layout-content>
    </a-layout>
  </a-layout>
</template>


<script>

export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      collapsed: false,
    };
  },
};
</script>
<style>
#components-layout-demo-custom-trigger .trigger {
  font-size: 18px;
  line-height: 64px;
  padding: 0 24px;
  cursor: pointer;
  transition: color 0.3s;
}

#components-layout-demo-custom-trigger .trigger:hover {
  color: #1890ff;
}

#components-layout-demo-custom-trigger .logo {
  height: 32px;
  background: rgba(255, 255, 255, 0.2);
  margin: 16px;
}
</style>
