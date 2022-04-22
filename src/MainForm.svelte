<script>
export let handleSubmit
let full_gear = false, helmet = false, jacket = false, shoes = false, weapon1 = false, weapon2 = false



function onSubmit() {
    handleSubmit({full_gear, helmet, jacket, shoes, weapon1, weapon2})
}

</script>

<style>

label {
    display: inline-block
}

.form-block {   
    text-align: left;
    margin: 0 35%;
}

</style>

<div class="form-block">
    <form on:submit|preventDefault={onSubmit}>
        <input type="checkbox" name="full_gear" bind:checked={full_gear} />
        <label for="full_gear">Full Gear</label><br />
    
        <input type="checkbox" name="helmet" bind:checked={helmet} />
        <label for="helmet">Helmet</label><br />
    
        <input type="checkbox" name="jacket" bind:checked={jacket} />
        <label for="jacket">Jacket</label><br />
    
        <input type="checkbox" name="shoes" bind:checked={shoes} />
        <label for="shoes">Shoes</label><br />
    
        <input type="checkbox" name="weapon1" bind:checked={weapon1} />
        <label for="weapon1">Weapon Slot #1</label><br />
    
        <input type="checkbox" name="weapon1" bind:checked={weapon2} />
        <label for="weapon2">Weapon Slot #2</label><br />

        <input type="submit" value="Submit" />
    </form>
</div>