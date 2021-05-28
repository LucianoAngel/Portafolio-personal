<template>
  <div>
    <b-navbar toggleable="lg" type="light" variant="light">
      <b-navbar-brand href="/">Portafolio Personal</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item exact>
						<b-img v-bind="{ width: 35, height: 35, class:'mr-1' }" :src="require('../assets/gmail2.png')" alt="Telegram"></b-img>
            ragadurana@uvm.edu.ve</b-nav-item
          >
          <b-nav-item href="https://t.me/Angellucianot" target="_blank" exact>
						<b-img v-bind="{ width: 35, height: 35 }" :src="require('../assets/telegram.png')" alt="Telegram"></b-img>
            @Angellucianot</b-nav-item
          >
          <b-nav-item href="https://github.com/LucianoAngel" target="_blank" exact>
						<b-img v-bind="{ width: 65, height: 35 }" :src="require('../assets/github.gif')" alt="Git Hub"></b-img>
            github.com/LucianoAngel
					</b-nav-item
          >
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: "Navbar",
};
</script>
