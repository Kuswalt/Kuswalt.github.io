<!-- Chris Jen Ian D. Roa -->
 <!-- Reference: Samual Oak Portfolio -->


<script>
    import Step from "./Step.svelte";

    // Array of project steps
    let steps = [
        {
            name: "WeatherWise",
            icon: "fa-solid fa-cloud",
            link: "https://github.com/Kuswalt/WeatherWise"
        },
        {
            name: "Formalytics",
            icon: "fa-solid fa-chart-simple",
            link: "https://github.com/Kuswalt/Formalytics"
        },
        {
            name: "AdvCalculator",
            icon: "fa-solid fa-calculator",
            link: "https://github.com/hizzCarlo/Advance-Calculator"
        },
    ];

    // Array of benefits
    let benefits = [
        {
            name: "a student developer",
            description: "For the past years, I have gone through a series of programming languages and frameworks, which ranges from HTML and CSS to PHP, Typescript, JavaScript and Python. I begin with online courses and tutorials. Online tutorials are so wonderful; I get a kick building projects from scratch. As my journey goes on, I enjoy doing everything-challenging myself whether in creating my personal website or developing some small application then learning all about it. Curiosity is something that, I think, will propel me; perseverance has always been my key to success and I am excited to keep growing in this ever-changing field!",
        },
        {
            name: "a backend developer",
            description: " I have experience working with technologies like SQL databases and RESTful API design. Recently, I developed a project that involved building a weather predition backend, which allowed me to implement features like weather forecasting and weather predictions. And am currently working on a project that involves building a webapp that allows users to ask questions to AI and get answers.",
        },
        {
            name: "interested in video games",
            description: "I have a passion for video games. From RPGs to indie titles, I love exploring the creativity and storytelling that games offer. Gaming has been a significant part of my life, inspiring me to analyze game design, mechanics, and user experience. I enjoy discussing the latest trends in the gaming industry and discovering hidden gems that push the boundaries of interactive storytelling.",
        },
    ];

    // Array of social media links
    let socials = [
        {
            name: "Gmail",
            icon: "fa-solid fa-envelope",
            description: "chrisianroa@gmail.com"
        },
        {
            name: "GitHub",
            icon: "fa-brands fa-github",
            link: "https://github.com/Kuswalt",
            description: "Kuswalt",
        },
        {
            name: "Facebook",
            icon: "fa-brands fa-facebook",
            link: "https://www.facebook.com/chrisjen.roa",
            description: "Chris Jen Roa",
        },
    ];

</script>


<main class="flex flex-col flex-1 p-4">
    <!-- Introduction Section -->
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
        
        <h5 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            Hi! I'm <span class="poppins text-blue-400 source-code-pro">Chris Jen Ian D. Roa</span>
            <br />A Student
            <span class="poppins text-blue-400">Developer</span>
        </h5>
            <p class="text-base sm:text-lg md:text-xl">
                A student at <span class="text-blue-400"> Gordon College</span> in the  <span class="text-blue-400"> Computer Studies</span> Department.
                and I’m currently taking a course on <span class="text-blue-400"> Bachelor of Science in Computer Science</span>
            </p>
            <a href="#social-info" class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-black text-white">
                <div
                    class="absolute top-0 right-full w-full h-full bg-blue-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"images/profileB1.jpg"}
                alt="img"
                class="object-cover z-[2] max-h-[70vh] rounded-full"
            />
        </div>
    </section>

    <!-- About Section -->
    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    > 
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-blue-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-blue-700 py-4"
        >
        <h6 class="text-large sm:text-xl md:text-">
            Curious to know more?
        </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                 Here's a bit more <span class="poppins text-blue-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am . . .
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
            
                <div class="flex gap-6 sm:gap-8">
                    <p
                        class="poppins text-4xl sm:text-5xl md:text-6xl text-blue-500 font-semibold"
                    >
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl press-start-font">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
    </section>

    <!-- Projects Section -->
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my projects this recent times.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Want to <span class="poppins text-blue-400">see</span> my works?
            </h3>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10 source-code-pro">
            {#each steps as step}
                <Step {step}>
                    <p>
                        {#if step.name === "WeatherWise"}
                            WeatherWise is a webapp weather forecast with location detection that utilizes
                            <strong class="text-blue-400"> Angular Framework</strong>, <strong class="text-blue-400">RestApi PHP</strong> & <strong class="text-blue-400">OpenWeather API </strong>to show 5 hour, 5 day weather forecasts.
                        {:else if step.name === "Formalytics"}
                            Formalytics is a group project for Application Development Course that utilizes <strong class="text-blue-400">Angular Framework</strong> & <strong class="text-blue-400">RestApi PHP</strong>. A webapp that allows a user to send questions to alumni to know their current life state and do analytical results based on the survey response.
                        {:else if step.name === "AdvCalculator"}
                            AdvCalculator is a <strong class="text-blue-400">Python</strong> built calculator, that can do basic calculations to advanced calculations. This is a project made with my friend hizzCarlo.
                        {/if}
                    </p>
                    <div class="flex-1 flex justify-between gap-4 items-end">
                        <div class="ml-auto cursor-pointer hover:text-white duration-200 relative after:absolute after:top-0 after:h-full after:right-full after:bg-black after:w-full after:duration-200 hover:after:translate-x-full after:z-[-1] overflow-hidden">
                            <a href={step.link} class="text-blue-400 hover:text-white">Go to &rarr;</a>
                        </div>
                    </div>
                </Step>
            {/each}
        </div>
    </section>

    <!-- Social Media Section -->
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="social-info">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                Connect with me.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Reach me on my <span class="poppins text-blue-400">social media</span>
            </h3>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            {#each socials as social}
                <Step step={social}>
                    {#if social.link}
                    <a href={social.link} class="text-blue-400 hover:text-white duration-200 relative after:absolute after:top-0 after:h-full after:left-0 after:w-0 after:duration-200 hover:after:w-full after:z-[-1] overflow-hidden" target="_blank" rel="noopener noreferrer">{social.description}</a>
                    {:else}
                        <p>{social.description}</p>
                    {/if}
                </Step>
            {/each}
        </div>
    </section>
</main>