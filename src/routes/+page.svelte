<script>
  import { Button, buttonVariants } from "$lib/components/ui/button";
  import * as Dialog from "$lib/components/ui/dialog";
  import { Input } from "$lib/components/ui/input";
  import { Label } from "$lib/components/ui/label";
  import Tablerow from "$lib/components/ui/Tablerow.svelte";
  import {
    Dice,
    Discord,
    Email,
    HandShake,
    Forum,
    Name,
  } from "$lib/components/ui/ascii";

  let members = [
    { name: "Akira", twitter: "akirathedev", joinDate: "30/10/2023" },
  ];
</script>

<div class="flex flex-col gap-8 md:gap-16 items-center text-center px-8 py-8">
  <Dice />
  <div class="flex flex-col md:flex-row">
    <Name />
  </div>
  <div class="flex flex-col gap-8 items-center">
    <p>
      Building stuff can be lonely, overwhelming and tiring, so we're doing it
      together.
    </p>
    <p class="text-gray-300">
      A small, private community of founders & indie hackers making small bets
      and supporting each other.
    </p>
    <Dialog.Root>
      <Dialog.Trigger class={buttonVariants({ variant: "outline" })}>
        Apply
      </Dialog.Trigger>
      <Dialog.Content class="sm:max-w-[425px]">
        <Dialog.Header>
          <Dialog.Title>Join The Gamblers Guild</Dialog.Title>
          <Dialog.Description>
            We're a private but inclusive group. If you'd like to join, send
            through your details and we'll reach out.
          </Dialog.Description>
        </Dialog.Header>
        <form
          action="https://api.sheetmonkey.io/form/eKNhm9DsCrqH4RLzp5QZX"
          method="post"
          class="grid gap-4 py-4"
        >
          <div class="grid grid-cols-4 items-center gap-4">
            <Label class="text-right">Twitter/X</Label>
            <Input id="username" class="col-span-3" name="Twitter" required />
          </div>
          <div class="grid grid-cols-4 items-center gap-4">
            <Label class="text-right">Email</Label>
            <Input
              id="email"
              name="Email"
              class="col-span-3"
              type="email"
              required
            />
          </div>
          <input
            type="hidden"
            name="Created"
            value="x-sheetmonkey-current-date-time"
          />
          <Dialog.Footer>
            <Button type="submit" value="Sign Up">Submit</Button>
          </Dialog.Footer>
        </form>
      </Dialog.Content>
    </Dialog.Root>
  </div>
  <div
    class="flex flex-col max-w-sm md:flex-row gap-8 justify-center md:max-w-screen-lg items-center mt-8"
  >
    <div class="flex flex-col gap-4 items-center w-full">
      <Forum />
      <p>⚀ Forum</p>
      <p class="text-gray-300">
        A message board for weekly check-ins and long-form discussions
      </p>
    </div>
    <div class="flex flex-col gap-4 items-center w-full">
      <Discord />
      <p>⚁ Discord</p>
      <p class="text-gray-300">
        A Discord server for quick feedback and help requests
      </p>
    </div>
    <div class="flex flex-col gap-4 items-center w-full">
      <Email />
      <p>⚂ Email</p>
      <p class="text-gray-300">
        A weekly email round-up to highlight achievements
      </p>
    </div>
  </div>
  <div class="flex flex-col gap-4">
    <div class="flex flex-col gap-4">
      <p>Founding Members</p>
      <p class="text-gray-300">⚀ ⚁ ⚂ ⚃ ⚄ ⚅</p>
    </div>
    <HandShake />
    <ul class="flex flex-col gap-4 max-w-screen-sm justify-between">
      <Tablerow />
      {#each members as member}
        <Tablerow {...member} />
      {/each}
    </ul>
  </div>
  <div class="flex flex-col gap-2">
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
</div>
