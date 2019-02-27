<style scoped>
h1{
    margin: 2%;
    font-weight: 300;
    font-size: 45px;
}
</style>

<template>
    <div class="container" 
        data-aos="fade-right" 
        data-aos-anchor-placement="top-bottom"
        data-aos-duration="1000"
        >
        <h1>RESUME</h1>
        <ResumeEntry v-for="job in resumeEntries" v-bind:job="job" v-bind:key="job.key"/>
      <hr/>
    </div>
</template>

<script>
import ResumeEntry from "./ResumeEntry.vue"
export default {
    components: {
        ResumeEntry,
    },
    data(){
        return{
            resumeEntries: [
        {
          key: 0,
          title: "Engineering Resident",
          location: "Google - Mountain View, CA",
          date: "July 2019 - Present",
          badge: "google",
          body: [
            "I just accepted an offer for a job at Google! Come July, I will be moving up to Mountain View, California and starting my new job as an Engineering Resident. The first two months of which, I’ll be learning as much as I can while taking classes made by Google. Then, I’ll have 2 five-month rotations with different teams. I’m excited to see what July brings! :)"
          ]
        },
        {
          key: 1,
          title: "Software Development Intern",
          location: "Amazon, Seattle, WA",
          date: "September - December 2018",
          badge: "aws",
          body: [
            "Worked on the AWS Elastic Block Store (EBS) Statistics team to improve internal system health tools by building a semi-structured data and log querying engine.",
            "Used Apache Spark + SparkSQL on top of AWS EMR, and S3 to build a SQL-like semi-structured data system to provide real-time statistics and insights into drive health throughout the EBS fleet.",
            "Incorporated log files into semi-structured databases to provide a wholistic view of fleet health."
          ]
        },
        {
          key: 2,
          title: "Software Engineering Intern",
          location: "OfferUp, Seattle, WA",
          date: "May - August 2018",
          badge: "offerup",
          body: [
            "Worked on the Android Autos team to improve user experience when buying and selling cars on the OfferUp platform. Developed a vehicle VIN scanning feature, a generic First Time User Experience page, and other auto-related features.",
            "Developed brand new VIN scanning feature that utilizes computer vision to scan vehicle information code. VIN scanning feature then utilizes 3rd party API to pull vehicle history information into the app.",
            "Designed and implemented generic onboarding tools and tooltips for other developers at OfferUp.",
            "Redesigned and refactored old design patterns to match current OfferUp best practices."
          ]
        },
        {
          key: 3,
          title: "Student Researcher",
          location: "USC Brain and Body Dynamics Lab",
          date: "January - May 2018",
          badge: "usc",
          body: [
            "Developed a clinical VR application with a team to explore novel prosthetic possibilities for paralyzed individuals. Designed experiments to study the relationship between the speed of learning complex tasks, and strategies used.",
            "Used Unity and C# to create a VR environment in which paralyzed individuals trained an EEG reading AI.",
            "Redesigned and upgraded robotic system that approximates human tendons for use with cadaver hands. Brought cost down from ~$8,000 to $500 per system and improved modularity of hardware and codebase.",
            "Created high-throughput system to handle data storage from clients, and pass data between hand controlling robot, VR environment, and robotic feedback over the network."
          ]
        }

      ]
        }
    }
}
</script>