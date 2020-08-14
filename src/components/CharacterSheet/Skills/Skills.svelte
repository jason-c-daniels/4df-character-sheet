<style>
    @import "Skills.css";
</style>

<script>
    import Section from '../Section';
    export let skills=[
        { name: 'Detect Lies', value:0 },
        { name: 'Disguise', value:0 },
        { name: 'Driving (caravans, cattle)', value:0 },
        { name: 'Etiquette', value:0 },
        { name: 'Locks', value:0 },
        { name: 'Lore (_____________)', value:0 },
        { name: 'Lore (_____________)', value:0 },
        { name: 'Lore (_____________)', value:0 },
        { name: 'Lore (_____________)', value:0 },
        { name: 'Melee Weapons', value:0 },
        { name: 'Navigation', value:0 },
        { name: 'Observation', value:0 },
        { name: 'Persuasion', value:0 },
        { name: 'Riding ', value:0 },
        { name: 'Seige Weapons', value:0 },
        { name: 'Smithing', value:0 },
        { name: 'Stealth', value:0 },
        { name: 'Strategy', value:0 },
        { name: 'Survival', value:0 },
        { name: 'Thrown Weapon', value:0 },
        { name: 'Tracking ', value:0 },
        { name: 'Tradecraft (_____________)', value:0 },
        { name: 'Tradecraft (_____________)', value:0 },
        { name: 'Tradecraft (_____________)', value:0 },
        { name: 'Tradecraft (_____________)', value:0 },
        { name: 'Unarmed Combat', value:0 }
    ];

    let skillsHint="Start with one Great (+4), two Good (+3), three Fair (+2), four Average (+1), rest at Mediocre (=0)"
    skillsHint="";
</script>

<Section title="Skills" hint="{skillsHint}">

    {#each skills as skill}
        <div class="skill-line">
            <span>+</span>
            <input maxlength="2" type="number" class="skill-value" min="0" max="10" bind:value={skill.value}/>
            <label>{skill.name}</label>
        </div>
    {/each}

</Section>
