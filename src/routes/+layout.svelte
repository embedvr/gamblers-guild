<script>
    import "../app.css";
    import "@fontsource-variable/source-code-pro";
</script>

<svelte:head>
    <title>The Gamblers Guild ⚅</title>

    <meta name="title" content="The Gamblers Guild ⚅" />
    <meta
        name="description"
        content="A collective of founders & indie hackers making small bets & supporting each other"
    />

    <!-- Open Graph / Facebook -->
    <meta property="og:type" content="website" />
    <meta property="og:url" content="https://www.thegamblersguild.com/" />
    <meta property="og:title" content="The Gamblers Guild ⚅" />
    <meta
        property="og:description"
        content="A collective of founders & indie hackers making small bets & supporting each other"
    />
    <meta property="og:image" content="/meta-cover.jpg" />

    <!-- Twitter -->
    <meta property="twitter:card" content="summary_large_image" />
    <meta property="twitter:url" content="https://www.thegamblersguild.com/" />
    <meta property="twitter:title" content="The Gamblers Guild ⚅" />
    <meta
        property="twitter:description"
        content="A collective of founders & indie hackers making small bets & supporting each other"
    />
    <meta property="twitter:image" content="/meta-cover.jpg" />
</svelte:head>

<main class="min-h-screen min-w-screen flex justify-center items-center">
    <slot />
</main>
