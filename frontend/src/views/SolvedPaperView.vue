<template>
  <Header />
  <PreviousYearQuestionPaper />
  <faq/>



  <Footer />
</template>

<script>
import Header from "@/components/Homepage/HeaderSec.vue";
import Footer from "@/components/Homepage/FooterSec.vue";
import faq from'@/components/SolvedPaper/FAQ.vue';
import PreviousYearQuestionPaper from 'D:/pre-treeproject/trehousingpublications/frontend/src/components/SolvedPaper/PreviousYearQuestionPaper.vue';




export default {
  name: "SolvedPaperView",
  components: {
    Header,
    faq,
    PreviousYearQuestionPaper,
    
   

    Footer,
  },
};
</script>

<style></style>
