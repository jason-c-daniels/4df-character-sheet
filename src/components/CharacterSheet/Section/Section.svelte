<style>
    @import "Section.css";
</style>

<script>
    export let title;
    export let hint = "";
    export let indent = "0.15in"
</script>

<div class="section">
    <div class="header" style="padding-left:{indent}">
        <span>{title}</span>
    </div>
    <div class="content" style="padding-left:{indent}">
        {#if (hint != "")}
            <span class="hint">{hint}</span>
        {/if}
        <slot>

        </slot>
    </div>
</div>