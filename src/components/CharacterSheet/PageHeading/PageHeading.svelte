<style>
    @import "PageHeading.css";
</style>

<script>

    import Logo from "./logo.svg"

    export let name = "";
    export let species = "";
    export let role = "";

</script>


<div class="table">
    <div class="tr">
        <div class="td bottom" style="width:80%">
            <div style="display:inline-block; width:100%;margin-left:0.25in; margin-right: 0.25in">
                <div style="display: block;">
                    <label style="display: inline-block" for="name"><span class="name-label">Name</span></label>
                    <span style="display: inline-block; width:85%">
                    <input class="name-input"
                           id="name"
                           maxlength="50"
                           type="text"
                           placeholder="Name"
                           bind:value="{name}"
                           style="width: 100%"/>
                    </span>
                </div>
                <div style="display: block; width: 100%; border-top: #333333 1pt solid">
                    <div style="display: inline-block; width: auto">
                        <label style="display: inline-block; width:auto" for="species">
                            <span class="name-label">Species</span>
                        </label>
                        <span style="display: inline-block; width:auto">
                        <input class="regular-input"
                               id="species"
                               maxlength="28"
                               type="text"
                               placeholder="Species"
                               bind:value="{species}"
                               style="width: 11em"/>
                        </span>
                    </div>
                    <div style="display: inline-block; width: auto">
                        <label style="display: inline-block; width:auto" for="role">
                            <span class="name-label">Role</span>
                        </label>
                        <span style="display: inline-block; width:auto">
                        <input class="regular-input"
                               id="role"
                               maxlength="20"
                               type="text"
                               placeholder="Role"
                               bind:value="{role}"
                               style="width: 8em"/>
                        </span>
                    </div>
                </div>
            </div>
        </div>
        <div class="td bottom">
            <div class="logo">
                <Logo height="100%" width="100%"/>
            </div>
        </div>
    </div>
</div>

