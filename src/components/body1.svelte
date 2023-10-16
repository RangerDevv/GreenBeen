<script lang="ts">
    import { gsap } from "gsap";
    
    import { Flip } from "gsap/Flip";
    import { ScrollTrigger } from "gsap/ScrollTrigger";
    import { Observer } from "gsap/Observer";
    import { ScrollToPlugin } from "gsap/ScrollToPlugin";
    import { Draggable } from "gsap/Draggable";
    import { MotionPathPlugin } from "gsap/MotionPathPlugin";
    import { EaselPlugin } from "gsap/EaselPlugin";
    import { PixiPlugin } from "gsap/PixiPlugin";
    import { TextPlugin } from "gsap/TextPlugin";
    
    
    gsap.registerPlugin(Flip,ScrollTrigger,Observer,ScrollToPlugin,Draggable,MotionPathPlugin,EaselPlugin,PixiPlugin,TextPlugin);

    // target the element with a class of "green" - rotate and move TO 100px to the left over the course of 1 second. 
    gsap.to(".green", {rotation: 360, x: 100, duration: 1});

    // target the element with a class of "purple" - rotate and move FROM 100px to the left over the course of 1 second. 
    gsap.from(".purple", {rotation: -360, x: -100, duration: 1});

    // target the element with a class of "blue" - rotate and move FROM 100px to the left, TO 100px to the right over the course of 1 second. 
    gsap.fromTo(".blue", {x: -100},{rotation: 360, x: 100, duration: 1});
</script>


<html lang="en">
    <body>
        <main>
            <div id="3DHolder1">
                <div class="box green w-10 h-10 bg-black"></div>
                <div class="box purple"></div>
                <div class="box blue"></div>
            </div>
            <div class='flex flex-wrap justify-evenly w-screen h-[80vh]'>
                <div class="w-[50vw] flex-col mt-9">
                    <p class="text-2xl font-semibold">The Importance of Green Energy Initiatives</p>
                    <p class="text-lg">The world is at a critical juncture when it comes to environmental sustainability. Green energy initiatives are vital to mitigating the harmful effects of fossil fuels and combating climate change. By adopting renewable energy sources, we can make a significant positive impact on the environment.</p>
                </div>
            </div>
        </main>
    </body>
</html>