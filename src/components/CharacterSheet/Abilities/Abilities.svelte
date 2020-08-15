<style>
    @import "Abilities.css";
</style>

<script>
    import Section from '../Section';

    export let abilities = [
        {name: "", description: ""},
        {name: "", description: ""},
        {name: "", description: ""},
        {name: "", description: ""},
        {name: "", description: ""},
        {name: "", description: ""}
    ];
    let rows = 3;
    let stuntsHint = "Start with three abilities for free. You may buy additional abilities for 1 Refresh each, so long as your Refresh remains at 1 or above."
    stuntsHint = "";
</script>

<Section title="Special Abilities" hint="{stuntsHint}" indent="0.25in">

    {#each abilities as ability,i}
        <div class="stunt">
            <input type="text" maxlength="40" class="name-input" placeholder="Please name the ability."
                   bind:value={ability.name}/>
            <textarea placeholder="Please describe the ability."
                      bind:value="{ability.description}"
                      maxlength="130"
                      rows="{rows}"></textarea>
        </div>
    {/each}
</Section>

<br/>
