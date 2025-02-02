<template>
  <div class="min-h-screen">
    <!-- Navbar -->
    <nav :class="[
      'fixed w-full z-50 transition-all duration-300',
      isScrolled
        ? 'py-4 bg-white/10 backdrop-blur-md border-b border-white/10 shadow-lg'
        : 'py-12'
    ]">
      <div class="navcontainer mx-auto flex justify-between items-start">
        <!-- Logo and Know image aligned left -->
        <div class="flex flex-col items-start">
          <img src="/src/assets/Logo.svg" alt="Logo" class="h-16 w-auto">
          <img src="/src/assets/Know.png" alt="Know Logo" class="h-12 w-auto mt-2 px-6">
        </div>

        <!-- Navigation Links aligned top -->
        <div class="flex mt-6 space-x-12">
          <!-- Use conditional classes for link text color -->
          <a href="#"
            :class="[isScrolled ? 'text-black hover:text-gray-500' : 'text-white hover:text-gray-300', 'text-xl font-light']">
            Home
          </a>
          <a href="#"
            :class="[isScrolled ? 'text-black hover:text-gray-500' : 'text-white hover:text-gray-300', 'text-xl font-light']">
            About
          </a>
          <a href="#"
            :class="[isScrolled ? 'text-black hover:text-gray-500' : 'text-white hover:text-gray-300', 'text-xl font-light']">
            Blog
          </a>
          <a href="#"
            :class="[isScrolled ? 'text-black hover:text-gray-500' : 'text-white hover:text-gray-300', 'text-xl font-light']">
            News
          </a>
          <a href="#"
            :class="[isScrolled ? 'text-black hover:text-gray-500' : 'text-white hover:text-gray-300', 'text-xl font-light']">
            Contact Us
          </a>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative h-screen">
      <!-- Background Image with Overlay -->
      <div class="absolute inset-0 bg-cover bg-center" style="background-image: url('/src/assets/hero-bg.png');">
        <div class="absolute inset-0" style="background-color: rgba(30, 35, 50, 0.8);"></div>
      </div>

      <!-- Content -->
      <div class="relative container mx-auto h-full flex flex-col items-center justify-center text-white">
        <h1 class="text-[70px] font-light text-center leading-tight mb-8 mt-20"
          style="font-family: 'Merriweather', serif;">
          Hey Doc! What's the best<br />
          food for my pet?
        </h1>



        <!-- Red Ribbon -->
        <div class="relative bg-red-600 transform -skew-x-[35deg] py-2 px-8 mb-6 mt-2 
            before:content-[''] before:absolute before:top-0 before:right-0 before:bottom-0 before:left-[-5px] 
            before:bg-red-600 before:transform before:skew-x-[50deg] before:-z-10">
          <span class="block transform skew-x-[35deg] text-2xl font-light relative">
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
      <div class="container mx-auto flex gap-4">
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
        <div class="grid grid-cols-2 gap-4 mb-20">
          <div class="flex flex-col justify-start">
            <h2 class="text-3xl font-medium mb-4 whitespace-nowrap" style="font-family: 'Merriweather'">
              Evaluate Account Creation Process</h2>
            <p class="mb-8 max-w-[30rem]">
              We encourage every prospective subscriber to our Pet Nutritional
              Technology service offering to set aside a few minutes to create an
              account and complete the process through purchase and review of
              an Optimal Diet Plan. <br>
              <br>
              Please review the 3 steps below with respect to user ID and purchase instructions. To maximize this trial,
              please complete with accuracy the Pet Information questionnair.
            </p>
            <div class="flex justify-center max-w-[30rem]">
              <button class="bg-[#F8B179] text-gray-600 px-8 py-3 rounded w-fit self-center font-bold"
                style="font-family: 'Inter', sans-serif;">
                Create Account
              </button>
            </div>
          </div>
          <div>
            <img src="/src/assets/laptop-mockup.png" alt="Laptop Mockup" class="w-full" />
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
                <!-- Text area with auto adjustable height -->
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
                <!-- Text area with auto adjustable height -->
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
                <!-- Text area with auto adjustable height -->
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
      <div class="absolute inset-0 bg-cover bg-center" style="background-image: url('/src/assets/vet-bg.png');">
      </div>

      <!-- Content -->
      <div class="relative container mx-auto text-black">
        <h2 class="text-4xl font-bold text-center mb-4"
          style="font-family: 'Merriweather', serif; text-shadow: 2px 2px 6px rgba(0, 0, 0, 0.3);">
          Request a Subscription Agreement
        </h2>
        <p class="text-center mb-12 text-xl font-light" style="font-family: 'Inter', sans-serif;">
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
      isScrolled: false
    }
  },
  methods: {
    handleSubmit() {
      console.log('Form submitted:', this.formData)
    },
    handleScroll() {
      const heroHeight = window.innerHeight;
      this.isScrolled = window.scrollY > heroHeight - 100;
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
  padding: 0 3rem;
}

.navcontainer {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 3rem;
}

/* Add any additional custom styles here */
</style>