<template>
    <div>
    
      <!-- Esports Training Section Start -->
      <div class="container mx-auto mt-20 pt-8 text-center">
        <!-- Heading and Hero Image -->
        <h1 class="text-4xl lg:text-5xl font-extrabold text-primary mb-6 animate-fadeIn">Unleash Your Esports Potential</h1>
        <p class="text-xl text-gray-600 mb-10 animate-fadeIn delay-300">
          Dive into essential skills and strategies designed to elevate your competitive edge in esports. Train like the pros with insights on teamwork, adaptability, and peak performance.
        </p>
  
        <div class="flex flex-col lg:flex-row items-center lg:space-x-16">
          <!-- Video Thumbnail with Play Button -->
          <div class="w-full lg:w-1/2 mb-8 lg:mb-0 relative group">
            <img
              src="/images/others/about-thumb.png"
              alt="Esports Training"
              class="rounded-lg shadow-lg transition-transform transform hover:scale-105"
              style="filter: brightness(0.9);"
            />
            <CoolLightBox :items="items" :index="index" @close="index = null"></CoolLightBox>
            <div
              @click="index = 0"
              class="absolute inset-0 flex justify-center items-center bg-black bg-opacity-40 cursor-pointer opacity-0 group-hover:opacity-100 transition-opacity duration-300"
            >
              <i class="icofont-ui-play text-white text-6xl"></i>
            </div>
          </div>
  
          <!-- Training Tips Section -->
          <div class="w-full lg:w-1/2 space-y-6">
            <div
              v-for="section in sections"
              :key="section.title"
              class="p-6 bg-gradient-to-r from-blue-500 to-indigo-500 text-white rounded-lg shadow-lg transform transition-transform hover:scale-105 animate-fadeIn"
            >
              <div class="flex items-center mb-4">
                <span class="text-3xl mr-4">🚀</span>
                <h3 class="text-2xl font-bold uppercase">{{ section.title }}</h3>
              </div>
              <p class="leading-relaxed text-lg">{{ section.content }}</p>
            </div>
          </div>
        </div>
      </div>
      <!-- Esports Training Section End -->
    </div>
  </template>
  
  <script>
  import CoolLightBox from "vue-cool-lightbox";
  import "vue-cool-lightbox/dist/vue-cool-lightbox.min.css";
  
  export default {
    components: {
      CoolLightBox,
    },
    data() {
      return {
        items: [
          {
            src: "https://www.youtube.com/watch?v=STko8mdMoNg",
          },
        ],
        index: null,
        sections: [
          {
            title: "Strategic Mastery & Teamwork",
            content:
              "Gain an edge by mastering game mechanics and team strategies. Sharpen communication, anticipate moves, and learn how to sync seamlessly with your team for unstoppable gameplay.",
          },
          {
            title: "Skill Optimization",
            content:
              "Push your limits! Set clear goals, maintain a consistent practice schedule, and refine your skills through feedback. Experiment with strategies to find your unique style and edge.",
          },
          {
            title: "Peak Physical and Mental Fitness",
            content:
              "Stay sharp and focused with balanced routines. Prioritize sleep, nutrition, and regular exercise to keep your mind and body prepared for intense gameplay and rapid decision-making.",
          },
          {
            title: "Adaptability and Resilience",
            content:
              "In the dynamic world of esports, adaptability is crucial. Embrace change, remain calm under pressure, and learn to turn setbacks into stepping stones to come back stronger every time.",
          },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  .fixed {
    position: fixed;
    width: 100%;
    top: 0;
    background-color: rgba(0, 0, 0, 0.85);
  }
  
  .bg-primary {
    background-color: #4c51bf;
  }
  
  .text-primary {
    color: #4c51bf;
  }
  
  .animate-fadeIn {
    animation: fadeIn 1s ease-out forwards;
  }
  
  .shadow-lg {
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.25);
  }
  </style>
  