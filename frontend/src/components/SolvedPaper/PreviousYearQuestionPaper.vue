<template>
  <div class="p-6 max-w-6xl mx-auto">
    <!-- Header Section -->
    <h2 class="text-h">BPSC Previous Year Question Papers</h2>
    <p class="text-gray">
      IBPS is a self-governing recruitment body, conducts recruitment in various banking organizations in India. IBPS RRB Scale 3 exam is a Group A post. IBPS RRB Scale 3 exam is one of the most important bank examinations and quite popular among all the aspirants. IBPS RRB Scale 3 is a single-day exam, and the examination process is quite simple. ixamBee is offering IBPS RRB Scale 3 previous year question papers with solutions that will assist you in attaining an idea about what to expect from the IBPS RRB Scale 3 exam. We are providing IBPS RRB Scale 3 memory-based question papers which will surely help you in making a proper and productive strategy. Practice the IBPS RRB Scale 3 previous year papers and get one step closer to your dream job.
    </p>
    <p class="text-sec">
      While taking the previous year's papers for IBPS RRB Scale 3 Officer if you feel a need for further guidance, then ixamBee offers an IBPS RRB Scale 3 online course which has been curated by our expert faculty. Moreover, the IBPS RRB Scale 3 Officer study material is prepared keeping the latest exam pattern and syllabus in mind.
    </p>

    <!-- Other Papers Section -->
    <h3 class="text-o">Other Previous Year Papers For You</h3>
    <div class="papers-container">
      <div 
        v-for="(paper, index) in papers" 
        :key="index" 
        class="paper-card"
        @click="handleClick(paper)">
        <span class="title">{{ paper }}</span>
        <span class="arrow-symbol-container">
          <span class="arrow-symbol">⟩</span>
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PreviousYearQuestionPaper",
  data() {
    return {
      papers: [
        "BPSC Previous Year Papers",
        "BPSC Previous Year Papers",
        "BPSC Previous Year Papers",
        "BPSC Previous Year Papers",
        "BPSC Previous Year Papers",
        "BPSC Previous Year Papers"
      ]
    };
  },
  methods: {
    handleClick(paper) {
      console.log(`Clicked on: ${paper}`);
    }
  }
};
</script>

<style scoped>
body {
  background-color: #f8f9fa;
}

.text-h, .text-o {
  font-weight: bolder;
  font-size: larger;
  text-align: left;
  margin-bottom: 16px;
  padding-left: 70px;
}

.text-gray {
  color: #6c757d;
  font-size: 16px;
  text-align: left;
  padding-left: 70px;
}

.text-sec {
  color: #6c757d;
  font-size: 16px;
  text-align: left;
  padding-left: 70px;
}

.papers-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  justify-content: left;
  padding-left: 70px;
}

.paper-card {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  max-width: 320px;
  height: 60px;
  padding: 12px;
  border-radius: 8px;
  border: 1px solid #ddd;
  background: #fff;
  cursor: pointer;
  transition: all 0.3s ease;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  position: relative;
}

.paper-card:hover {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.title {
  color: #007bff;
  font-size: 16px;
  font-weight: bold;
}

.arrow-symbol-container {
  position: relative;
  display: inline-block;
}

.arrow-symbol {
  font-size: 18px;
  color: blue;
  font-weight: bold;
  cursor: pointer;
}

@media (max-width: 768px) {
  .text-h, .text-o {
    font-size: 1.25rem;
    padding-left: 20px;
  }

  .text-gray, .text-sec {
    font-size: 0.9rem;
    padding-left: 20px;
  }

  .papers-container {
    padding-left: 20px;
  }

  .paper-card {
    max-width: 100%;
  }
}
</style>
