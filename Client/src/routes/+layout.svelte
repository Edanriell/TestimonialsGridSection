<script lang="ts">
    import "@app/styles/styles.css";

    import {DefaultLayout} from "@widgets/layouts/default";

    let {children} = $props();
</script>

<DefaultLayout>
    {@render children?.()}
</DefaultLayout>