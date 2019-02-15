<template>
  <div class="row">
    <div class="col-sm-9">
      <div class="headline">
        <h1>
          {{ cv_data.profile.name }}
          <span class="location">{{ cv_data.profile.location }}</span>
        </h1>
      </div>
      <p>
        {{ cv_data.profile.summary }}
      </p>

      <div class="cv-block">
        <h2>Experience</h2>
        <ul class="roles">
          <li v-for="experience in cv_data.experience">
            <h3>
              {{ experience.organisation }}
              <span class="location">{{ experience.location }}</span>
              <span class="role">{{ experience.position }}</span>
            </h3>
            <span class="timeframe">{{ experience.term}}</span>
            <p>
              {{ experience.summary }}
            </p>
            <ul class="projects">
              <li v-for="project in experience.projects">
                <h4>
                  {{ project.name }}
                  <span class="company">{{ project.organisation }}</span>
                </h4>
                <span class="timeframe">{{ project.term }}</span>
                <span class="timeframe-summary">{{ project.term_length }}</span>
                <p>
                  {{ project.summary }}
                </p>
                <ul class="skills">
                  <li v-for="skill in project.skills">
                    {{ skill }}
                  </li>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
      </div>
    </div>
    <div class="col-sm-3">
      <ul class="contact">
        <li class="phone">{{ cv_data.profile.contact.phone }}</li>
        <li class="email">{{ cv_data.profile.contact.email }}</li>
        <li class="twitter">{{ cv_data.profile.social.twitter }}</li>
        <li class="github">{{ cv_data.profile.social.github }}</li>
        <li>stackoverflow.com/users/{{ cv_data.profile.social.stackoverflow_user_id }}</li>
        <li>linkedin.com/in/{{ cv_data.profile.social.linkedin }}</li>
      </ul>

      <h4>Skills</h4>
      <ul>
        <li v-for="skill_group in cv_data.profile.skills">
          <span v-for="(skill, index) in skill_group.skills">
            {{skill}}<span v-if="index <= skill_group.length">, </span>
          </span>
        </li>
      </ul>

      <h4>Certifications</h4>
      <ul>
        <li v-for="certification in cv_data.certifications">
          <span>{{ certification.title}}</span>
          <span v-if="certification.date">{{ certification.date}}</span>
        </li>
      </ul>

      <h4>Community</h4>
      <ul>
        <li v-for="role in cv_data.community">
          <span>{{ role.role }}</span>
          <span>{{ role.organisation }}</span>
          <span>{{ role.term }}</span>
        </li>
      </ul>

      <!-- TODO: split into talks and workshops -->
      <h4>Recent events</h4>
      <ul>
        <li v-for="event in cv_data.events">
          <span>{{ event.event}}</span>
          <span>{{ event.organisation}}</span>
          <span>{{ event.date }}</span>
        </li>
      </ul>

      <h4>Education</h4>
      <ul>
        <li v-for="qualification in cv_data.education">
          <span>{{ qualification.qualification}}</span>
          <span>{{ qualification.institution}}</span>
          <span>{{ qualification.term }}</span>
          <span>{{ qualification.summary }}</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    cv_data: Object
  }
  // name: 'HelloWorld',
  // data () {
  //   return {
  //     msg: 'Welcome to Your Vue.js App'
  //   }
  // }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}

.timeframe-summary::before {
  content: "(";
}
.timeframe-summary::after {
  content: ")";
}
</style>
