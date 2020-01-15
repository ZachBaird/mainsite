<template>
  <v-container>
    <v-img
      src="v.png"
      width="150px"
      height="150px"
      contain
      class="mx-auto"
      alt="My wife and I"
    />
    <br>
    <div class="introduction">
      <p>
        Welcome!<br><br>My name is Zach. I am a software engineer currently developing for Leidos in Harrisburg, PA. With almost 3 years of experience, I have primarily worked with software from the healthcare and military sectors.<br>If you're interested in my work experience,
        <v-btn
          href="../ZachBairdResume.pdf"
          target="_blank"
          color="primary"
          small
          text
        >
          see my resume!
        </v-btn>
      </p>
      <p>
        In my personal time, I take a serious interest in self-investment and open-source development. If I'm not working on a project for myself, I'm either tutoring on The Odin Project or spending time with my wife and 2 dogs; Kona and Chai.
        <br>
        If you want to see some personal projects,
        <v-btn
          href="/projects"
          target="_blank"
          color="primary"
          small
          text
        >
          click here!
        </v-btn>
      </p>
    </div>
    <div class="introduction my-5">
      <h2 class="font-weight-regular text-center mb-2">
        Kona & Chai
      </h2>
      <v-img
        src="v.png"
        height="150px"
        width="150px"
        contain
        class="mx-auto"
        alt="Kona"
      />
      <br>
      <v-img
        src="v.png"
        height="150px"
        width="150px"
        contain
        class="mx-auto"
        alt="Chai"
      />
    </div>
  </v-container>
</template>

<script>
export default {
  data () {
    return {}
  }
}
</script>

<style scoped>
.introduction {
    max-width: 650px;
    width: 70%;
    margin: auto;
}
</style>
