<style>
    @import "Wound.css";
</style>

<script>
    import CheckedItem, {defaultCss as CSS} from "../CheckedItem/CheckedItem.svelte";

    export let name = "Mild";
    export let value = 2;
    export let isExtra = false;
    export let description = "";
    let css = {...CSS, color: 'black'};
    let grayCss = {...css, color: 'gray'}

</script>

<div class="row consequence">

    <div class="column">
        <CheckedItem css="{isExtra == "true" ? grayCss : css}" number="{value}" checked={description!=""}/>

    </div>
    <div class="column" style="padding-left:1em; width:90%;">
        <label class="title"><span>{name}</span></label>
        <textarea maxlength="70" rows=2 bind:value={description} placeholder="Please describe the wound"></textarea>
    </div>
</div>
