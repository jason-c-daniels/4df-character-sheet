<style>
    @import "ResetAndLuck.css";
</style>

<script>
    export let reset = 3;
    export let luck = 3;
</script>


<div class="header">
    <div style="display: inline-block">&nbsp;</div>
    <div class="reset-points">
        <input
                maxlength="1"
                class="circle"
                type="number"
                step={1}
                min={0}
                max={10}
                bind:value={reset}
        />
    </div>
    <div class="reset-label">
        <span style="margin-left:5.3em">Reset</span>
    </div>
    <div class="luck-label">
        <span style="margin-right:5.3em">Luck</span>
    </div>
    <div class="luck-points">
        <input
                maxlength="1"
                class="circle"
                type="number"
                step={1}
                min={0}
                max={10}
                bind:value={luck}
        />
    </div>
</div>
