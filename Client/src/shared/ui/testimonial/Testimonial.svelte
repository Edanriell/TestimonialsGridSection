<script lang="ts">
    interface Props {
        authorImageSrc: string;
        authorImageAlt: string;
        authorFullName: string;
        authorOccupation: string;
        title: string;
        quote: string;
        bgColor: string;
        titleColor: string;
        textColor: string;
        imageBorderColor: string;
        authorTextColor: string;
        authorOccupationTextColor: string;
        quoteSvg?: boolean;
    }

    let {
        authorImageSrc,
        authorImageAlt,
        authorFullName,
        authorOccupation,
        title,
        quote,
        bgColor,
        titleColor,
        textColor,
        imageBorderColor,
        authorTextColor,
        authorOccupationTextColor,
        quoteSvg = false
    }: Props = $props();
</script>

<article
        style="
            --bg-color: {bgColor};
            --title-color: {titleColor};
            --text-color: {textColor};
            --img-border-color: {imageBorderColor};
            --author-text-color: {authorTextColor};
            --author-occupation-text-color: {authorOccupationTextColor};
        "
        class="relative w-full h-full rounded-[0.5rem] p-[2rem] bg-[var(--bg-color)] shadow-[40px_60px_50px_-47px_rgba(72,85,106,0.25)]">
    {#if quoteSvg}
        <svg class="hidden z-0 absolute top-0 w-[6.5rem] h-[6.375rem] tablet:block tablet:right-[10.438rem] desktop:right-[3.75rem]"
             fill="none" height="102"
             viewBox="0 0 104 102"
             width="104"
             xmlns="http://www.w3.org/2000/svg">
            <path clip-rule="evenodd"
                  d="M42 59.7268V102H0V75.7394C0 59.9403 1.48485 47.9042 4.45455 39.6311C7.42424 31.3579 12.0114 23.752 18.2159 16.8132C24.4205 9.87441 32.3485 4.27002 42 0V19.3752C36.9091 22.2575 33.0114 25.8603 30.3068 30.1837C27.6023 34.5071 25.5606 39.044 24.1818 43.7943C22.803 48.5447 22.1136 53.8556 22.1136 59.7268H42ZM104 59.7268V102H62V75.7394C62 59.9403 63.4848 47.9042 66.4545 39.6311C69.4242 31.3579 73.9848 23.752 80.1364 16.8132C86.2879 9.87441 94.2424 4.27002 104 0V19.3752C98.9091 22.2575 95.0114 25.8603 92.3068 30.1837C89.6023 34.5071 87.5606 39.044 86.1818 43.7943C84.803 48.5447 84.1136 53.8556 84.1136 59.7268H104Z"
                  fill="#A775F1"
                  fill-rule="evenodd"/>
        </svg>
    {/if}
    <figure class="relative z-10">
        <figcaption class="relative">
            <div class="flex flex-row items-center gap-x-[1.063rem]">
                <enhanced:img alt="{authorImageAlt}"
                              class="rounded-full relative block w-[1.75rem] h-[1.75rem] border-[red] border-[var(--img-border-color)] border-[0.125rem]"
                              src="{authorImageSrc}"/>
                <div class="flex flex-col gap-y-[0.25rem]">
                    <cite class="font-[Barlow] font-medium text-[0.813rem] leading-[110%] text-[var(--author-text-color)] not-italic">{authorFullName}</cite>
                    <small class="font-[Barlow] font-medium text-[0.688rem] leading-[110%] text-[var(--author-occupation-text-color)]">{authorOccupation}</small>
                </div>
            </div>
        </figcaption>
        <h2 class="mt-[1rem] font-[Barlow] font-semibold! text-[1.25rem] leading-[120%] text-[var(--title-color)] text-pretty">{title}</h2>
        <blockquote
                class="mt-[1rem] font-[Barlow] font-medium! text-[0.813rem] leading-[140%] text-[var(--text-color)] text-pretty">
            “ {quote} ”
        </blockquote>
    </figure>
</article>