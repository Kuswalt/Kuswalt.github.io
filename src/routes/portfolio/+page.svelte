<script>
    import Step from "$lib/Step.svelte";

    // Array of project information
    let projects = [
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
</script>

<section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
    <div class="flex flex-col gap-2 text-center">
        <h6 class="text-large sm:text-xl md:text-2xl font-afacad">
            A Few of My Projects This Recent Times.
        </h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl font-afacad">
            Want to <span class="poppins text-blue-400" style="font-family: 'Afacad Flux', sans-serif;">see</span> my works?
        </h3>
    </div>

    <!-- Display each project with a description and link -->
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10 source-code-pro">
        {#each projects as project}
            <Step {project}>
                <p class="text-justify font-afacad">
                    {#if project.name === "WeatherWise"}
                        WeatherWise is a webapp weather forecast with location detection that utilizes
                        <strong class="text-blue-400"> Angular Framework</strong>, <strong class="text-blue-400">RestApi PHP</strong> & <strong class="text-blue-400">OpenWeather API </strong>to show 5 hour, 5 day weather forecasts.
                    {:else if project.name === "Formalytics"}
                        Formalytics is a group project for Application Development Course that utilizes <strong class="text-blue-400">Angular Framework</strong> & <strong class="text-blue-400">RestApi PHP</strong>. A webapp that allows a user to send questions to alumni to know their current life state and do analytical results based on the survey response.
                    {:else if project.name === "AdvCalculator"}
                        AdvCalculator is a <strong class="text-blue-400">Python</strong> built calculator, that can do basic calculations to advanced calculations. This is a project made with my friend hizzCarlo.
                    {/if}
                </p>
                <div class="flex-1 flex justify-between gap-4 items-end">
                    <div class="ml-auto cursor-pointer hover:text-white duration-200 relative after:absolute after:top-0 after:h-full after:right-full after:bg-black after:w-full after:duration-200 hover:after:translate-x-full after:z-[-1] overflow-hidden">
                        <a href={project.link} class="text-blue-400 hover:text-white">Go to &rarr;</a>
                    </div>
                </div>
            </Step>
        {/each}
    </div>
</section>