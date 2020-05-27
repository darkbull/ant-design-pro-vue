<template>
  <div>
    <a-card :bordered="false">
      <a-menu v-model="current" mode="horizontal">
        <a-menu-item key="mail">
          <a-icon type="mail" /> Navigation One
        </a-menu-item>
        <a-menu-item key="app" disabled>
          <a-icon type="appstore" /> Navigation Two
        </a-menu-item>
        <a-sub-menu key="submenu">
          <span slot="title">
            <a-icon type="setting" /> Sub Menu
          </span>
          <a-menu-item-group title="item1">
            <a-menu-item key="xx"> Option 1 </a-menu-item>
            <a-menu-item key="xx2"> Option 2 </a-menu-item>
          </a-menu-item-group>
          <a-menu-item-group title="item2">
            <a-menu-item key="submenu:3"> Option 3 </a-menu-item>
            <a-menu-item key="submenu:4"> Option 4 </a-menu-item>
          </a-menu-item-group>
        </a-sub-menu>
        <a-menu-item key="go">
          <a href="http://www.baidu.com"> Baidu </a>
        </a-menu-item>
      </a-menu>
    </a-card>

    <a-divider></a-divider>

    <a-card :bordered="false">
      <a-menu mode="inline" style="width:256px" :defaultOpenKeys="['m1']" :defaultSelectedKeys="['sub:1']" @click="handleClick">
        <a-sub-menu key="m1">
          <span slot="title">
            <a-icon type="mail" /> Nav One
          </span>
          <a-menu-item-group>
            <span slot="title">
              <a-icon type="appstore" /> Item -1
            </span>
            <a-menu-item key="sub:1">Option 1</a-menu-item>
            <a-menu-item key="sub:2">Option 2</a-menu-item>
          </a-menu-item-group>
          <a-menu-item-group title="Item -2">
            <a-menu-item key="sub:3">Option 3</a-menu-item>
            <a-menu-item key="sub:4">Option 4</a-menu-item>
          </a-menu-item-group>
        </a-sub-menu>

        <a-sub-menu key="m2">
          <span slot="title">
            <a-icon type="appstore" /> Nav Two
          </span>
          <!-- <a-sub-menu> -->
          <a-menu-item key="m2:1">Option 5</a-menu-item>
          <a-menu-item key="m2:2">Option 6</a-menu-item>
          <a-sub-menu title="SubMenu">
            <a-menu-item key="m2:3">Option 7</a-menu-item>
            <a-menu-item key="m2:4">Option 8</a-menu-item>
          </a-sub-menu>
          <!-- </a-sub-menu> -->
        </a-sub-menu>

        <a-sub-menu key="m3">
          <span slot="title">
            <a-icon type="setting"></a-icon> Nav Three
          </span>
          <a-menu-item key="m3:1">Option 1</a-menu-item>
          <a-menu-item key="m3:2">Option 2</a-menu-item>
          <a-menu-item key="m3:3">Option 3</a-menu-item>

        </a-sub-menu>
      </a-menu>
    </a-card>

  </div>
</template>

<script>
export default {
  data () {
    return {
      current: ['mail']
    }
  },
  methods: {
    handleClick (e) {
      console.log('click:', e)
    }
  }
}
</script>

<style>

</style>
