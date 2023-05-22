<script>
  import { Drawer, Button } from 'flowbite-svelte';

  let navigationHidden = true;
</script>

<Drawer transitionType="fly" bind:hidden={navigationHidden}>
  <nav class="flex flex-col items-start text-2xl">
    <button class="px-4 py-2 hover:text-green-400">Projects</button>
    <button class="px-4 py-2 hover:text-green-400">About</button>
    <button class="px-4 py-2 hover:text-green-400">Contact</button>
  </nav>
</Drawer>

<div class="h-20 w-full bg-black absolute text-white flex items-center">
  <div class="px-4 text-4xl">matbmp</div>
  <a
    href="https://github.com/matbmp/"
    class="ms-auto italic px-4 text-2xl flex items-center text-white bg-white/25 rounded-2xl mx-4"
  >
    Github
  </a>

  <div class="hidden">
    <nav class="ms-auto px-4 text-xl hidden md:block">
      <button class="px-4 hover:text-green-400">Projects</button>
      <button class="px-4 hover:text-green-400">About</button>
      <button class="px-4 hover:text-green-400">Contact</button>
    </nav>
    <div class="ms-auto md:hidden">
      <button class="mx-4" on:click={() => (navigationHidden = false)}
        >Nav</button
      >
    </div>
  </div>
</div>
<div class="h-screen flex flex-col justify-center">
  <div
    class="mx-auto w-5/6 lg:w-1/3 moving-border"
  >
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
    <br>
    <div class='flex justify-center text-4xl pt-16 font-bold'>↓ My projects ↓</div>
  </div>
</div>

<div class="flex items-center">
  <div class="mx-auto w-7/8 lg:w-2/3">
    <a
      target="_blank"
      rel="noopener noreferrer"
      href="https://shareitpoland.netlify.app/"
    >
      <div class="bg-amber-200 p-4 m-4">
        <div class="py-4">
          <span class="text-6xl">ShareIt</span>
          <p class="text-2xl text-slate-700">
            Simple reddit copycat with accounts, posts, comments, and likes.
          </p>

          <p class="text-slate-500 text-xl">
            Created with <span class="text-amber-500 font-bold"
              >Svelte hosted on Netlify</span
            >
            and
            <span class="text-purple-500 font-bold"
              >ASP.NET hosted on Digital Ocean</span
            >
          </p>
        </div>
        <img alt="lumen" src="shareit.png" />
      </div>
    </a>

    <a
      target="_blank"
      rel="noopener noreferrer"
      href="https://matbmp.github.io/lumen/"
    >
      <div class="bg-amber-200 p-4 m-4">
        <div class="py-4">
          <span class="text-6xl">Lumen</span>
          <p class="text-2xl text-slate-700">
            Tiny utility website for creating CSS gradients.
          </p>
          <p class="text-slate-500 text-xl">
            Created with <span class="text-amber-500 font-bold"
              >Svelte hosted on Github Pages</span
            >
          </p>
        </div>
        <img alt="lumen" src="lumen.png" />
      </div>
    </a>
  </div>
</div>


