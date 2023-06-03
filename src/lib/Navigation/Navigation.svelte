<script>
    import { drawerStore } from '@skeletonlabs/skeleton';
    import { onMount } from 'svelte';

    let logged_in = false;


    $: logged = logged_in

    function drawerClose() {
        drawerStore.close();
    }

</script>

<nav class="list-nav p-4 min-h-screen">
	<ul>
		<li><a href="/" on:click={drawerClose}>Home</a></li>
        <li><a href="/bvg" on:click={drawerClose}>Verse Generator </a></li>

        <!-- {#if !logged}
            <li><a href="/login" on:click={drawerClose}>Log In</a></li>
        {:else}
            <li><a href="/admin" on:click={drawerClose}>Your Account</a></li>
        {/if}
    -->
	</ul>
    <div class=" text-gray-500 lg:bottom-0 lg:p-4 lg:absolute ">
        <p class="text-xs"> Made with 🤍 for Him</p>
    </div>
    <div class=" text-gray-400 lg:bottom-0 lg:p-4 dark:hidden lg:absolute">
        <p class="text-xs"> Made with ❤️ for Him</p>
    </div>
</nav>