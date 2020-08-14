<style>
    @import "Attributes.css";
</style>

<script>
    import Attribute from "./Attribute";
    import Consequence from "./Consequence";
    import Section from '../Section';

    export let attributes = {
        physicalStressTaken: 0,
        mentalStressTaken: 0,
        consequences: {
            mild1: "",
            moderate: "",
            severe: "",
            mild2: "",
        }
    };
    export let will = 0;
    export let physique = 0;

    function getStressTrackCount(attr) {
        if (attr > 0) {
            if (attr > 2) {
                return 6;
            }
            return 4;
        }
        return 3;
    }
</script>

<Section title="Attributes">
    <div style="clear: both; clear-after: both; display: block;position: relative">
        <div class="row subheading">
            <span>Physical / Mental</span>
        </div>
        <div style="width:50%; float: left">

            <Attribute name="Strength" bind:stressTaken="{attributes.physicalStressTaken}"/>
            <Attribute name="Endurance" bind:stressTaken="{attributes.mentalStressTaken}"/>
            <Attribute name="Agiility" bind:stressTaken="{attributes.mentalStressTaken}"/>

        </div>
        <div style="width:50%; float: left; clear-after: both;border-left-color: black; border-left-style: solid; border-left-width: 1pt;">

            <Attribute name="Intelligence" bind:stressTaken="{attributes.physicalStressTaken}"/>
            <Attribute name="Willpower" bind:stressTaken="{attributes.mentalStressTaken}"/>
            <Attribute name="Perception" bind:stressTaken="{attributes.mentalStressTaken}"/>

        </div>
    </div>
    <div style="clear:both; clear-after: both; display: block; position: relative">
        <div class="row subheading">
            <br/>
            <span style="font-weight: bold">CONSEQUENCES</span>
        </div>

        <Consequence name="Mild" isExtra="false" value="2" bind:description="{attributes.consequences.mild1}"/>
        <Consequence name="Moderate" isExtra="false" value="4" bind:description="{attributes.consequences.moderate}"/>
        <Consequence name="Severe" isExtra="false" value="6" bind:description="{attributes.consequences.severe}"/>
    </div>
</Section>
