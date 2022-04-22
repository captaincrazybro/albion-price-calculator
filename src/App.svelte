<script>
import MainForm from "./MainForm.svelte";

let mfSubmitted = false
let checkedList

function handleMFSubmit(checked) {
    checkedList = checked
    mfSubmitted = true
}
</script>

<style>
    .page {
        text-align: center;
        margin: 50px 100px;
    }

    .header {
        background-color: blueviolet;
        color: white;
        padding: 10px;
        text-align: center;        
    }
</style>

<div class="header">
    Albion Online Gear Price Calculator
</div>
<div class="page">
    {#if !mfSubmitted }
        <MainForm handleSubmit={handleMFSubmit} />
    {:else}
        {#each Object.entries(checkedList) as [name, isChecked]}
            {#if isChecked}
                
            {/if}
        {/each}
    {/if}
</div>