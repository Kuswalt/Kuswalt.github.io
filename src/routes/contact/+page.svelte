<script>
    import Step from "$lib/Step.svelte";

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
            description: "Chris Jen Roa",
        },
    ];
</script>


<section class="py-20 lg:py-32 flex flex-col gap-24" id="social-info">
    <div class="flex flex-col gap-2 text-center">
        <h6 class="text-large sm:text-xl md:text-2xl"style="font-family: 'Afacad Flux', sans-serif;">
            Connect with Me.
        </h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl"style="font-family: 'Afacad Flux', sans-serif;">
            Reach me on my <span class="poppins text-blue-400"style="font-family: 'Afacad Flux', sans-serif;">social media</span>
        </h3>
    </div>

    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
        {#each socials as social}
            <Step project={social}>
                {#if social.link}
                <a href={social.link} class="text-blue-400 hover:text-white duration-200 relative after:absolute after:top-0 after:h-full after:left-0 after:w-0 after:duration-200 hover:after:w-full after:z-[-1] overflow-hidden" target="_blank" rel="noopener noreferrer">{social.description}</a>
                {:else}
                    <p style="font-family: 'Afacad Flux', sans-serif;">{social.description}</p>
                {/if}
            </Step>
        {/each}
    </div>
</section>