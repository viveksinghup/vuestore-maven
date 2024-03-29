<template>
  <div class="bg-gray bg-opacity-50">
    <section class="bg-gray10 bg-opacity-50">
      <div class="container mx-auto px-4">
        <div
          class="
            flex flex-col-reverse
            md:flex-row
            pt-32
            pb-16
            md:pb-16
            px-6
            md:px-0
          "
        >
          <div class="flex items-center text-center lg:text-left lg:w-2/5">
            <div>
              <h2 class="text-4xl font-semibold md:text-7xl">
                Your Facility Experts
              </h2>
              <div class="h-2 md:w-16 bg-brandBlue my-10"></div>
              <div class="mt-2 text-sm md:text-lg">
                We are a full-fledged facility management company based in
                India. Our offerings include comprehensive facility management
                solutions to meet the growing demands for a better and healthier
                working environment.
              </div>
              <div class="flex justify-center lg:justify-start mt-7">
                <router-link
                  class="
                    px-7
                    py-2
                    leading-8
                    font-medium
                    rounded
                    border-2 border-brandBlue
                    text-brandBlue
                    hover:bg-brandBlue hover:text-white
                    transition
                    flex
                    items-center
                  "
                  to="/about/#facility"
                  >Know More</router-link
                >
              </div>
            </div>
          </div>
          <div class="lg:w-3/5 flex justify-center">
            <div class="h-full md:mb-0 mb-10 assets">
              <img
                src="@/assets/images/backgorund/hero-img.png"
                class="max-w-full"
              />
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="py-10">
      <div class="container mx-auto px-6 md:px-4">
        <div class="flex flex-col text-left md:flex-row">
          <div class="flex flex-col items-left md:w-1/2">
            <div class="text-2xl md:text-5xl font-medium">Our Services</div>
            <div class="h-1 hidden md:flex w-96 bg-black mt-6 mb-4"></div>
          </div>
          <div
            class="
              md:px-20 md:w-2/3
              flex-shrink-0
              text-lg
              md:text-2xl
              mt-10
              md:mt-16
            "
          >
            Bringing you the finest facility management solutions for a better
            and healthier working environment with our expertise and experience.
          </div>
        </div>

        <div
          class="
            grid grid-cols-1
            sm:grid-cols-1
            md:grid-cols-2
            xl:grid-cols-3
            gap-4
            mt-16 md:mt-24 allcard
          "
        >
          <div
            v-for="(data, index) in services"
            :key="index"
            class="flex card flex-col group bg-gray pl-8 md:pl-14 pr-8 py-5"
          >
            <div class="flex-1">
              <div class="flex items-center ctitle">
                <h2 class="flex flex-col font-bold p-2 text-2xl mr-4">
                  0{{ index + 1 }}
                </h2>
                <h2 class="mt-4 font-bold text-xl">{{ data.title }}</h2>
              </div>
              <div
                class="
                  h-1
                  w-20
                  bg-yellow
                  transition
                  group-hover:bg-brandBlue
                  mt-4
                  mb-4
                "
              ></div>
              <p class="text-gray-500 text-left mt-3 pr-4">
                {{ data.description }}
              </p>
            </div>
            <router-link :to="data.url" class="inline-block transition"
              ><img
                src="@/assets/images/arrow-blue.svg"
                class="w-10 card-arrow my-6"
            /></router-link>
          </div>
        </div>
      </div>
    </section>

    <div class="pt-20 pb-5 md:pt-48 relative overflow-hidden">
      <div class="container mx-auto px-6 md:px-20">
        <div class="flex md:flex-row items-center flex-col">
          <div class="md:w-1/2">
            <div
              class="
                text-2xl text-left md:text-5xl md:pr-32
                form-heading
                mb-5 md:mb-10
                md:mb-0
              "
            >
              Get a free consultation from top industry professionals and manage
              your facility with ease and perfection.
            </div>
            <div class="h-2 w-16 md:flex bg-brandBlue mt-5 mb-10 md:mb-4"></div>
          </div>
          <div class="md:w-1/2">
            <EnquiryForm></EnquiryForm>
          </div>
        </div>
      </div>
    </div>

    <section class="relative overflow-hidden py-32 md:py-64">
      <div class="container mx-auto px-4">
        <div class="flex flex-col md:flex-row">
          <div class="lg:lg:w-2/5 px-10 md:pr-0 md:pl-0 mb-10 md:mb-0">
            <img
              src="@/assets/images/backgorund/cust-info.png"
              class="max-w-full md:pr-10 assets"
            />
          </div>
          <div
            class="flex items-center pl-2 text-left lg:w-3/5 md:pl-20"
          >
            <div>
              <div class="text-xl md:text-3xl">
                Customer-centric solutions by Maven are powered by our
                experience + expertise approach, a unique combination of best
                industry practices with specialized solutions. Our solution
                driven methodology delivers increased productivity and provides
                the right ambiance for employees, visitors, and potential
                clients.
              </div>
              <div class="flex mt-10">
                <router-link
                  to="/services"
                  class="
                    px-9
                    py-3.5
                    leading-8
                    font-medium
                    bg-brandBlue
                    text-white
                    transition
                    flex
                    items-center
                  "
                  >Explore More
                  <span class="pl-2">
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      class="h-6 w-6"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke="currentColor"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M14 5l7 7m0 0l-7 7m7-7H3"
                      />
                    </svg>
                  </span>
                </router-link>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
  <section>
    <div class="bg-black relative overflow-hidden">
      <div class="container mx-auto px-10 md:px-4">
        <div
          class="
            flex flex-col
            md:flex-row
            py-20
            md:py-48 md:px-20
            items-center
            text-white
          "
        >
          <div class="lg:w-1/2">
            <div class="flex items-center lg:text-left md:pr-20">
              <div>
                <h2 class="text-2xl font-semi md:text-7xl mb-10 md:mb-0">
                  Why Choose Maven For Your Facility Needs?
                </h2>
                <div class="h-2 hidden md:block w-24 bg-brandBlue mt-10"></div>
              </div>
            </div>
          </div>
          <div class="flex items-center text-center lg:text-left lg:w-1/2">
            <div>
              <ul class="list list-outside space-y-8 md:space-y-16">
                <li
                  class="flex md:items-center"
                  v-for="(data, index) in textList"
                  :key="index"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="22.698"
                    height="15.063"
                    class="flex-shrink-0"
                    viewBox="0 0 22.698 15.063"
                  >
                    <path
                      id="Path_36"
                      data-name="Path 36"
                      d="M-137.889,6350.618l-2.566-7.657h-5.228l2.483,7.407h-4.7l-2.483-7.407h-5.228l2.482,7.406h-4.888l-2.566,7.657h5.228l2.482-7.406h4.711l-2.483,7.405h5.228l2.483-7.405Z"
                      transform="translate(160.586 -6342.961)"
                      fill="#ffcd28"
                    />
                  </svg>
                  <p class="ml-4 text-left">{{ data }}</p>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="overflow-hidden h-52 md:h-96">
    <img
      src="@/assets/images/home-coverimg.png"
      class="w-full object-cover h-full assets"
    />
  </section>

  <div class="bg-white">
    <section>
      <div class="container mx-auto md:px-20 pt-10 md:pt-40 pb-10 md:pb-12">
        <div class="flex flex-col items-center px-10 md:px-40">
          <div
            class="relative text-lg md:text-4xl quote-text text-left md:p-10 w-full m-1"
          >
            <img
              src="@/assets/images/comma.png"
              class="hidden md:block w-16 absolute -m-16 -mt-10 my-6 assets"
            />
            The FM industry is dynamically changing with unpredictable
            fluctuations and advancing technologies. The need for facility
            management has surged with the need for a virus-free and healthy
            ambience.
          </div>
        </div>
      </div>
    </section>

    <!-- Our Clients -->
    <section>
      <div
        class="
          container
          mx-auto
          px-4
          border-t border-gray10 border-opacity-50
          pt-10
          md:pt-24
        "
      >
        <div class="flex flex-col items-center">
          <div class="text-2xl md:text-5xl font-medium">Our Clients</div>
          <div class="h-2 w-16 hidden md:flex bg-brandBlue mt-5 mb-4"></div>
        </div>
        <div class="py-10">
          <marquee
            class="GeneratedMarquee"
            onmouseover="this.stop();"
            onmouseout="this.start();"
            repeat="yes"
            direction="left"
            scrollamount="5"
            behavior="scroll"
            loop="10"
          >
            <div class="flex space-x-5">
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/byjus.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/marvel.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/nexus.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/tsi.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo1.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo3.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo4.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo5.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo6.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo22.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/byjus.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/marvel.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/nexus.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/tsi.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo6.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo5.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo4.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo3.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo1.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo22.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/byjus.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/marvel.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/nexus.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/tsi.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo1.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo3.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo4.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo5.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo6.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/logo22.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/byjus.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/marvel.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/nexus.png" class="max-h-65" />
              </div>
              <div class="w-52 flex-shrink-0">
                <img src="@/assets/images/tsi.png" class="max-h-65" />
              </div>
            </div>
          </marquee>
        </div>
      </div>
    </section>
  </div>
  <section class="mt-28">
    <div class="bg-opacity-50 bg-gray">
      <div class="container mx-auto px-4">
        <div class="flex py-20 flex-col-reverse md:flex-row">
          <div
            class="flex items-center text-left lg:w-2/5 md:pr-20"
          >
            <div>
              <h2 class="text-xl md:text-6xl">
                Business Segments We Operate In
              </h2>
              <div
                class="h-2 w-16 hidden md:block bg-brandBlue my-10"
              ></div>
              <div class="mt-2 text-sm md:text-lg">
                We offer extensive facility management services in different
                industry segments. Our facility engineers are competently
                trained and experienced in providing cost-effective solutions
                while adhering to all the necessary regulations and mitigating
                the risk of unforeseen losses.
              </div>
            </div>
          </div>
          <div class="lg:w-3/5">
            <div class="w-100 h-full mb-10 md:mb-0">
              <img
                src="@/assets/images/backgorund/business.png"
                class="max-w-full md:pr-10 assets"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import EnquiryForm from "../common/EnquiryForm";
export default {
  name: "Home",
  data() {
    return {
      textList: [
        "We are always up-to-date with the current trends and best practices in the Facility Management space.",
        "We strictly adhere to statutory compliance norms without compromising quality in our services.",
        "Our employees/staff go through rigorous training before they are assigned to any project.",
        "We believe in a better tomorrow therefore, we use sustainable technology, tools & equipment in the delivery of soft services.",
        "We offer customized and innovative solutions to reach beyond your expectations.",
      ],
      services: [
        {
          title: "TECHNICAL SOLUTIONS",
          description:
            "We offer a whole range of Electromechanical, Maintenance and Repair solutions. Our competently trained staff provides regular and meticulous system check-ups, with performance evaluation and tech updates to optimise and ensure there is no productivity loss.",
          url: "/services/#techsolution",
        },
        {
          title: "SOFT SERVICE SOLUTIONS",
          description:
            "We employ a combination of Mechanised + Manpower led housekeeping strategies to beautify your facility. Our solution architects curate customized and cost-effective housekeeping and maintenance strategies to help you keep your vicinity hygienic, clean and green.",
          url: "/services/#softsolution",
        },
        {
          title: "PEST MANAGEMENT SOLUTIONS",
          description:
            "Our pest management solutions are aimed at eliminating the population of insects that are considered detrimental to humans, your facility and the environment by using green methods to ensure quality, health and safety regulations.",
          url: "/services/#pest",
        },
        {
          title: "SECURITY SOLUTIONS",
          description:
            "We have one of the best-trained security personnel in the industry with keen observation skills and a wide range of security solutions and access control systems. We offer fully-customized security services to schools, government buildings, public centres, retail stores, commercial and residential buildings, hotels, etc.",
          url: "/services/#security",
        },
        {
          title: "SPECIALISED SERVICES SOLUTIONS",
          description:
            "Our extensive specialized solutions are exclusively designed to meet your short-term facility needs. We offer one-time Project and Façade cleaning services, and Vendor management, Help-desk management, Staffing and Payroll solutions.",
          url: "/services/#specialservices",
        },
      ],
    };
  },
  components: {
    EnquiryForm,
  },
};
</script>

<style lang="postcss" scoped>
.form-heading {
  line-height: 62px;
}
.card-arrow {
  transition: 0.45s;
  transform: scale3d(1, 1, 1);
}
.card:hover .card-arrow {
  transform: scale3d(1.2, 1.2, 1.2);
}
.quote-text{
  line-height: 50px;
}
.bussiness-img{
  max-height: 900px;
}
.allcard .card:first-child .ctitle{
  padding-right: 110px;
}
.allcard .card:nth-child(4) .ctitle{
  padding-right: 110px;
}
.max-h-65{
  max-height: 65px;
  margin: 0 auto;
}
@media screen and (max-width: 800px) {
  .form-heading {
    line-height: 32px;
  }
}
</style>
