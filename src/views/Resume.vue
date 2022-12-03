<template>
  <v-layout row justify-center align-center wrap class="mt-4 pt-2">
    <v-flex xs12 sm12 md4 lg4 xl4 class="mt-4 pt-4">
      <h2 class="mb-4 pl-4 pt-2">Education</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">Expected in January 2023 -</div>
                
              </v-flex>
              <v-flex class="pl-2">
                <strong>George Mason University</strong>
                
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">October 2020 - September 2022</div>
                
              </v-flex>
              <v-flex class="pl-2">
                <strong>Aptech Computer Education</strong>

              </v-flex>
            </v-layout>
          </v-timeline-item>

         
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-flex xs12 sm12 md4 lg4 xl4 class="mt-4 pt-2">
      <h2 class="mb-4 pl-4">Experience</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">October 2022 - Current</div>
                
              </v-flex>
              <v-flex class="pl-2">
                <strong>Python Web Developer</strong>
                
              </v-flex>
            </v-layout>
          </v-timeline-item>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">October 2020 - September 2022</div>
                
              </v-flex>
              <v-flex class="pl-2">
                <strong>PHP Web Developer</strong>
                
              </v-flex>
            </v-layout>
          </v-timeline-item>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">January 2020 - August 2020</div>
                
              </v-flex>
              <v-flex class="pl-2">
                <strong>PHP Web Developer Intern</strong>
                
              </v-flex>
            </v-layout>
          </v-timeline-item>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">June 2019 - December 2019</div>
                
              </v-flex>
              <v-flex class="pl-2">
                <strong>Front-End Web Developer Intern</strong>
                
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-flex xs12 sm12 md4 lg4 xl4 class="mt-4 pt-2">
      <h2 class="mb-4 pl-4">IT Certifications</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">October 2022</div>
                
              </v-flex>
              <v-flex class="pl-2">
                <strong>PCAP™ – Certified Associate in Python Programming</strong>
                
              </v-flex>
            </v-layout>
          </v-timeline-item>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">November 2022</div>
                
              </v-flex>
              <v-flex class="pl-2">
                <strong>PCEP™ – Certified Entry-Level Python Programmer</strong>
                
              </v-flex>
            </v-layout>
          </v-timeline-item>
         
        </v-timeline>
      </v-card-text>
    </v-flex>
    
  </v-layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Resume',
    titleTemplate: "%s ← Eldin's Space",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        name: 'description',
        content:
          'Vue NUXT HTML CSS JavaScript Design Adobe XD Photoshop Coding Skills Resume Work Web Developer Front-End'
      },
      { charset: 'utf-8' },
      { property: 'og:title', content: "Eldin' Space" },
      { property: 'og:site_name', content: "Eldin' Space" },
      { property: 'og:type', content: 'website' },
      { property: 'og:url', content: 'https://eldin.space' },
      {
        property: 'og:image',
        content: 'https://i.imgur.com/Dcz2PGx.jpg'
      },
      {
        property: 'og:description',
        content:
          'Vue NUXT HTML CSS JavaScript Design Adobe XD Photoshop Coding Skills Resume Work Web Developer Front-End'
      }
    ]
  },
  data () {
    return {
      value: 0,
      buffer1: 0,
      buffer2: 0,
      buffer3: 0,
      buffer4: 0,
      buffer5: 0,
      buffer6: 0,
      bufferValue: 100,
      interval: 0
    }
  },
  mounted () {
    this.startBuffer()
  },

  beforeDestroy () {
    clearInterval(this.interval)
  },

  methods: {
    startBuffer () {
      this.interval = setInterval(() => {
        this.buffer1 = 90
        this.buffer2 = 85
        this.buffer3 = 80
        this.buffer4 = 80
        this.buffer5 = 90
        this.buffer6 = 70
      }, 800)
    }
  }
}
</script>
<style >
</style>
