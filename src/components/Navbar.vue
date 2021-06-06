<template>
    <div>
      <b-navbar toggleable="lg" type="light" variant="" fixed="top" class="bg-white nav-bottom-border">
        <b-container>
            <b-navbar-brand href="/">
              <img src="@/assets//logo.png" alt="Adaiyalam" >
               அடையாளம்
            </b-navbar-brand>

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
            <b-collapse id="nav-collapse"  is-nav>
            
              <!-- Left aligned nav items -->

              <b-navbar-nav>
                <!--
                <b-nav-item href="/#/tamil-murai">தமிழ் முறை </b-nav-item>
                -->
             

                   
              </b-navbar-nav>
              
              <!-- Right aligned nav items -->
              <b-navbar-nav class="ml-auto">
                <b-nav-form>
                    <PostCatDrop :category="category"/>
                </b-nav-form>
                <b-nav-item-dropdown right>
                    <!-- Using 'button-content' slot -->
                    <template slot="button-content"><em>User</em></template>
                  
                  
                    <b-dropdown-item href="/#/login">Login</b-dropdown-item>
              
                  
                    <b-dropdown-item href="/#/profile">Profile</b-dropdown-item>

                
                  
          
                      
                  
                </b-nav-item-dropdown>
              </b-navbar-nav>
            </b-collapse>
          </b-container>
      </b-navbar>
    </div>  
</template>


<script>

import PostCatDrop from "./PostCatDrop.vue";  

export default {
  name: 'Navbar',
  components: {  
        PostCatDrop 
  } ,
  data () {
    return {
      category:'',
    }
  },
  methods: {
    getMeal() {
      
    }
  }

};
</script>


<style scoped>

.bg-white {
    background-color: white !important;
}

.nav-bottom-border {
  box-shadow: 0 4px 12px 0 rgba(0, 0, 0, 0.05);
}

/* change navbar background on collapse */
@media (max-width: 768px) {
  nav.navbar {
    background: white;
  }
}

/* change navbar-brand color on hover */
.navbar a.navbar-brand:hover {
  color: red;
}

/* this allows the image to occupy all the padding space of the navbar--brand */
.navbar-brand
{
  padding: 0px;
}

.navbar-brand > img
{
   height: 100%; 
   width: 65px; 
   max-height: 100%; 
   margin: 0 auto; 
}
</style>