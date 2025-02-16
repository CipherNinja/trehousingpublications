<template>
  <main>
    <Header />
    <div style="display: flex; flex-direction: row;">
      <div>
        <TreFourZero />
        <PyqOverview />
        <TextTable/>
        <Notification />
        <BiharSyllabusComponent/>
        <PyqSyPdf />
      </div>
    <PyqRightSection/>
    </div>
    <Footer />
  </main>
</template>

<script>
import Header from "@/components/Homepage/HeaderSec.vue";
import Footer from "@/components/Homepage/FooterSec.vue";
import Notification from "@/components/PYQ/NotificationPanel.vue";
import PyqSyPdf from "@/components/PYQ/PyqSyPdf.vue";
import BiharSyllabusComponent from "@/components/PYQ/BiharSyllabusComponent.vue";
import TextTable from "@/components/PYQ/TextTable.vue";
import TreFourZero from "@/components/PYQ/TreFourZero.vue";
import PyqOverview from '@/components/PYQ/PyqOverview.vue';
import PyqRightSection from "@/components/PYQ/PyqRightSection.vue";

export default {
  name: "SyllabusView",
  components: {
    Header,
    TreFourZero,
    PyqRightSection,
    Notification,
    PyqSyPdf,
    BiharSyllabusComponent,
    TextTable,
    PyqOverview,
    Footer,
  },
};
</script>