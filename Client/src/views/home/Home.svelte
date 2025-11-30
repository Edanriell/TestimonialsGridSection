<script lang="ts">
    import {Testimonial} from "@shared/ui/testimonial";

    const testimonials = [
        {
            authorImageSrc: "images/raster/authors/Daniel_Clifford.jpg",
            authorImageAlt: "Daniel Clifford",
            authorFullName: "Daniel Clifford",
            authorOccupation: "Verified Graduate",
            title: "I received a job offer mid-course, and the subjects I learned were current, if not more so, in the company I joined. I honestly feel I got every penny’s worth.",
            quote: "I was an EMT for many years before I joined the bootcamp. I’ve been looking to make a transition and have heard some people who had an amazing experience here. I signed up for the free intro course and found it incredibly fun! I enrolled shortly thereafter. The next 12 weeks was the  best - and most grueling - time of my life. Since completing the course, I’ve  successfully switched careers, working as a Software Engineer at a VR startup.",
            bgColor: "var(--color-purple-500)",
            titleColor: "var(--color-white)",
            textColor: "var(--color-purple-50)",
            quoteSvg: true,
        },
        {
            authorImageSrc: "images/raster/authors/Jonathan_Walters.jpg",
            authorImageAlt: "Jonathan Walters",
            authorFullName: "Jonathan Walters",
            authorOccupation: "Verified Graduate",
            title: "The team was very supportive and kept me motivated",
            quote: "I started as a total newbie with virtually no coding skills. I now work as a mobile engineer for a big company. This was one of the best investments I’ve made in myself.",
            bgColor: "var(--color-grey-500)",
            titleColor: "var(--color-white)",
            textColor: "var(--color-grey-100)"
        },
        {
            authorImageSrc: "images/raster/authors/Kira_Whittle.jpg",
            authorImageAlt: "Kira Whittle",
            authorFullName: "Kira Whittle",
            authorOccupation: "Verified Graduate",
            title: "Such a life-changing experience. Highly recommended!",
            quote: "Before joining the bootcamp, I’ve never written a line of code. I needed some structure from professionals who can help me learn programming step by step. I was encouraged to enroll by a former student of theirs who can only say wonderful things about the program. The entire curriculum and staff did not disappoint. They were very hands-on and I never had to wait long for assistance. The agile team project, in particular, was outstanding. It took my learning to the next level in a way that no tutorial could ever have. In fact, I’ve often referred to it during interviews as an example of my developent experience. It certainly helped me land a job as a full-stack developer after receiving multiple offers. 100% recommend!",
            bgColor: "var(--color-white)",
            titleColor: "var(--color-grey-500)",
            textColor: "var(--color-grey-400)"
        },
        {
            authorImageSrc: "images/raster/authors/Jeanette_Harmon.jpg",
            authorImageAlt: "Jeanette Harmon",
            authorFullName: "Jeanette Harmon",
            authorOccupation: "Verified Graduate",
            title: "An overall wonderful and rewarding experience",
            quote: "Thank you for the wonderful experience! I now have a job I really enjoy, and make a good living while doing something I love.",
            bgColor: "var(--color-white)",
            titleColor: "var(--color-grey-500)",
            textColor: "var(--color-grey-400)"
        },
        {
            authorImageSrc: "images/raster/authors/Patrick_Abrams.jpg",
            authorImageAlt: "Patrick Abrams",
            authorFullName: "Patrick Abrams",
            authorOccupation: "Verified Graduate",
            title: "Awesome teaching support from TAs who did the bootcamp themselves. Getting guidance from them and learning from their experiences was easy.",
            quote: "The staff seem genuinely concerned about my progress which I find really refreshing. The program gave me the confidence necessary to be able to go out in the world and present myself as a capable junior developer. The standard is above the rest. You will get the personal attention you need from an incredible community of smart and amazing people.",
            bgColor: "var(--color-dark-blue)",
            titleColor: "var(--color-grey-200)",
            textColor: "var(--color-grey-100)"
        },
    ];
</script>

<section class="relative">
    <h1 class="sr-only">Testimonials grid section</h1>
    <ul class="grid grid-cols-1 gap-x-[2rem] tablet:grid-cols-2 tablet:gap-[2rem] desktop:grid-cols-4 desktop:grid-rows-2 desktop:gap-x-[2rem] desktop:gap-y-[1.5]">
        {#each testimonials as {
            authorImageSrc,
            authorImageAlt,
            authorFullName,
            authorOccupation,
            title,
            quote,
            bgColor,
            titleColor,
            textColor
        }, index (index)}
            <li class="relative">
                <Testimonial authorImageSrc={authorImageSrc} authorImageAlt={authorImageAlt}
                             authorFullName={authorFullName} authorOccupation={authorOccupation} title={title}
                             quote={quote} bgColor={bgColor} titleColor={titleColor} textColor={textColor}/>
            </li>
        {/each}
    </ul>
</section>