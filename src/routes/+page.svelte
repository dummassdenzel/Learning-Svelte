<script lang="ts">
    import { page } from '$app/stores';
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
  $: activeUrl = $page.url.pathname;
</script>


<Navbar>
    <NavBrand href="/">
      <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">Denzel Manz Perez</span>
    </NavBrand>
    <NavHamburger />
    <NavUl {activeUrl}>
        <NavLi href="/home">Home</NavLi>
        <NavLi href="/hello-world">Hello World</NavLi>
    </NavUl>
</Navbar>
<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<p class="text-blue-500">If this is blue, tailwind works.</p>
