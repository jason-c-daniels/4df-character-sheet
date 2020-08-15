<style>
    @import "CharacterSheet.css";
</style>

<script context="module">

</script>

<script>
    import PageHeading from "./PageHeading";
    import Traits from "./Traits";
    import Attributes from "./Attributes";
    import Skills from "./Skills";
    import Abilities from "./Abilities";
    import ResetAndLuck from "./ResetAndLuck";

    export let character;
</script>


<div class="character-sheet">
    <PageHeading bind:name="{character.name}" bind:species={character.species} bind:role={character.role}/>
    <div class="table">

        <div class="tr">
            <div class="td border">
                <Traits bind:aspects="{character.aspects}"/>
            </div>
            <div class="td">
                <Attributes bind:attributes="{character.attributes}" bind:will={character.skills[18].value}
                            bind:physique={character.skills[12].value}/>
            </div>
        </div>

        <div class="tr">
            <div class="td border">
                <Abilities bind:stunts="{character.stunts}"/>
                <ResetAndLuck bind:fate="{character.fate}" bind:refresh="{character.refresh}"/>
            </div>
            <div class="td">
                <Skills bind:skills={character.skills}/>
            </div>
        </div>
    </div>
</div>