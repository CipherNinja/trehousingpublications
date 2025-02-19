<template>
  <div class="container">
    <!-- Header Section -->
    <h2 class="text-h">BPSC Previous Year Question Papers</h2>
    <p class="text-gray">
      IBPS is a self-governing recruitment body that conducts recruitment in various banking organizations in India.
      IBPS RRB Scale 3 exam is a Group A post. It is one of the most important bank examinations and is quite popular among all aspirants.
      We are providing IBPS RRB Scale 3 memory-based question papers which will help you prepare strategically.
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
        "IBPS RRB Scale 3 Papers",
        "SSC CGL Previous Year Papers",
        "UPSC Civil Services Papers",
        "Railway NTPC Previous Papers",
        "State PCS Exam Papers"
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
/* ✅ Main Container - Fully Responsive */
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

/* ✅ Responsive Typography */
.text-h, .text-o {
  font-weight: bold;
  font-size: 2rem;
  text-align: left;
  margin-bottom: 16px;
  padding-left: 5%;
}

.text-gray {
  color: #6c757d;
  font-size: 1.1rem;
  text-align: left;
  padding-left: 5%;
  line-height: 1.6;
}

/* ✅ Responsive Grid Layout */
.papers-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
  padding: 10px 5%;
}

/* ✅ Paper Card Design */
.paper-card {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  max-width: 350px;
  height: 65px;
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

/* ✅ Bottom Gradient */
.paper-card::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: linear-gradient(to right, #00008b, #0044cc);
  border-bottom-left-radius: 8px;
  border-bottom-right-radius: 8px;
}

/* ✅ Paper Title */
.title {
  color: #007bff;
  font-size: 1rem;
  font-weight: bold;
}

/* ✅ Arrow Symbol */
.arrow-symbol-container {
  position: relative;
  display: inline-block;
}

.arrow-symbol {
  font-size: 20px;
  color: blue;
  font-weight: bold;
  cursor: pointer;
}

.arrow-symbol-container:hover .arrow-symbol {
  color: black;
}

/* ✅ Yellow Circle on Hover */
.arrow-symbol-container:hover::before {
  content: '';
  position: absolute;
  top: -4px;
  left: -4px;
  width: 28px;
  height: 28px;
  background-color: yellow;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.arrow-symbol-container:hover .arrow-symbol {
  position: relative;
  z-index: 1;
}

/* ✅ RESPONSIVENESS 🔹 */
@media (max-width: 1024px) {
  .text-h, .text-o, .text-gray {
    padding-left: 3%;
  }
  
  .papers-container {
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    padding-left: 3%;
    padding-right: 3%;
  }

  .paper-card {
    max-width: 100%;
  }
}

@media (max-width: 768px) {
  .text-h, .text-o {
    font-size: 1.7rem;
  }

  .text-gray {
    font-size: 1rem;
  }

  .papers-container {
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 15px;
  }

  .paper-card {
    height: 60px;
    padding: 10px;
  }

  .title {
    font-size: 1rem;
  }

  .arrow-symbol {
    font-size: 18px;
  }
}

@media (max-width: 480px) {
  .text-h, .text-o {
    font-size: 1.5rem;
  }

  .text-gray {
    font-size: 0.9rem;
    padding-left: 2%;
  }

  .papers-container {
    grid-template-columns: 1fr;
    padding-left: 2%;
    padding-right: 2%;
  }

  .paper-card {
    height: 55px;
    padding: 8px;
  }

  .title {
    font-size: 0.9rem;
  }

  .arrow-symbol {
    font-size: 16px;
  }
}
</style>
