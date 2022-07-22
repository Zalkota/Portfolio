<template>
    <div>

        <Navbar
        />
        <!-- <pdf src="resume.pdf"></pdf> -->
        <TableFrame
        />

        <Footer/>

    </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import TableFrame from "./components/TableFrame.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "Home",
  components: { Navbar, Footer, TableFrame},

};
</script>
