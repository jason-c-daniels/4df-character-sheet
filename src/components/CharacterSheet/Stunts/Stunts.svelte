<style>
    @import "Stunts.css";
</style>

<script>
    import Section from '../Section';

    export let stunts = [
        {name: "", description: ""},
        {name: "", description: ""},
        {name: "", description: ""},
        {name: "", description: ""},
        {name: "", description: ""},
        {name: "", description: ""}
    ];
    let rows = 3;
    let stuntsHint = "Start with three stunts for free. You may buy additional stunts for 1 Refresh each, so long as your Refresh remains at 1 or above."
    stuntsHint = "";
</script>

<Section title="Stunts" hint="{stuntsHint}" indent="0.25in">

    {#each stunts as stunt,i}
        <div class="stunt">
            <input type="text" maxlength="40" class="name-input" placeholder="Please name the stunt."
                   bind:value={stunt.name}/>
            <textarea placeholder="Please describe the stunt."
                      bind:value="{stunt.description}"
                      maxlength="130"
                      rows="{rows}"></textarea>
        </div>
    {/each}
</Section>

<br/>
