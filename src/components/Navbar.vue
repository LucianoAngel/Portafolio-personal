<template>
    <div>
        <b-navbar toggleable="lg" type="light" variant="light">

        <b-navbar-brand href="/">Portafolio Personal</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

         <b-collapse id="nav-collapse" is-nav>

             <b-navbar-nav>
                <b-nav-item exact> <b-avatar icon="envelope" variant="info"></b-avatar> ragadurana@uvm.edu.ve</b-nav-item>
                <b-nav-item exact> <b-avatar icon="telephone" variant="info"></b-avatar> 04247750438</b-nav-item>
                <b-nav-item exact ><b-avatar icon="share-fill" variant="info"></b-avatar> github.com/LucianoAngel</b-nav-item>
            </b-navbar-nav>

         </b-collapse>

        </b-navbar>

    </div>
</template>

<script>
export default {
    name:'Navbar'
}
</script>