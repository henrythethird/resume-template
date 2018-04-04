<template>
  <div class="main">
    <h1 class="name">{{ name }}</h1>
    <h2 class="position">Software Engineering Student</h2>

    <Section 
      v-for="section in sections" 
      class="section" 
      :items="section.items"
      :key="section.title"
    >
      <template slot="title">{{ section.title }}</template>
    </Section>
  </div>
</template>

<script>
import Section from './Section'

export default {
  name: 'Main',
  props: ['name'],
  components: {
    Section
  },
  data () {
    return {
      sections: [
        {
          title: 'work experience',
          items: [
            {
              range: "2012-2014",
              title: "Some other company LLC",
              subtitle: "Junior Frontend Engineer",
              text:
                "Sartorial cardigan flexitarian health goth. Flannel swag synth man braid, drinking vinegar gastropub neutra. Gastropub yr drinking vinegar hell of pug viral irony vape cold-pressed scenester cronut whatever woke VHS brunch. Try-hard locavore vice gluten-free wolf. Chicharrones skateboard man braid, woke pinterest yr microdosing. Microdosing sriracha selfies VHS glossier shabby chic YOLO jianbing beard put a bird on it activated charcoal drinking vinegar cornhole roof party flannel."
            },
            {
              range: "2014-2016",
              title: "Yet another company",
              subtitle: "Professional Frontend Engineer",
              text:
                "Sartorial cardigan flexitarian health goth. Flannel swag synth man braid, drinking vinegar gastropub neutra. Gastropub yr drinking vinegar hell of pug viral irony vape cold-pressed scenester cronut whatever woke VHS brunch. Try-hard locavore vice gluten-free wolf. Chicharrones skateboard man braid, woke pinterest yr microdosing. Microdosing sriracha selfies VHS glossier shabby chic YOLO jianbing beard put a bird on it activated charcoal drinking vinegar cornhole roof party flannel."
            }
          ]
        },
        {
          title: 'education',
          items: [
            {
              range: '2012-2014',
              title: "University of Applied Sciences Zürich",
              subtitle: 'Bacherlor of Computer Science',
              text: 'Vice cardigan meh, locavore tacos chicharrones brunch pabst hammock tote bag distillery marfa direct trade DIY vegan. Palo santo trust fund tattooed hot chicken artisan, taiyaki polaroid cornhole offal umami tousled bushwick leggings tumeric. Street art cardigan snackwave small batch four loko chartreuse trust fund hella stumptown ethical mumblecore put a bird on it typewriter adaptogen authentic. Vegan everyday carry 90\'s palo santo beard occupy gastropub readymade tumblr single-origin coffee pitchfork. Vexillologist mumblecore listicle unicorn hammock messenger bag gentrify coloring book raw denim twee tbh master cleanse. Prism try-hard salvia, flannel green juice kitsch affogato subway tile migas. Paleo succulents farm-to-table, salvia fanny pack green juice seitan pug flexitarian actually squid echo park truffaut cronut chillwave.'
            }
          ]
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  .name {
    padding: 0;
    margin-top: 20px;
    font-size: 50px;
  }

  .position {
    font-size: 16px;
    font-style: italic;
    opacity: 0.6;
    letter-spacing: 3px;
    font-variant: small-caps;
    margin-bottom: 124px;
  }

  .main {
    padding: 50px;
  }

  .section {
    margin-bottom: 50px;
  }
</style>