<script>

  const myModal = new HystModal({
    linkAttributeName: "data-hystmodal",
  });

</script>

<div class="hystmodal" id="about-modal" aria-hidden="true">
  <div class="hystmodal__wrap">
    <div class="hystmodal__window" role="dialog" aria-modal="true">
      <button data-hystclose class="hystmodal__close">Закрыть</button>
        <h1>Hello World! 🚀 😎 📊 🌐</h1>
        <h2>Thanks for stopping by!! 💖</h2>
        <p>
          I am passionate about everything from full stack web development to big data analytics.
          Over the past year, I have been exploring these topics, through personal projects and hackathons.
          In the future, I would love to able to combine these two fields of software engineering, and make practical applications out of them.
        </p>
        <p>
          I am currently seeking internships and co-ops, that start from January (Spring 2023). I am also officially registered within the co-op program at SFU.
          Feel free to reach out to me <a href="mailto:tanish_shah@sfu.ca">here</a> or any of my other socials, if you have any opportunities. 
          I am extremely open and flexible to discuss with. 
        </p>
        <h1 class="sql-fun">
          <span style="color : #ac8ac6">SELECT</span>
          <span style="color : gold">*</span>
          <span style="color : #ac8ac6">FROM</span>
          <span style="color : gold">JOBS</span>
          <span style="color : #ac8ac6">WHERE</span>
          <span style="color : gold">JOB_TITLE</span>
          <span style="color : #ac8ac6">LIKE</span>
          <span style="color : #ac8ac6">IN</span>
          (
            <span style="color : lime ">"%Web%"</span>,
            <span style="color : lime">"%Full Stack%"</span>,
            <span style="color : lime">"%Data%"</span>,
            <span style="color : lime">"%Analyst%"</span>
          );
        </h1>
    </div>
  </div>
</div>

<style>
  h1 {
    margin : 10px;
  }

  h2 {
    font-size : 18px;
    margin-left : 20px;
  }

  .sql-fun {
    color : white;
    background-color : #282c34;
    padding : 7.5px;
    font-size : 15px;
  }

  .sql-fun > span {
    margin : 2.5px;
  }

  p {
    padding : 20px;
  }

</style>