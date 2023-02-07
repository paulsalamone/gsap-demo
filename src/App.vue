<template>
  <header>
    <h1>gsap <span>demo</span></h1>
  </header>
  <main>
    <section>
      <h2>1. Basic Animations</h2>
      <h3>Structure:</h3>
      <p class="structure">
        gsap.to("<span>selector</span>",<br />
        { <span>parameters</span> }
        <br />
        )
      </p>
      <div class="demo" id="demo1">demo1</div>
      <p>
        x: 300
        <button @click="handlePlayPause(1)">play</button>
      </p>

      <div class="demo" id="demo2">demo2</div>
      <p>
        rotation: 360
        <button @click="handlePlayPause(2)">play</button>
      </p>
      <div class="demo" id="demo3">demo3</div>
      <p>
        opacity: 0
        <button @click="handlePlayPause(3)">play</button>
      </p>
    </section>
    <section>
      <h2>2. Timeline Animations</h2>
      <h3>Structure:</h3>
      <p class="structure">
        const <span>myTimeline</span> = gsap.timeline( <br />
        &nbsp; {<span> timeline parameters</span>} <br />
        )
        <br />
      </p>
      <p class="structure">
        myTimeline.to("<span>selector</span>",{
        <br />
        &nbsp; {<span> keyframe 1 parameters </span>} <br />)
        <br />

        myTimeline.to("<span>selector</span>",{
        <br />
        &nbsp; {<span> keyframe 2 parameters </span>} <br />)
        <br />

        myTimeline.to("<span>selector</span>",{
        <br />
        &nbsp; {<span> keyframe 3 parameters </span>} <br />)
        <br />
      </p>
      <div class="demo yellow" id="demo4">demo4</div>
      <p>
        x: 150, color: "orange" <br />
        x: 300, color: "magenta" <br />
        x: 450, color: "green" <br />
        x: 600, color: "black" <br />

        <button @click="handleDemo4()">play</button>
      </p>
    </section>
    <section>
      <h2>3. Plugins (example: ScrollTrigger)</h2>
      <h3>Structure:</h3>
      <p class="structure">gsap.registerPlugin(<span>ScrollTrigger</span>)</p>
      <p class="structure">
        gsap.to("<span>selector</span>", { <br />
        &nbsp; <span>scrollTrigger</span>: { <br /><span
          >&nbsp;&nbsp;&nbsp;scrollTrigger parameters</span
        >
        },<br />
        &nbsp; <span>tween parameters</span> });
        <br />
        )
      </p>
      <p class="puffer">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt quam
        et delectus, aperiam veniam sequi a id eaque fugit, inventore in dolorem
        dignissimos omnis cupiditate accusamus quas ad dolore iusto est
        repellendus! Quasi vitae, commodi ex id laborum eos a omnis harum
        corporis cum? Optio consectetur nobis exercitationem asperiores iure nam
        nihil culpa quis omnis quas officia harum obcaecati, quisquam et unde
        consequatur ut velit dicta cupiditate ullam dolores non. Accusantium
        laudantium iure quo temporibus? Vero maiores a qui accusantium?
        Aspernatur est consequatur ea? Eaque numquam, impedit soluta accusantium
        repudiandae cupiditate inventore ea architecto. Enim dignissimos
        suscipit ut adipisci totam?
      </p>
      <div class="demo green" id="demo5">demo5</div>
      <p>
        gsap.to("#demo5", { <br />
        &nbsp;scrollTrigger: { <br />
        &nbsp;&nbsp;trigger: "#demo5", <br />
        &nbsp;&nbsp;start: "top center",
        <br />&nbsp;&nbsp;scrub: 1,<br />
        },<br />
        &nbsp;x: 600,<br />
        });
      </p>
      <p class="puffer">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt quam
        et delectus, aperiam veniam sequi a id eaque fugit, inventore in dolorem
        dignissimos omnis cupiditate accusamus quas ad dolore iusto est
        repellendus! Quasi vitae, commodi ex id laborum eos a omnis harum
        corporis cum? Optio consectetur nobis exercitationem asperiores iure nam
        nihil culpa quis omnis quas officia harum obcaecati, quisquam et unde
        consequatur ut velit dicta cupiditate ullam dolores non. Accusantium
        laudantium iure quo temporibus? Vero maiores a qui accusantium?
        Aspernatur est consequatur ea? Eaque numquam, impedit soluta accusantium
        repudiandae cupiditate inventore ea architecto. Enim dignissimos
        suscipit ut adipisci totam?
      </p>
      <div id="demo6">
        pinned area
        <div class="demo-slide" id="demo6-slide">slide</div>
        <!-- <div class="demo-slide" id="steve">slide 2</div>
        <div class="demo-slide" id="dan">slide 3</div> -->
      </div>
      <p>
        gsap.to("#demo6-slide", {<br />
        &nbsp; scrollTrigger: { <br />
        &nbsp; &nbsp; trigger: "#demo6", <br />
        &nbsp; &nbsp; start: "top 100px", <br />
        &nbsp; &nbsp; scrub: 1, <br />
        &nbsp; &nbsp; stagger: 0.5, <br />
        &nbsp; &nbsp; <span>pin: true</span>,<br />
        &nbsp; &nbsp; delay: 1,<br />
        &nbsp; },<br />
        &nbsp; x: 100,<br />
        &nbsp; backgroundColor: "#000021"<br />

        });
      </p>
      <p class="puffer">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt quam
        et delectus, aperiam veniam sequi a id eaque fugit, inventore in dolorem
        dignissimos omnis cupiditate accusamus quas ad dolore iusto est
        repellendus! Quasi vitae, commodi ex id laborum eos a omnis harum
        corporis cum? Optio consectetur nobis exercitationem asperiores iure nam
        nihil culpa quis omnis quas officia harum obcaecati, quisquam et unde
        consequatur ut velit dicta cupiditate ullam dolores non. Accusantium
        laudantium iure quo temporibus? Vero maiores a qui accusantium?
        Aspernatur est consequatur ea? Eaque numquam, impedit soluta accusantium
        repudiandae cupiditate inventore ea architecto. Enim dignissimos
        suscipit ut adipisci totam? Lorem, ipsum dolor sit amet consectetur
        adipisicing elit. Libero iure, sequi officia atque commodi perspiciatis
        ducimus accusamus blanditiis doloremque voluptates magni quas maxime
        ipsa! Ab fugit possimus obcaecati amet, corporis explicabo ullam rem
        minus. Maiores hic voluptates voluptate similique recusandae. Amet quam
        deleniti iste provident unde illo iure autem sunt porro corporis in,
        ducimus error excepturi possimus fugiat debitis placeat eveniet
        aspernatur non consequatur quidem architecto? In, explicabo earum qui
        rem dolorum iusto incidunt autem numquam reiciendis at perferendis
        nesciunt distinctio temporibus non suscipit tempora quia dicta molestias
        eveniet velit! Alias possimus facilis quidem voluptatem corrupti illo
        quod numquam qui!
      </p>
    </section>
  </main>
</template>

<script>
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);
export default {
  data() {
    return {};
  },
  mounted() {
    this.demo1 = gsap.to("#demo1", {
      x: 300,
      duration: 1,
      repeat: -1,
      yoyo: true,
      paused: true,
    });

    this.demo2 = gsap.to("#demo2", {
      rotation: 360,
      duration: 1,
      repeat: -1,
      yoyo: true,
      paused: true,
    });
    this.demo3 = gsap.from("#demo3", {
      opacity: 0,
      duration: 1,
      repeat: -1,
      yoyo: true,
      paused: true,
    });
    this.demo4 = gsap.timeline({
      repeat: 0,
      onComplete: () => {
        stop();
      },
    });

    gsap.to("#demo5", {
      scrollTrigger: {
        trigger: "#demo5",
        start: "top center",
        scrub: 1,
      },
      x: 600,
    });

    gsap.to("#demo6-slide", {
      scrollTrigger: {
        trigger: "#demo6",
        start: "top 100px",
        scrub: 1,
        stagger: 0.5,
        pin: true,
        // markers: true,
        delay: 1,
      },
      x: 100,
      backgroundColor: "#000021",
    });
    // gsap.to("#steve", {
    //   scrollTrigger: {
    //     trigger: "#steve",
    //     start: "top 100px",
    //     scrub: 1,
    //     stagger: 0.5,
    //     pin: true,
    //     markers: true,
    //     delay: 1,
    //   },
    //   x: 110,
    // });
    // gsap.to("#dan", {
    //   scrollTrigger: {
    //     trigger: "#demo6",
    //     start: "top 100px",
    //     scrub: 1,
    //     stagger: 0.5,
    //     pin: true,
    //     markers: true,
    //     delay: 1,
    //   },
    //   x: 120,
    // });
    // gsap.to("#demo6-b", {
    //   scrollTrigger: {
    //     trigger: "#demo6",
    //     start: "top top",
    //     scrub: 1,

    //     pin: true,
    //   },
    //   x: 0,
    //   stagger: 1,
    // });
    // gsap.to("#demo6-c", {
    //   scrollTrigger: {
    //     trigger: "#demo6",
    //     start: "top top",
    //     scrub: 1,
    //     pin: true,
    //   },
    //   x: 0,
    //   stagger: 2,
    // });
  },
  methods: {
    handlePlayPause(index) {
      if (this[`demo${index}`].vars.paused) {
        this[`demo${index}`].play();
        this[`demo${index}`].vars.paused = false;
      } else {
        this[`demo${index}`].pause();
        this[`demo${index}`].vars.paused = true;
      }
    },

    handleDemo4() {
      // this.demo4.restart();

      this.demo4.to("#demo4", {
        backgroundColor: "orange",
        x: 150,
      });
      this.demo4.to("#demo4", {
        backgroundColor: "magenta",
        x: 300,
      });
      this.demo4.to("#demo4", {
        backgroundColor: "green",
        x: 450,
      });
      this.demo4.to("#demo4", {
        backgroundColor: "black",
        color: "white",
        x: 600,
      });

      // this.demo4.stop();
    },
  },
};
</script>

<style lang="scss" src="./styles.scss"></style>
