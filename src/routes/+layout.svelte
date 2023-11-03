<script>
  import "../app.css";
  import "@fontsource-variable/source-code-pro";
  import { PlausibleAnalytics } from "@accuser/svelte-plausible-analytics";
  import { page } from "$app/stores";
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

<PlausibleAnalytics />

{#if !String($page.url.pathname).startsWith("/invite")}
  <header class="w-full flex justify-center py-12">
    <ul class="flex justify-between max-w-md gap-4 sm:gap-12">
      <li><a class="underline underline-offset-4" href="/">Home</a></li>
      <li>
        <a class="underline underline-offset-4" href="/coc">Code of Conduct</a>
      </li>
      <li>
        <a
          class="underline underline-offset-4"
          href="https://twitter.com/gamblersguild"
          target="_blank">Twitter</a
        >
        ↗
      </li>
    </ul>
  </header>
{/if}

<main
  class="min-h-screen min-w-screen flex justify-center items-center overflow-x-hidden"
>
  <slot />
</main>

{#if !String($page.url.pathname).startsWith("/invite")}
  <footer class="flex flex-col gap-16 items-center justify-center my-8">
    <div class="flex flex-col gap-2 items-center">
      <p>⚀ ⚁ ⚂ ⚃ ⚄ ⚅</p>
      <p class="text-gray-300">
        Audentes Fortuna Iuvat // Fortune favors the bold
      </p>
    </div>
    <div class="flex gap-2">
      <p>Credits:</p>
      <p class="text-gray-300">
        Glitch animation by <a
          href="https://twitter.com/harry_webb98"
          target="_blank">Harry</a
        >
      </p>
    </div>
    <a href="https://twitter.com/gamblersguild" target="_blank">𝕏</a>
  </footer>
{/if}
