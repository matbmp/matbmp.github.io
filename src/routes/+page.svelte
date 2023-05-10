<script>
  import { Drawer, Button } from "flowbite-svelte";

  let navigationHidden = true;
</script>

<Drawer transitionType="fly"  bind:hidden={navigationHidden}>
  <nav class="flex flex-col items-start text-2xl">
    <button class="px-4 py-2 hover:text-green-400">Projects</button>
    <button class="px-4 py-2 hover:text-green-400">About</button>
    <button class="px-4 py-2 hover:text-green-400">Contact</button>
  </nav>
</Drawer>

<div class="h-16 w-full bg-black absolute text-white flex items-center">
  <div class="px-4 text-4xl">matbmp</div>
  <div class="italic text-2xl flex items-center text-rose-500">
    in construction
  </div>

  <nav class="ms-auto px-4 text-xl hidden md:block">
    <button class="px-4 hover:text-green-400">Projects</button>
    <button class="px-4 hover:text-green-400">About</button>
    <button class="px-4 hover:text-green-400">Contact</button>
  </nav>
  <div class="ms-auto md:hidden">
    <button class="mx-4" on:click={() => (navigationHidden = false)}>Nav</button
    >
  </div>
</div>
<div class="h-screen flex items-center">
  <div class="mx-auto w-5/6 lg:w-1/3">
    <span class="text-4xl">
      Hi, I am <span class="text-green-400">Mateusz Biernacki</span>,<br />
      a student of computer science with interests in
    </span>
    <br />
    <span class="text-2xl">
      <span class="text-purple-500">web developmnet</span><br />
      <span class="text-cyan-500">computer graphics</span><br />
      <span class="text-amber-500">computer vision</span>
    </span>
  </div>
</div>
