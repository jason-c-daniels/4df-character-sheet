<style>
    @import "Attribute.css";
</style>
<script>
    import CheckedItem, {defaultCss as CSS} from "../CheckedItem/CheckedItem.svelte";
    export let name = "";
    export let stressTaken=0;
    export let value = 0;
    let count;
    $: count = Math.trunc(1 + value / 2);
    let css={...CSS,color:'black', size:"1.0em"};
    let grayCss={...css,color:'gray',size:"1.0em"};

    function handleCheckedChanged(event) {
        stressTaken += event.detail.checked ? 1 : -1;
    }
</script>


<div class="row">
    <div class="title-column stress-track-title">
        <input style="clear-after: both" maxlength="2" type="number" class="attr-value" min="0" max="12" bind:value={value}/>
        <span style="clear-after: both">{name}</span>
    </div>
</div>
    <div class="row" >
        <div style="padding-left: 1em">
    {#each Array(6) as _, i}
        <div class="column">
            <CheckedItem css="{i<count ? css: grayCss}" number=" " checked="{i < stressTaken}" on:checkedChanged={handleCheckedChanged}/>
        </div>
    {/each}
        </div>
</div>
