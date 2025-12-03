<script lang="ts">
    import {ErrorView} from "@views/error";
    import {page} from "$app/state";
</script>

<svelte:head>
    <title>Error</title>
    <meta content="Testimonials grid section" name="description"/>
</svelte:head>

<ErrorView error={page.error} status={page.status}/>