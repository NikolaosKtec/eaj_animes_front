<script>
    import {BNavbar,BNavbarBrand,BCollapse,BNavbarNav,BNavbarToggle} from 'bootstrap-vue'
    export default{
        name: 'HeadCommon',
        components:{
            BNavbar, BNavbarBrand, BCollapse, BNavbarNav, BNavbarToggle
        }
    }
</script>
<template>
    <Div>
  <BNavbar toggleable="md" type="dark" variant="dark">
    <B-navbar-brand href="#">
      <img style="width: 130px;" src="../assets/logo_ani_st.png" alt="">
    </B-navbar-brand>

    <B-navbar-toggle target="nav-collapse"></B-navbar-toggle>

    <B-collapse id="nav-collapse" class="container-fluid"  is-nav>
      <B-navbar-nav>
        <B-nav-item href="#">Link</B-nav-item>
        <B-nav-item href="#" disabled>Disabled</B-nav-item>
      </B-navbar-nav>

      <!-- Right aligned nav items -->
      <B-navbar-nav class="">
          <div class="container-fluid mx-0">
            <div class="row">
              <div class="col-10">
                <B-form-input  class=" mr-sm-2 mr-0" placeholder="Search">

                </B-form-input> 
              </div>

              <div class="col-2">
                <B-button size="sm" class=" my-2 my-sm-0" type="submit">
                <span class="material-symbols-outlined">
                    search
                </span>
                </B-button>
              </div>

            </div>
          </div>

        <!-- <B-nav-item-dropdown right> -->
          <!-- Using 'button-content' slot -->
          <!-- <template #button-content>
            <em>User</em>
          </template>
          <B-dropdown-item href="#">Profile</B-dropdown-item>
          <B-dropdown-item href="#">Sign Out</B-dropdown-item>
        </B-nav-item-dropdown> -->
      </B-navbar-nav>
    </B-collapse>
  </BNavbar>
</Div>
</template>