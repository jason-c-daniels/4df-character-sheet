<style>
    @import "Skills.css";
</style>

<script context="module">
    export function getDefaultSkillList() {
       return [
            { name: 'Bows/Crossbow', value:0 },
            { name: 'Detect Lies', value:0 },
            { name: 'Disguise', value:0 },
            { name: 'Driving (caravans, cattle)', value:0 },
            { name: 'Etiquette', value:0 },
            { name: 'Locks', value:0 },
            { name: 'Lore (                                           )', value:0  },
            { name: 'Lore (                                           )', value:0  },
            { name: 'Lore (                                           )', value:0  },
            { name: 'Melee Weapons', value:0 },
            { name: 'Navigation', value:0 },
            { name: 'Observation', value:0 },
            { name: 'Persuasion', value:0 },
            { name: 'Riding ', value:0 },
            { name: 'Siege Weapons', value:0 },
            { name: 'Sleight of Hand', value:0 },
            { name: 'Smithing', value:0 },
            { name: 'Stealth', value:0 },
            { name: 'Strategy', value:0 },
            { name: 'Survival', value:0 },
            { name: 'Thrown Weapon', value:0 },
            { name: 'Tracking ', value:0 },
            { name: 'Tradecraft (                                )', value:0  },
            { name: 'Tradecraft (                                )', value:0  },
            { name: 'Tradecraft (                                )', value:0  },
            { name: 'Unarmed Combat', value:0 }
        ];
    }
</script>


<script>
    import Section from '../Section';

    export let skills = getDefaultSkillList();

    let skillsHint = "Start with one Great (+4), two Good (+3), three Fair (+2), four Average (+1), rest at Mediocre (=0)"
    skillsHint = "";
</script>

<Section title="Skills" hint="{skillsHint}">

    {#each skills as skill}
        <div class="skill-line">
            <span>+</span>
            <input maxlength="2" type="number" class="skill-value" min="0" max="10" bind:value={skill.value}/>
            <input type="text" maxlength="50" bind:value={skill.name} style="width:12em;"/>
        </div>
    {/each}

</Section>
