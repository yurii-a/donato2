<template>
  <navbar
    position="fixed"
    type="primary"
    menu-classes="ml-auto"
  >
    <template>
      <router-link
        v-popover:popover1
        class="navbar-brand"
        to="/presentation"
      >
        My Site Name
      </router-link>
      <el-popover
        ref="popover1"
        popper-class="popover"
        placement="bottom"
        width="200"
        trigger="hover"
      >
        <div class="popover-body">
          Designed by Invision. Coded by Creative Tim
        </div>
      </el-popover>
    </template>
    <template slot="navbar-menu">
      <drop-down
        tag="li"
        title="Sample Dropdown"
      >
        <nav-link class="dropdown-item">
          <i class="now-ui-icons shopping_box" /> Headers
        </nav-link>
      </drop-down>
    </template>
  </navbar>
</template>

<script>
  import { DropDown, Navbar, NavLink } from '@/components';
  import { Popover } from 'element-ui'

  export default {
    name: 'MainNavbar',
    components: {
      DropDown,
      Navbar,
      NavLink,
      [Popover.name]: Popover
    }
  }
</script>

<style scoped>

</style>
