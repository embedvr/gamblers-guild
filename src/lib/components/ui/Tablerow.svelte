<script>
    let { name, twitter, joinDate } = $$props;
</script>

<li class="grid grid-cols-1 sm:grid-cols-3 sm:gap-8 grow">
    {#if name}
        <p class="text-gray-300">
            {name}
        </p>
    {:else}
        <p class="hidden sm:block">Name</p>
    {/if}

    {#if twitter}
        <a
            href={`https://twitter.com/${twitter}`}
            target="_blank"
            class="text-gray-300"
        >
            {twitter}
        </a>
    {:else}
        <p class="hidden sm:block">Twitter</p>
    {/if}

    {#if joinDate}
        <p class="text-gray-300">
            {joinDate}
        </p>
    {:else}
        <p class="hidden sm:block">Join Date</p>
    {/if}
</li>
