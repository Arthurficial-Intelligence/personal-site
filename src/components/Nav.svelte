<script>
    import { onMount } from "svelte";
    import { browser } from "$app/environment"; // import the browser package
    import { goto } from "$app/navigation"; // for client-side navigation

    let currentPath = "";

    onMount(() => {
        if (browser) {
            currentPath = window.location.pathname;
            // Listen to the history changes and update the current path
            window.addEventListener("popstate", () => {
                currentPath = window.location.pathname;
            });
        }
    });

    const navigate = (path) => {
        currentPath = path;
        goto(path);
    };
</script>

<nav>
    <h3>AI</h3>
    <ul>
        <li>
            <a
                href="/"
                on:click|preventDefault={() => navigate("/")}
                class={currentPath === "/" ? "active" : ""}>Home</a
            >
        </li>
        <li>
            <a
                href="/about"
                on:click|preventDefault={() => navigate("/about")}
                class={currentPath === "/about" ? "active" : ""}>About</a
            >
        </li>
        <li>
            <a
                href="/portfolio"
                on:click|preventDefault={() => navigate("/portfolio")}
                class={currentPath === "/portfolio" ? "active" : ""}
                >Portfolio</a
            >
        </li>
    </ul>
</nav>

<style>
    h3 {
        color: orange;
        font-size: 32px;
    }
    nav {
        width: 120px;
        height: 100vh;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        border-right: 1px solid orange;
        margin-right: 16px;
    }

    ul {
        padding-left: 0;
    }

    li {
        list-style: none;
    }
    li:not(:last-child) {
        margin-bottom: 16px;
    }

    a {
        text-decoration: none;
    }
    a:hover {
        color: orange;
        text-decoration: underline;
    }
    a.active {
        color: orange;
        text-decoration: underline;
    }
</style>
