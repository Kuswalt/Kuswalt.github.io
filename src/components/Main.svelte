<script>
    import Step from "./Step.svelte";

    let steps = [
        {
            name: "WeatherWise",
            icon: "fa-solid fa-cloud",
            description: "",
            link: "https://github.com/Kuswalt/WeatherWise"
        },
        {
            name: "Formalytics",
            icon: "fa-solid fa-chart-simple",
            description: "",
            link: "https://github.com/Kuswalt/Formalytics"
        },
        {
            name: "Pokédex",
            icon: "",
            description: "",
            link: ""
        },
    ];

    let benefits = [
        {
            metric: "10x",
            name: "a self taught developer",
            description: "I taught myself to code using free online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Starting of with JavaScript, HTML & CSS and evolving my knowledge base to include JavaScript frameworks, backend programming, design, cloud services and much much more.",
        },
        {
            name: "a product design & UX finatic",
            description: "Carefully crafting and designing amazing user experiences allows me to express and experiment with every morsel of creativity I have. I love the challenge of learning new design concepts and enabling users with amazing online experiences.",
        },
        {
            name: "an excellent communicator",
            description: "Communication is key and it's a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team.",
        },
    ];

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
            link: "https://facebook.com/Chris-Jen-Roa",
            description: "Chris Jen Roa",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h5 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Hi! I'm <span class="poppins text-violet-400">Chris Jen Ian Roa</span>
                <br />A Developer
                <span class="poppins text-violet-400">Student</span>
            </h5>
            <!-- <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400"> favorite tech</span> includes JavaScript
                (NEXT.JS or SvelteKit), TailwindCSS, Node.js + Express.js & PostgreSQL
                or Firebase/Firestore!
            </p> -->
            <a href="#social-info" class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950">
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"images/profileB.jpg"}
                alt="img"
                class="object-cover z-[2] max-h-[70vh] rounded-full"
            />
        </div>
    </section>


    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <!-- <div class="z-[-1] bg-violet-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div> -->
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
        >
           
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                 <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am . . .
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
            
                <div class="flex gap-6 sm:gap-8">
                    <p
                        class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                    >
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
    </section>



    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my projects this past years.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>



        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                  
                <p>
                    WeatherWise is a webapp weather forecast with location detetction that utilizes
                     <strong class="text-violet-400"> Angular Framework</strong>, <strong class="text-violet-400">RestApi PHP</strong> & <strong class="text-violet-400">OpenWeather API </strong>to show 5 hour, 5 day weather forecasts.
                </p>
                <div class="flex-1 flex justify-betweeen gap-4 items-end">
                    <div
                        class="ml-auto cursor-pointer hover:text-slate-950 duration-200 relative after:absolute after:top-0 after:h-0 after:right-full after:bg-white after:w-full after:h-full after:duration-200 hover:after:translate-x-full after:z-[-1] overflow-hidden"
                    >
                        <a href={steps[0].link} class="text-violet-400">Go to &rarr;</a>
                    </div>
                </div>
            </Step>


            <Step step={steps[1]}>
                <p>
                    Formalytics is a group project for Application Development Course that utilizes <strong
                        class="text-violet-400">Angular Framework</strong
                    > & <strong class="text-violet-400">RestApi PHP</strong>. A webapp
                    that allows a user to send questions to alumnis to know their currrent life state and do analytical results based on the survey response.
                </p>
                <div class="flex-1 flex justify-betweeen gap-4 items-end">
                    <div
                        class="ml-auto cursor-pointer hover:text-slate-950 duration-200 relative after:absolute after:top-0 after:h-0 after:right-full after:bg-white after:w-full after:h-full after:duration-200 hover:after:translate-x-full after:z-[-1] overflow-hidden"
                    >
                        <a href={steps[1].link} class="text-violet-400">Go to &rarr;</a>
                    </div>
                </div>
            </Step>




            <Step step={steps[2]}>
                <!-- <p>
                    The Pokédex is a <strong class="text-violet-400"
                        >SvelteKit & TailwindCSS</strong
                    >
                    web application, hosted on
                    <strong class="text-violet-400">Netlify</strong>, that
                    consumes and caches the
                    <strong class="text-violet-400">Pokémon API</strong>
                    to display all Pokémon information. Gotta catch them all!
                </p> -->
                <div class="flex-1 flex justify-betweeen gap-4 items-end">
                    <div
                        class="ml-auto cursor-pointer hover:text-slate-950 duration-200 relative after:absolute after:top-0 after:h-0 after:right-full after:bg-white after:w-full after:h-full after:duration-200 hover:after:translate-x-full after:z-[-1] overflow-hidden"
                    >
                        <a href={steps[2].link} class="text-violet-400">Go to &rarr;</a>
                    </div>
                </div>
            </Step>
        </div>
    </section>

    <section class="py-20 lg:py-32 flex flex-col gap-24" id="social-info">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                Connect with me.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Follow me on <span class="poppins text-violet-400">social media</span>
            </h3>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            {#each socials as social}
            <Step step={social}>
                {#if social.link}
                <a href={social.link} class="text-violet-400 hover:text-slate-950 duration-200 relative after:absolute after:top-0 after:h-full after:left-0 after:bg-white after:w-0 after:duration-200 hover:after:w-full after:z-[-1] overflow-hidden" target="_blank" rel="noopener noreferrer">{social.description}</a>
            {:else}
                    <p>{social.description}</p>
                {/if}
            </Step>
        {/each}
        </div>
    </section>

</main>

