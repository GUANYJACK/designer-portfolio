<template>
  <div class="banner-1">
    <!-- NavBar -->
    <nav
      class="container px-6 mx-auto md:flex md:justify-between md:items-center"
    >
      <div class="flex items-center justify-between">
        <div class="relative w-16 h-16">
          <img
            class="rounded-full border border-gray-100 shadow-sm"
            src="https://media.licdn.com/dms/image/v2/D5635AQFp-n-2KbId2A/profile-framedphoto-shrink_400_400/B56Zrc_3sfLQAk-/0/1764644322480?e=1774425600&amp;v=beta&amp;t=GKTaWm_ZEmz5W4b5TiSpW_lgU0OrYyOmro1yXq9O1uY"
            alt="user image"
          />
        </div>
        <!-- Mobile menu button -->
        <div @click="showMenu = !showMenu" class="flex md:hidden">
          <button
            type="button"
            class="text-gray-800 hover:text-gray-400 focus:outline-none focus:text-gray-400"
          >
            <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
              <path
                fill-rule="evenodd"
                d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
              ></path>
            </svg>
          </button>
        </div>
      </div>
      <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
      <ul
        :class="showMenu ? 'flex' : 'hidden'"
        class="flex-col items-end mt-8 space-y-4 md:flex md:space-y-0 md:flex-row md:items-center md:space-x-10 md:mt-0"
      >
        <li class="menu-button"><a href="#">Home</a></li>
        <li class="menu-button"><a href="#work" v-smooth-scroll>Works</a></li>
        <!-- <li class="menu-button">
          <a href="#testimonial" v-smooth-scroll>Testimonials</a>
        </li> -->
        <li class="menu-button"><a href="#about" v-smooth-scroll>About</a></li>
      </ul>
    </nav>
    <!-- End Navbar -->

    <div class="flex items-center">
      <div class="w-11/12 space-y-5 md:space-y-10">
        <h3
          class="hello-button text-gray-700 w-fit md:py-3 md:px-5 py-1 px-2 rounded-lg 3xl:text-3xl 2xl:text-xl lg:text-xl md:text-md text-sm font-semibold font-work_sans"
        >
          👋 你好！Hello！Hola！
        </h3>
        <h1
          class="3xl:text-8xl 2xl:text-7xl xl:text-6xl lg:text-4xl md:text-3xl sm:text-3xl text-xl font-Eczar font-bold leading-tight text-gray-700"
        >
          It's
          <span class="text-black font-semibold">
            {{ profile.name }}
          </span>
          🐷<br />{{ profile.role }}
        </h1>

        <div class="md:flex gap-1 md:gap-10">
          <button class="text-white bg-gray-800 submit-button hidden md:block">
            View My Work
          </button>
          <a
            href="#contact"
            v-smooth-scroll
            class="text-gray-800 border-4 border-gray-800 submit-button mb-5 md:mb-0"
          >
            Contact Me
          </a>
        </div>
      </div>

      <div class="w-8/12 flex justify-end">
        <img
          class="max-h-[800px] w-auto object-contain"
          src="./assets/卡通形象透明正方图.png"
          alt="user image"
        />
      </div>
    </div>
  </div>

  <div class="banner-2 space-y-10 pb-20" id="work">
    <h3 class="heading3 my-5">My Recent Work</h3>
    <div class="card">
      <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-1/2">
        <h4 class="project-title item">Sheepify States</h4>
        <p class="font-work_sans pr-12">
          Designed some empty state screens in kawaii style for the popular
          sheepify app.Tailwind lets you conditionally apply utility classes in
          different states using variant modifiers. For example, use hover:gap-6
          to only apply the gap-6 utility
        </p>
        <button class="text-sky-800 font-bold text-2xl tracking-wider">
          View Case Study
        </button>
      </div>
      <div class="card-image bg-green-100">
        <img
          class="object-cover w-full h-72 md:h-96"
          src="./assets/project1.png"
        />
      </div>
    </div>

    <div class="card">
      <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-1/2">
        <h4 class="project-title item">Sheepify States</h4>
        <p class="font-work_sans pr-12">
          Designed some empty state screens in kawaii style for the popular
          sheepify app.Tailwind lets you conditionally apply utility classes in
          different states using variant modifiers. For example, use hover:gap-6
          to only apply the gap-6 utility
        </p>
        <button class="text-sky-800 font-bold text-2xl tracking-wider">
          View Case Study
        </button>
      </div>
      <div class="card-image">
        <img
          class="object-cover w-full h-48 md:h-96"
          src="./assets/project2.png"
        />
      </div>
    </div>

    <div class="card">
      <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-1/2">
        <h4 class="project-title">Sheepify States</h4>
        <p class="font-work_sans pr-12">
          Designed some empty state screens in kawaii style for the popular
          sheepify app.Tailwind lets you conditionally apply utility classes in
          different states using variant modifiers. For example, use hover:gap-6
          to only apply the gap-6 utility
        </p>
        <button class="text-sky-800 font-bold text-2xl tracking-wider">
          View Case Study
        </button>
      </div>
      <div class="card-image bg-green-100">
        <img
          class="object-cover w-full h-72 md:h-96"
          src="./assets/project1.png"
        />
      </div>
    </div>
  </div>

  <!-- <div class="banner-1" id="testimonial">
    <div class="space-y-4 grid place-items-center mt-5">
      <h3 class="heading3">Some Generous Words</h3>
      <p class="font-work_sans text-gray-600 font-semibold leading-relaxed">
        Some of my favorite testimonials from my clients
      </p>
    </div>
    <div class="max-w-6xl mx-auto px-8 py-16">
      <div class="relative">
        <div class="relative lg:flex rounded-lg shadow-2xl overflow-hidden">
          <div
            class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
          >
            <img
              class="absolute h-full w-full object-cover"
              src="https://a.slack-edge.com/80588/marketing/img/meta/slack_hash_256.png"
              alt=""
            />
            <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
            <svg
              class="relative"
              width="200"
              height="120"
              viewBox="0 0 200 120"
            >
              <path
                fill="#fff"
                fill-rule="evenodd"
                d="M63.75 75.24l2.5-5.93c2.7 2.05 6.3 3.13 9.85 3.13 2.61 0 4.27-1.03 4.27-2.6-.04-4.37-15.7-.95-15.82-11.9-.04-5.58 4.8-9.86 11.66-9.86 4.08 0 8.16 1.03 11.06 3.38l-2.34 6.05c-2.66-1.73-5.97-2.97-9.12-2.97-2.13 0-3.55 1.03-3.55 2.36.04 4.28 15.82 1.94 15.98 12.4 0 5.7-4.72 9.69-11.5 9.69-4.96 0-9.52-1.2-12.99-3.75zm96.01-8.08a7.16 7.16 0 0 1-8.11 3.5 7.35 7.35 0 0 1-5.38-7.13c0-3.34 2.2-6.27 5.38-7.12 3.16-.85 6.5.58 8.11 3.5l6.9-3.93a15.02 15.02 0 0 0-17.03-7.42 15.42 15.42 0 0 0-11.33 14.97c0 7.04 4.66 13.2 11.33 14.97a15.02 15.02 0 0 0 17.04-7.43l-6.9-3.9zM91.71 35.25h8.64v43.16h-8.64V35.25zm78.34 0v43.16h8.65V65.48l10.25 12.93H200l-13.03-15.37 12.06-14.34h-10.58l-9.76 11.9V35.25h-8.64zm-43.82 31.1a8.14 8.14 0 0 1-6.83 3.56 7.24 7.24 0 0 1-7.33-7.16 7.24 7.24 0 0 1 7.33-7.15 8.1 8.1 0 0 1 6.83 3.67v7.08zm0-18v3.4c-1.43-2.36-5-4-8.72-4-7.7 0-13.76 6.64-13.76 14.96 0 8.33 6.07 15.04 13.76 15.04 3.73 0 7.3-1.63 8.72-4v3.4H135v-28.8h-8.77zM10.53 66.4A5.32 5.32 0 0 1 5.3 71.8 5.32 5.32 0 0 1 .04 66.4a5.32 5.32 0 0 1 5.25-5.38h5.25v5.38zm2.63 0a5.32 5.32 0 0 1 5.25-5.38c2.9 0 5.25 2.4 5.25 5.38v13.46a5.32 5.32 0 0 1-5.25 5.39 5.32 5.32 0 0 1-5.25-5.39V66.4zm5.26-21.63a5.32 5.32 0 0 1-5.25-5.38A5.32 5.32 0 0 1 18.42 34c2.9 0 5.25 2.41 5.25 5.39v5.38h-5.25zm0 2.74c2.9 0 5.25 2.41 5.25 5.39a5.32 5.32 0 0 1-5.25 5.38H5.25A5.32 5.32 0 0 1 0 52.9a5.32 5.32 0 0 1 5.25-5.39h13.17zm21.03 5.39a5.32 5.32 0 0 1 5.25-5.39c2.9 0 5.25 2.41 5.25 5.39a5.32 5.32 0 0 1-5.25 5.38h-5.25V52.9zm-2.62 0a5.32 5.32 0 0 1-5.25 5.38 5.32 5.32 0 0 1-5.25-5.38V39.39A5.32 5.32 0 0 1 31.58 34c2.9 0 5.25 2.41 5.25 5.39v13.5zm-5.25 21.58c2.9 0 5.25 2.41 5.25 5.38a5.32 5.32 0 0 1-5.25 5.39 5.32 5.32 0 0 1-5.25-5.39v-5.38h5.25zm0-2.7a5.32 5.32 0 0 1-5.25-5.38 5.32 5.32 0 0 1 5.25-5.38h13.17c2.9 0 5.25 2.4 5.25 5.38a5.32 5.32 0 0 1-5.25 5.39H31.58z"
              />
            </svg>
          </div>
          <div class="relative lg:w-7/12 bg-white">
            <svg
              class="absolute h-full text-white w-24 -ml-12"
              fill="currentColor"
              viewBox="0 0 100 100"
              preserveAspectRatio="none"
            >
              <polygon points="50,0 100,0 50,100 0,100" />
            </svg>
            <div
              class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
            >
              <p v-html="profile.testimonial.quote"></p>
              <p class="mt-6">
                <a
                  :href="profile.testimonial.link"
                  class="font-medium text-indigo-600 hover:text-indigo-900"
                >
                  &rarr; {{ profile.testimonial.name }}</a
                >
              </p>
            </div>
          </div>
        </div>
        <div class="absolute inset-y-0 left-0 lg:flex lg:items-center">
          <button
            class="mt-24 lg:mt-0 -ml-6 h-12 w-12 rounded-full bg-white p-3 shadow-lg"
          >
            <svg
              class="h-full w-full text-indigo-900"
              fill="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                d="M5.41 11H21a1 1 0 0 1 0 2H5.41l5.3 5.3a1 1 0 0 1-1.42 1.4l-7-7a1 1 0 0 1 0-1.4l7-7a1 1 0 0 1 1.42 1.4L5.4 11z"
              />
            </svg>
          </button>
        </div>
        <div class="absolute inset-y-0 right-0 lg:flex lg:items-center">
          <button
            class="mt-24 lg:mt-0 -mr-6 h-12 w-12 rounded-full bg-white p-3 shadow-lg"
          >
            <svg
              class="h-full w-full text-indigo-900"
              fill="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                d="M18.59 13H3a1 1 0 0 1 0-2h15.59l-5.3-5.3a1 1 0 1 1 1.42-1.4l7 7a1 1 0 0 1 0 1.4l-7 7a1 1 0 0 1-1.42-1.4l5.3-5.3z"
              />
            </svg>
          </button>
        </div>
      </div>
    </div>
  </div> -->

  <div class="banner-2 md:flex items-center md:justify-evenly" id="about">
    <img
      class="md:h-[500px] h-[400px]"
      src="./assets/坐姿透明.png"
      alt="user image"
    />
    <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-1/2">
      <h4 class="project-title item">{{ profile.name }}</h4>
      <p class="font-work_sans" v-html="profile.aboutHtml"></p>
      <button class="text-sky-800 font-bold text-2xl tracking-wider">
        More about me...
      </button>
    </div>
  </div>

  <div id="contact" class="banner-1 flex h-full items-center">
    <div class="w-7/12 p-12">
      <h2 class="text-gray-700 md:text-6xl text-2xl font-Eczar mb-5 font-bold">
        Let’s work together and make everything super cute and super useful.
      </h2>
      <a
        class="underline text-2xl text-blue-600 font-work_sans"
        :href="'mailto:' + profile.email"
      >
        📧 {{ profile.email }}
      </a>
    </div>
    <div class="w-5/12 pr-28">
      <div class="flex flex-wrap justify-end gap-2">
        <!-- Only LinkedIn + Instagram (others removed) -->
        <a
          href="https://www.instagram.com/guanyj_/"
          target="_blank"
          rel="noopener"
          class="bg-gray-700 p-2 font-semibold text-white inline-flex items-center justify-center rounded-2xl"
        >
          <svg
            class="w-4 h-4 md:w-10 md:h-10 lg:w-10 lg:h-10 xl:h-10 xl:w-10 fill-current"
            role="img"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path d="M7.75 2h8.5A5.75 5.75 0 0 1 22 7.75v8.5A5.75 5.75 0 0 1 16.25 22h-8.5A5.75 5.75 0 0 1 2 16.25v-8.5A5.75 5.75 0 0 1 7.75 2zm0 1.5A4.25 4.25 0 0 0 3.5 7.75v8.5A4.25 4.25 0 0 0 7.75 20.5h8.5A4.25 4.25 0 0 0 20.5 16.25v-8.5A4.25 4.25 0 0 0 16.25 3.5h-8.5zM12 7.75a4.25 4.25 0 1 1 0 8.5 4.25 4.25 0 0 1 0-8.5zM12 9.25a2.75 2.75 0 1 0 0 5.5 2.75 2.75 0 0 0 0-5.5zm4.75-2.75a.75.75 0 1 1 0 1.5.75.75 0 0 1 0-1.5z"/>
          </svg>
        </a>

        <a
          href="https://www.xiaohongshu.com/user/profile/640a16990000000010028c9c"
          target="_blank"
          rel="noopener"
          class="bg-gray-700 p-2 font-semibold text-white inline-flex items-center justify-center rounded-2xl"
        >
          <img
            class="w-4 h-4 md:w-10 md:h-10 lg:w-10 lg:h-10 xl:h-10 xl:w-10"
            src="./assets/xiaohongshu.png"
            alt="小红书"
          />
        </a>

        <a
          :href="profile.linkedinUrl"
          target="_blank"
          rel="noopener"
          class="bg-gray-700 p-2 font-semibold text-white inline-flex items-center justify-center rounded-2xl"
        >
          <svg
            class="w-4 h-4 md:w-10 md:h-10 lg:w-10 lg:h-10 xl:h-10 xl:w-10 fill-current"
            role="img"
            viewBox="0 0 256 256"
            xmlns="http://www.w3.org/2000/svg"
          >
            <g>
              <path
                d="M218.123122,218.127392 L180.191928,218.127392 L180.191928,158.724263 C180.191928,144.559023 179.939053,126.323993 160.463756,126.323993 C140.707926,126.323993 137.685284,141.757585 137.685284,157.692986 L137.685284,218.123441 L99.7540894,218.123441 L99.7540894,95.9665207 L136.168036,95.9665207 L136.168036,112.660562 L136.677736,112.660562 C144.102746,99.9650027 157.908637,92.3824528 172.605689,92.9280076 C211.050535,92.9280076 218.138927,118.216023 218.138927,151.114151 L218.123122,218.127392 Z M56.9550587,79.2685282 C44.7981969,79.2707099 34.9413443,69.4171797 34.9391618,57.260052 C34.93698,45.1029244 44.7902948,35.2458562 56.9471566,35.2436736 C69.1040185,35.2414916 78.9608713,45.0950217 78.963054,57.2521493 C78.9641017,63.090208 76.6459976,68.6895714 72.5186979,72.8184433 C68.3913982,76.9473153 62.7929898,79.26748 56.9550587,79.2685282 M75.9206558,218.127392 L37.94995,218.127392 L37.94995,95.9665207 L75.9206558,95.9665207 L75.9206558,218.127392 Z M237.033403,0.0182577091 L18.8895249,0.0182577091 C8.57959469,-0.0980923971 0.124827038,8.16056231 -0.001,18.4706066 L-0.001,237.524091 C0.120519052,247.839103 8.57460631,256.105934 18.8895249,255.9977 L237.033403,255.9977 C247.368728,256.125818 255.855922,247.859464 255.999,237.524091 L255.999,18.4548016 C255.851624,8.12438979 247.363742,-0.133792868 237.033403,0.000790807055"
              ></path>
            </g>
          </svg>
        </a>
      </div>
    </div>
  </div>

  <button
    v-show="showScrollTop"
    @click="scrollToTop"
    class="fixed bottom-6 right-6 z-50 flex items-center justify-center h-12 w-12 rounded-2xl bg-gray-800 text-white shadow-lg hover:bg-gray-700 focus:outline-none"
    aria-label="Scroll to top"
  >
    <svg class="h-6 w-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <path d="M18 15l-6-6-6 6" />
    </svg>
  </button>
</template>
<script>
  export default {
    data() {
      return {
        showMenu: false,
        showScrollTop: false,
        profile: {
          name: "Jack Guan",
          role: "a self-motivated AI Enthusiast",
          linkedinUrl: "https://www.linkedin.com/in/jackguan2/",
          email: "guanyjack@foxmail.com",
          aboutHtml:
            "Ex-CCB Corporate Banking (3 Yrs)<br />MSc ISTM in CUHK <br />B.Eng in SCUT<br /> <br />" +
            "I love exploring different perspectives and finding creative solutions to problems. <br />I am passionate about using technology to make a positive impact on people's lives and am always looking for new opportunities to grow and learn.",
          // testimonial: {
          //   name: "Client Name",
          //   link: "#",
          //   quote:
          //     "[Client Name] said: <strong>Great work!</strong> They delivered a polished, usable experience and were a pleasure to work with.",
          // },
        },
      }
    },
    methods: {
      scrollToTop() {
        window.scrollTo({ top: 0, behavior: "smooth" })
      },
      onScroll() {
        this.showScrollTop = window.scrollY > 300
      },
    },
    mounted() {
      window.addEventListener("scroll", this.onScroll)
    },
    beforeUnmount() {
      window.removeEventListener("scroll", this.onScroll)
    },
  }
</script>
