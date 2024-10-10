<script>

    let about = [
        {
            name: "a Student Developer",
            description: "For the past years, I have gone through a series of programming languages and frameworks, which ranges from HTML and CSS to PHP, Typescript, JavaScript and Python. I begin with online courses and tutorials. Online tutorials are so wonderful; I get a kick building projects from scratch. As my journey goes on, I enjoy doing everything-challenging myself whether in creating my personal website or developing some small application then learning all about it. Curiosity is something that, I think, will propel me; perseverance has always been my key to success and I am excited to keep growing in this ever-changing field!",
        },
        {
            name: "a Backend Developer",
            description: " I have experience working with technologies like SQL databases and RESTful API design. Recently, I developed a project that involved building a weather predition backend, which allowed me to implement features like weather forecasting and weather predictions. And am currently working on a project that involves building a webapp that allows users to ask questions to AI and get answers.",
        },
        {
            name: "Interested in Video Games",
            description: "I have a passion for video games. From RPGs to indie titles, I love exploring the creativity and storytelling that games offer. Gaming has been a significant part of my life, inspiring me to analyze game design, mechanics, and user experience. I enjoy discussing the latest trends in the gaming industry and discovering hidden gems that push the boundaries of interactive storytelling.",
        },
    ];
</script>


<main class="flex flex-col flex-1 p-4">
    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-blue-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-blue-700 py-4" >
            <h6 class="text-large sm:text-xl md:text- font-afacad">
                Curious to know more?
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl font-afacad">
                Here's more <span class="poppins text-blue-400"style="font-family: 'Afacad Flux', sans-serif;">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl font-afacad">
            I am . . .
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each about as item, index}
                <!-- <div class="flex gap-6 sm:gap-8">
                    <p class="poppins text-4xl sm:text-5xl md:text-6xl text-blue-500 font-semibold">
                        0{index + 1}
                    </p> -->
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl font-afacad">
                            {item.name}
                        </h3>
                        <p class="text-justify font-afacad">{item.description}</p>
                    </div>
                
            {/each}
        </div>
    </section>
</main>