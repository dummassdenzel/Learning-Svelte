<script lang="ts">
    import { Alert } from 'flowbite-svelte';
    import { InfoCircleSolid } from 'flowbite-svelte-icons';
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
        <NavLi href="../">Default</NavLi>
        <NavLi href="/hello-world">Hello World</NavLi>
    </NavUl>
</Navbar>

    <Alert>
        <InfoCircleSolid slot='icon'/>
        <span class="font-medium">Welcome to the Home page!</span>
    </Alert>

    <h1 class="font-bold text-center mt-6">You are in the Home page</h1>