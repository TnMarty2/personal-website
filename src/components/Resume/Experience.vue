<script>
export default {
  data(){
    return {
      experiences:[
        {
          year: "Oct 2023 - Present",
          jobs: "Front-End Developer",
          company: "Generazone",
          location: "Yogyakarta",
          description: [
            "Developed and maintained websites using Wordpress and Elementor, creating an efficient and simple web.",
            "created a safe space for Gen Z to develop themselves while having difficulty regulating emotions and other mental problems.",
          ]
        },
        {
          year: "Aug 2023 - Jan 2024",
          jobs: "Machine Learning Cohort",
          company: "PT Dicoding Akademi Indonesia",
          location: "Bandung",
          description: [
            "Developed projects using Python, create machine learning models that can be used to predict cataract eye.",
            "Learning machine learning specialization, equipped with tech expertise, soft skills, and English proficiency.",
            "Define and explain key concepts involved in data analytics including data, data analysis, and data ecosystem."
          ]
        }
      ]
    }
  }
}
</script>

<template>
  <section>
    <div class="d-flex align-items-center justify-content-between mb-4">
      <h2 class="text-primary fw-bolder mb-0">Experience</h2>
<!--      <a class="btn btn-primary px-4 py-3" href="#!">-->
<!--        <div class="d-inline-block bi bi-download me-2"></div>-->
<!--        Download Resume-->
<!--      </a>-->
    </div>

    <div v-for="experience of experiences" :key="'experience-index-' + experience.company" class="card shadow border-0 rounded-4 mb-5">
      <div class="card-body px-3 px-md-5 py-5">
        <div class="row align-items-center gx-5">
          <div class="col text-center text-lg-start mb-4 mb-lg-0">
            <div class="p-4 rounded-4">
              <div class="text-primary fw-bolder mb-2">{{experience.year}}</div>
              <div class="small fw-bolder">{{experience.jobs}}</div>
              <div class="small text-muted">{{experience.company}}</div>
              <div class="small text-muted">{{experience.location}}</div>
            </div>
          </div>
          <div class="col-lg-8">
            <div>
              <ul class="mb-0">
                <li v-for="desc of experience.description">
                  {{desc}}
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>