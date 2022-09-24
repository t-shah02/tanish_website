<script>
  import ProjectCard from "./ProjectCard.svelte";

  const myModal = new HystModal({
    linkAttributeName: "data-hystmodal",
  });

  // prop definitioos for projects

  const UNI_MEETUPS = {
    title: "UniMeetups - Calgary Hacks 2022",
    links: {
      github: "https://github.com/t-shah02/UniMeetups",
      devpost: "https://devpost.com/software/unimeetups",
      youtube: "https://www.youtube.com/watch?v=OKCbhloGrm4",
    },
    techStack: [
      "Python",
      "Jinja",
      "HTML",
      "CSS",
      "Bootstrap 5",
      "Flask",
      "Repl.it DB",
      "Google Maps API",
    ],
    images: [
      "/static/uni_meetups/1.PNG",
      "/static/uni_meetups/2.PNG",
      "/static/uni_meetups/3.PNG",
    ],
    description:
      "UniMeetups is an application, that aims to connect university students that share common schedules, interests and goals. Authenticated users would be placed in one of 40 university hubs, based on their geogrpahical location and would be suggested matches instantly on signup. My team of 3 members had no prior experience to web development, and it was an amazing experience. We learned about the differences between front-end and back-end development, servers, APIs, endpoints, and CSS styling libraries!",
  };

  const SHOPINDER = {
    title : "Shopinder - RU Hacks 2022",
    links : {
      github : "https://github.com/t-shah02/shopinder",
      devpost : "https://devpost.com/software/shopinder",
      youtube : "https://www.youtube.com/watch?v=fGWjb30AEJQ"
    },
    images : [
      "/static/shopinder/1.PNG",
      "/static/shopinder/2.PNG",
      "/static/shopinder/3.PNG"
    ],
    techStack : [
      "Python",
      "Twilio",
      "SMTP",
      "Svelte",
      "HTML",
      "CSS",
      "Google OAuth",
      "Flask",
      "MongoDB",
      "BeautifulSoup4"
    ],
    description : "Shopinder is a shopping reminder app, where users can enter a product URL from our dozen supported stores, and add that product to their list of items. Every product to add to the list prompts the user to be reminded via SMS or email for notifications. This project was really useful for understanding page animations, handling error cases while web scraping, URL parsing with regex, and powerful third party service APIs that do heavy lifitng for your app."
  }


  const VIRTUAGNOSIS = {
    title : "Virtuagnosis - Hawk Hacks 2022",
    links : {
      github : "https://github.com/t-shah02/virtuagnosis",
      devpost : "https://devpost.com/software/virtuagnosis",
      youtube : "https://www.youtube.com/watch?v=9u4eY1A8AYQ"
    },
    techStack : [
      "Python",
      "Svelte",
      "HTML",
      "CSS",
      "Flask",
      "pandas",
      "numpy",
      "scikitlearn"
    ],
    images : [
      "/static/virtuagnosis/1.PNG",
      "/static/virtuagnosis/2.PNG",
    ],
    description : "Virtuagnosis is a disease prediction application, which accurately targets the 5 closest illnesses, the user might have depending on the symptoms they have selected on the front end. I found a disease medical dataset on Kaggle, as the main source for the train/test split of the K-nearest neighbor algorithm model. I used pandas for data cleaning, filtering, and feature engineering before creating a trained model. According to the metrics we calculated, our model could predict the correct disease 90% of the time."
  }



  const ECHIDNA_PY = {
    title : "Echidna.py - Discord Bot",
    links : {
      discord : "https://discord.com/api/oauth2/authorize?client_id=885305246962843648&permissions=311385245760&scope=bot%20applications.commands"
    },
    techStack : [
      "Python",
      "requests",
      "BeautifulSoup4",
      "Pillow",
      "numpy",
      "Pycord",
      "SQL",
      "Git",
      "Heroku"
    ],
    images : [
      "/static/echidna_py/1.PNG"
    ],
    description : "A bot written using the Pycord fork of discord.py. The mascot of the bot is Echidna (The Witch of Greed), from Re:Zero - Starting Life in Another World. This was one of my first serious Python projects, and it taught me code structure, using Git effecitvely for version control, packages, web scraping, HTTP requests, and asynchronous programming. The bot has anime, image processing, math, memes, and other fun miscellaneous command groups."
  }

  const TUNES_JAVA = {
    title : "Java Tunes - Desktop Music Player",
    links : {
      github : "https://github.com/t-shah02/java-tunes"
    },
    images : [
      "/static/java_tunes/1.PNG",
      "/static/java_tunes/2.PNG",
      "/static/java_tunes/3.PNG",
      "/static/java_tunes/4.PNG",

    ],
    techStack : [
      "Java",
      "Swing (GUI)",
      "JavaFX Media",
      "org.json"
    ],
  
    description : "An old fashioned music player written using the Swing GUI framework, in Java 8. Users can select mp3 files to play from their machine, create playlists, open playlists, edit/remove playlists, and lastly have their own optional album covers. I learned a lot about the OOP paradigm, styling layouts used in different types of front-end architectures, persisting the state of an application in memory, and how to model industry-level UML diagrams for large scale projects."
  }


</script>

<div class="hystmodal" id="projects-modal" aria-hidden="true">
  <div class="hystmodal__wrap">
    <div class="hystmodal__window" role="dialog" aria-modal="true">
      <button data-hystclose class="hystmodal__close">Закрыть</button>
      <h1>Projects (Personal and Hackathon) 📄</h1>

      <ProjectCard {...UNI_MEETUPS} />
      <ProjectCard {...SHOPINDER} />
      <ProjectCard {...VIRTUAGNOSIS} />
      <ProjectCard {...ECHIDNA_PY} />
      <ProjectCard {...TUNES_JAVA}/>

    </div>
  </div>
</div>

<style>
  h1 {
    margin: 10px;
    text-align: center;
  }
</style>
