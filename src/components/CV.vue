<template>
  <div class="hello">

    <div class="headline">
      <h1>Ryan Brooks Sheffield <span class="location">UK/Remote</span></h1>
    </div>
    <p>
      An experienced CTO, leader and full-stack developer, with a focus on people, process and remote-first working. I have a track record of introducing Agile processes, TDD and code quality, and favour steady, lasting change and building for the future.
    </p>

    <div class="cv-block">
      <h2>Experience</h2>
      <ul class="roles">
        <li>
          <h3>
            Slate Horse Ltd
            <span class="location">Oxford/Sheffield</span>
            <span class="role">Director &amp; Principal Consultant</span>
          </h3>
          <span class="timeframe">January 2015 – Present</span>
          <p>
            Offering Interim CTO services, project-based contract development and consultancy with a focus on software quality, testing, and empowering developers. I undertook the following projects:
          </p>
          <ul class="projects">
            <li>
              <h4>
                National Pupil Database Find & Explore
                <span class="company">Department for Education</span>
              </h4>
              <span class="timeframe">September 2018 – March 2019</span>
              <span class="timeframe-summary">6 months</span>
              <p>
                Technical Architect in a cross-functional team. Used domain modelling to solve critical problems with the existing service. Prototyped Excel loading into ElasticSearch to help researchers discover available data, architected a VPN/RDP-based secure research environment, and a suite of standard extracts/process for researchers to access the data. Also assisted technical recruitment.
              </p>
              <ul class="skills">
                <li>Ruby</li>
                <li>ElasticSearch</li>
                <li>PostgreSQL</li>
                <li>SQL Server</li>
                <li>Azure</li>
              </ul>
            </li>
          </ul>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
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
