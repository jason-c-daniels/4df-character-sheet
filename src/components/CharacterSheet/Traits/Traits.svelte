<style>
    @import "Traits.css";
</style>

<script>
    import Section from '../Section';

    export let traits = {
        concept: "",
        problem: "",
        relationship: "",
        otherTraits: ["", ""]
    };
    let rows = 2;
</script>

<Section title="Traits" indent="0.25in">
    <div class="trait" style="width: 3.5in">
        <label class="trait-label">
            <span>Concept</span>
        </label>
        <textarea placeholder="Who and/or what is this character?"
                  bind:value="{traits.concept}"
                  rows="{rows}"
                  maxlength="110"
        ></textarea>
    </div>

    <div class="trait">
        <label class="trait-label">
            <span>Problem</span>
        </label>
        <textarea placeholder="What makes this character's life difficult?"
                  bind:value="{traits.problem}"
                  rows="{rows}"
                  maxlength="110"
        ></textarea>
    </div>
    <div class="trait">
        <label class="trait-label">
            <span>Relationship</span>
        </label>
        <textarea placeholder="How did the party members team up?"
                  bind:value="{traits.relationship}"
                  rows="{rows}"
                  maxlength="110"
        ></textarea>
    </div>
    <div class="trait">
        <label class="trait-label">
            <span>Misc. Trait</span>
        </label>
        <textarea placeholder="Please describe the trait"
                  bind:value="{traits.otherTraits[0]}"
                  maxlength="110"
                  rows="{rows}"
        ></textarea>
    </div>
    <div class="trait">
        <label class="trait-label">
            <span>Misc. Trait</span>
        </label>
        <textarea placeholder="Please describe the trait."
                  bind:value="{traits.otherTraits[1]}"
                  maxlength="110"
                  rows="{rows}"
        ></textarea>
    </div>
</Section>
