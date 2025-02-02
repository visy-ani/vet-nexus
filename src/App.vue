<template>
  <div class="min-h-screen">
    <!-- Navbar -->
    <nav :class="[
      'navbar fixed w-full z-50 transition-all duration-300',
      isScrolled ? 'py-4 bg-[#2D3250] shadow-lg' : 'py-12'
    ]">
      <div class="navcontainer mx-auto flex justify-between items-start px-4">
        <!-- Logo and Know image aligned left -->
        <div class="flex flex-col items-start">
          <img src="/src/assets/Logo.svg" alt="Logo" class="h-12 w-auto sm:h-16">
          <img src="/src/assets/Know.png" alt="Know Logo" class="h-8 w-auto mt-2 px-4 sm:h-12 sm:px-6">
        </div>

        <!-- Mobile Menu Button -->
        <button @click="toggleMenu" class="block lg:hidden mt-6">
          <svg xmlns="http://www.w3.org/MPH" viewBox="0 0 24 24" fill="none" stroke="currentColor"
            :class="[isScrolled ? 'text-black' : 'text-white']" class="w-6 h-6">
            <path v-if="!isMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16" />
            <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>

        <!-- Desktop Navigation -->
        <div class="hidden lg:flex mt-6 space-x-12">
          <a v-for="link in navLinks" :key="link" href="#" :class="[
            isScrolled ? 'text-white hover:text-gray-500' : 'text-white hover:text-gray-300',
            'text-xl font-light'
          ]">
            {{ link }}
          </a>
        </div>

        <!-- Mobile/Tablet Menu -->
        <div v-show="isMenuOpen"
          class="lg:hidden absolute top-full left-0 w-full bg-white/95 backdrop-blur-md shadow-lg">
          <div class="flex flex-col py-4">
            <a v-for="link in navLinks" :key="link" href="#"
              class="px-6 py-3 text-white hover:bg-gray-100 text-lg border-b border-gray-100 last:border-none"
              @click="closeMenu">
              {{ link }}
            </a>
          </div>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative h-screen">
      <!-- Background Image with Overlay -->
      <div class="absolute inset-0 bg-center bg-[#2D3250]">
        <div class="absolute inset-0 bg-cover bg-[url('/src/assets/hero-bg.png')]"></div>
      </div>

      <!-- Content -->
      <div class="relative container mx-auto h-full flex flex-col items-center justify-center text-white">
        <h1
          class="text-3xl sm:text-4xl md:text-5xl lg:text-[70px] font-light text-center leading-tight mb-4 sm:mb-6 lg:mb-8 mt-10 sm:mt-16 lg:mt-20"
          style="font-family: 'Merriweather', serif;">
          Hey Doc! What's the best<br class="hidden sm:block" />
          <span class="sm:hidden"> </span>food for my pet?
        </h1>



        <!-- Red Ribbon -->
        <div class="ribbon">
          <span class="ribbon-text">
            Science + Data + Genetics = Optimal Pet Diet
          </span>
        </div>







        <p class="text-center text-lg mb-14 max-w-xl">
          Watch the full walkthrough of our app's features and see how it
          revolutionizes pet nutrition using science, data, and genetics.
        </p>

        <button class="bg-[#F4C095] text-gray-800 px-8 py-3 rounded text-lg">
          Review Client Experience & Subscriber Web Portal Features
        </button>
      </div>
    </section>

    <!-- Database Section -->
    <section class="py-6 bg-white">
      <div class="container mx-auto flex gap-4 databaseSection">
        <!-- Left Side - Phone Mockup -->
        <div class="auto">
          <img src="/src/assets/phone-mockup.png" alt="Pet Health Profile Mobile App" class="rounded-3xl" />
        </div>

        <!-- Right Side - Content -->
        <div class="w-3/4 space-y-8 pt-8">
          <div>
            <h2 class="text-3xl font-bold mb-3">
              Pet Industry's Largest Pet Nutritional Database
            </h2>
            <p class="text-gray-600 text-sm leading-relaxed">
              We have mined and documented the nutritional content from over 10,000 canine pet diets in
              today's marketplace. Each diet is graded with respect to the percentage of water, protein,
              carbohydrates, fats, vitamins, and minerals, and fillers such as corn, corn gluten meal, wheat,
              soy, synthetic preservatives, and animal fat.
            </p>
          </div>

          <div>
            <h2 class="text-3xl font-bold mb-3">
              Proprietary Data Collection Process
            </h2>
            <p class="text-gray-600 text-sm leading-relaxed">
              Each client of a companion pet veterinary practice is encouraged to complete a Pet Health Profile.
              This 5-7-minute questionnaire serves two purposes: First, it collects pet health data to identify up
              to five pet diets on the market that meet the pet's nutritional needs. Second, it helps uncover
              symptoms of potential food allergies and existing health conditions that an Optimal Diet and/or
              their veterinarian can address.
            </p>
          </div>

          <div>
            <h2 class="text-3xl font-bold mb-3">
              Lifetime Optimal Diet Plan™
            </h2>
            <p class="text-gray-600 text-sm leading-relaxed">
              Every veterinarian believes optimal pet nutrition is the cornerstone in both enriching and
              prolonging the lives of companion pets. Vetnexus Intelligent pet nutrition technology combines
              science, data, and a genetic profile in determining an optimal diet plan over the lifetime of each
              pet, under the supervision of the pet owner's veterinarian.
            </p>
          </div>
        </div>

      </div>
    </section>

    <!-- Account Section -->
    <section class="py-20 bg-[#2D3250] text-white">
      <div class="container mx-auto">
        <!-- Top Content -->
        <div :class="['accountGrid flex flex-col sm:grid grid-cols-2 gap-4 mb-20']">
          <div class="account-section flex flex-col justify-start">
            <h2 class="account-heading text-3xl font-medium mb-4 whitespace-nowrap"
              :style="{ fontFamily: 'Merriweather' }">
              Evaluate Account Creation Process
            </h2>
            <p class="account-text mb-8 max-w-[30rem]">
              We encourage every prospective subscriber to our Pet Nutritional
              Technology service offering to set aside a few minutes to create an
              account and complete the process through purchase and review of
              an Optimal Diet Plan. <br>
              <br>
              Please review the 3 steps below with respect to user ID and purchase instructions. To maximize this trial,
              please complete with accuracy the Pet Information questionnair.
            </p>
            <div class="flex justify-center max-w-[30rem]">
              <button
                class="create-account-btn bg-[#F8B179] text-gray-600 px-8 py-3 rounded w-fit self-center font-bold"
                :style="{ fontFamily: 'Inter, sans-serif' }">
                Create Account
              </button>
            </div>
          </div>
          <div>
            <img src="/src/assets/laptop-mockup.png" alt="Laptop Mockup" class="w-full">
          </div>
        </div>

        <!-- Steps Section -->
        <h2 class="text-4xl font-normal text-center mb-12" style="font-family: 'Merriweather', serif;">
          3 Simple Steps to Get Started
        </h2>

        <div class="w-full">
          <div class="max-w-7xl mx-auto">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-12">
              <!-- Step 1 -->
              <div class="flex flex-col items-center">
                <div class="flex flex-col text-center h-[100px]">
                  <h2 class="text-xl md:text-2xl font-semibold mb-2">
                    Step 1) Create Account Page
                  </h2>
                  <p class="mb-4">
                    User ID: Use <span class="text-[#ED2324]">97Nort</span> as your user ID
                  </p>
                </div>
                <!-- Image -->
                <div class="relative w-full md:max-w-4xl mx-auto aspect-video">
                  <img src="/src/assets/step1.png" alt="Create Account Page"
                    class="w-full h-full object-cover rounded-xl shadow-lg border-2 border-white" />
                </div>

              </div>

              <!-- Step 2 -->
              <div class="flex flex-col items-center max-w-[100%]">
                <div class="flex flex-col text-center h-[100px]">
                  <h2 class="text-xl md:text-2xl font-semibold mb-2">
                    Step 2) Diet Plan Services Page
                  </h2>
                  <p class="mb-4 max-w-[80%] self-center">
                    Select <span class="text-[#ED2324]">Optimal Diet Plan</span> and
                    <span class="text-[#ED2324]">$99</span> as preferred payment
                  </p>
                </div>
                <!-- Image -->
                <div class="relative w-full md:max-w-4xl mx-auto aspect-video">
                  <img src="/src/assets/step2.png" alt="Create Account Page"
                    class="w-full h-full object-cover rounded-xl shadow-lg border-2 border-white" />
                </div>
              </div>

              <!-- Step 3 -->
              <div class="flex flex-col items-center">
                <div class="flex flex-col text-center h-[100px]">
                  <h2 class="text-xl md:text-2xl font-semibold mb-2">
                    Step 3) Shopping Cart Page
                  </h2>
                  <p class="mb-4">
                    Use <span class="text-[#ED2324]">NDVC100</span> as the promo code
                  </p>
                </div>
                <!-- Image -->
                <div class="relative w-full md:max-w-4xl mx-auto aspect-video">
                  <img src="/src/assets/step3.png" alt="Step 3"
                    class="w-full h-[85%] rounded-xl shadow-lg border-2 border-white" />

                </div>

              </div>
            </div>
          </div>
        </div>

      </div>
    </section>

    <!-- Subscription Section -->
    <section class="relative py-20">
      <!-- Background Image with Overlay -->
      <div class="absolute inset-0 bg-cover bg-center bg-[url('/src/assets/vet-bg.png')]">
      </div>

      <!-- Content -->
      <div class="relative container mx-auto text-black">
        <h2 class="Subscription-heading text-4xl font-bold text-center mb-4"
          style="font-family: 'Merriweather', serif; text-shadow: 2px 2px 6px rgba(0, 0, 0, 0.3);">
          Request a Subscription Agreement
        </h2>
        <p class="Subscription-subheading text-center mb-12 text-xl font-light"
          style="font-family: 'Inter', sans-serif;">
          To receive your subscription agreement, please fill out the form below<br />
          and submit your request. We'll get in touch with you shortly!
        </p>

        <!-- Form -->
        <div class="max-w-md mx-auto bg-[#2D3250] p-8 rounded-lg border-4 border-[#F8B179] text-white">
          <div class="flex justify-center items-center text-2xl font-bold">
            <img src="/src/assets/Logo.svg" alt="Logo" class="h-16 w-auto">
          </div>
          <form @submit.prevent="handleSubmit" class="space-y-2">
            <div>
              <label class="block mb-1">Name:</label>
              <input v-model="formData.name" type="text" class="w-full px-4 py-2 rounded bg-white/10" />
            </div>
            <div>
              <label class="block mb-1">Name of Veterinary Practice:</label>
              <input v-model="formData.practice" type="text" class="w-full px-4 py-2 rounded bg-white/10" />
            </div>
            <div>
              <label class="block mb-1">Website Address:</label>
              <input v-model="formData.website" type="text" class="w-full px-4 py-2 rounded bg-white/10" />
            </div>
            <div>
              <label class="block mb-1">Email Address:</label>
              <input v-model="formData.email" type="email" class="w-full px-4 py-2 rounded bg-white/10" />
            </div>
            <button type="submit"
              class="w-full bg-[#F8B179] mt-8 text-gray-800 p-3 rounded hover:bg-[#f3b27b] transition-colors uppercase font-normal"
              style="font-family: 'Inter', sans-serif;">
              PLEASE SEND SUBSCRIPTION AGREEMENT
            </button>

          </form>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      formData: {
        name: '',
        practice: '',
        website: '',
        email: ''
      },
      isScrolled: false,
      isMenuOpen: false,
      navLinks: ['Home', 'About', 'Blog', 'News', 'Contact Us']
    }
  },
  methods: {
    handleSubmit() {
      console.log('Form submitted:', this.formData)
    },
    handleScroll() {
      const heroHeight = window.innerHeight; 
      const scrollTriggerPoint = heroHeight / 5;
      this.isScrolled = window.scrollY > scrollTriggerPoint;
    },
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
    closeMenu() {
      this.isMenuOpen = false;
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  unmounted() {
    window.removeEventListener('scroll', this.handleScroll);
  }
}
</script>


<style>
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}

.account-heading {
  font-size: 1.875rem;
  line-height: 2.25rem;
}

.create-account-btn {
  font-size: 1rem;
}

.navcontainer {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 1rem;

  @media (min-width: 640px) {
    padding: 0 2rem;
  }

  @media (min-width: 1024px) {
    padding: 0 3rem;
  }
}

@media (max-width: 768px) {
  .navbar {
    padding: 0.5rem 0;
  }

  .accountGrid {
    grid-template-rows: repeat(2, minmax(0, 1fr));
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
}

@media (max-width: 640px) {
  h1 {
    line-height: 1.2;
    padding: 0 1rem;
  }

  .databaseSection {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .account-heading {
    font-size: 1.2rem;
  }

  .Subscription-heading {
    font-size: 2rem;
  }

  .Subscription-subheading {
    font-size: 0.9rem;
  }
}

@media (min-width: 641px) and (max-width: 1024px) {
  h1 {
    line-height: 1.3;
    padding: 0 2rem;
  }
}

.ribbon {
  position: relative;
  background-color: #dc2626;
  transform: skewX(-20deg);
  padding: 0.5rem 1.5rem;
  margin-bottom: 1rem;
  margin-top: 0.25rem;
}

.ribbon::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: -3px;
  background-color: #dc2626;
  transform: skewX(30deg);
  z-index: -1;
}

.ribbon-text {
  display: block;
  transform: skewX(20deg);
  font-size: 1.25rem;
  font-weight: 300;
  white-space: normal;
  padding: 0 0.75rem;
  text-align: center;
}

@media (max-width: 640px) {
  .ribbon {
    padding: 0.2rem 0.5rem;
    transform: skewX(-15deg);
  }

  .ribbon::before {
    transform: skewX(25deg);
  }

  .ribbon-text {
    font-size: 0.875rem;
    padding: 0 0.25rem;
  }
}

/* Tablets */
@media (min-width: 641px) and (max-width: 1024px) {
  .ribbon {
    padding: 0.3rem 0.75rem;
    transform: skewX(-18deg);
  }

  .ribbon::before {
    transform: skewX(28deg);
  }

  .ribbon-text {
    font-size: 1rem;
  }
}

@media (min-width: 1024px) {
  .ribbon {
    padding: 0.6rem 1.5rem;
    transform: skewX(-25deg);
  }

  .ribbon::before {
    transform: skewX(35deg);
  }

  .ribbon-text {
    font-size: 1.5rem;
    font-weight: 400;
  }
}
</style>