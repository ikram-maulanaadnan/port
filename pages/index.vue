<template>
  <b-container fluid class="bg-light p-5">
    <b-row>
      <b-col md="4" class="text-center">
        <b-img src="@/assets/pp.jpg" rounded-circle alt="Profile Picture" fluid class="mb-3" />
        <h2>Your Name</h2>
        <p class="text-muted">Aspiring [Data science, data analyst, IoT and data enginner]</p>
        <b-button variant="primary" href="https://www.linkedin.com/in/ikram-maulana-adnan-009960247/">Contact Me</b-button>
      </b-col>
      <b-col md="8">
        <b-card class="shadow-lg mb-3">
          <b-card-title class="text-primary">About me</b-card-title>
          <b-card-text>
            Aspiring Information Technology professional and current undergraduate student at Brawijaya University, 
            dedicated to leveraging a solid foundation in computer science, programming, and network administration to contribute effectively in the IT field. Passionate about cybersecurity, data engineering, and Network Engineering.
I thrive in dynamic environments and am always eager to learn new technologies and methodologies. With hands-on experience in various IT projects and a commitment to continuous improvement, I aim to solve real-world problems through innovative technological solutions.
          </b-card-text>
        </b-card>

        <b-card class="shadow-lg mb-3">
          <b-card-title class="text-primary">Skills</b-card-title>
          <b-card-text>
            <b-list-group>
              <b-list-group-item v-for="(skill, index) in skills" :key="index">
                <b-icon icon="check-circle" variant="success" class="mr-2"></b-icon> {{ skill }}
              </b-list-group-item>
            </b-list-group>
          </b-card-text>
        </b-card>

        <b-card class="shadow-lg mb-3">
          <b-card-title class="text-primary">Education</b-card-title>
          <b-card-text>
            <b>An Undergraduate Student</b> - Brawijaya University<br />
            Database,Computer Networking,Website Programming And Object Oriented Programming
            GPA: 3.84<br /><br />
            <b>Senior High School</b> - SMAN 4 KAB TANGERANG (2020-2023)<br />
            Mathematics And Life Science
          </b-card-text>
        </b-card>

        <b-card class="shadow-lg mb-3">
          <b-card-title class="text-primary">Projects</b-card-title>
          <b-card-text>
            <b-list-group>
              <b-list-group-item v-for="(project, index) in projects" :key="index">
                <b-icon icon="folder" variant="info" class="mr-2"></b-icon> 
                <a :href="project.link" target="_blank">{{ project.name }}</a>: {{ project.description }}
              </b-list-group-item>
            </b-list-group>
          </b-card-text>
        </b-card>

        <b-card class="shadow-lg mb-3">
          <b-card-title class="text-primary">Activities</b-card-title>
          <b-card-text>
            <b-list-group>
              <b-list-group-item v-for="(activity, index) in activities" :key="index">
                <b-icon icon="star" variant="warning" class="mr-2"></b-icon> {{ activity }}
              </b-list-group-item>
            </b-list-group>
          </b-card-text>
        </b-card>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: 'ResumeProfile',
  data() {
    return {
      skills: ['MySql', 'Python', 'Java', 'Basic IoT'],
      projects: [
        { name: 'Project ', link: '-', description: '-' },
        { name: 'Project ', link: '-', description: '-' },
      ],
      activities: [
        'Exchange and Collaboration programs at Universiti Teknologi Petronas',
      
      ]
    }
  }
}
</script>

<style scoped>
h2 {
  margin-top: 10px;
}
.b-card {
  transition: transform 0.2s;
}
.b-card:hover {
  transform: scale(1.02);
}
.bg-light {
  background-color: #f8f9fa !important;
}
</style>
