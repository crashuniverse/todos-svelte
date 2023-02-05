<script>
    export let tasks = [
        'walk in the park',
        'take a picture of clouds',
        'visit school',
    ];
    export let description;

    function handleClick() {
        tasks = tasks.concat(description);
    }
</script>

<h2>Tasks</h2>
<ul>
    {#each tasks as task}
        <li>{task}</li>
    {/each}
</ul>

<h2>Add task</h2>
<label for=description>
    <input name=description bind:value={description} />
</label>
<div>
    <br />
    <button on:click={handleClick}>Add task</button>
</div>

<style>
</style>