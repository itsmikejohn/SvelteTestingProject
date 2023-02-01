<script>
    import { createEventDispatcher } from "svelte";
    const dispatcher = createEventDispatcher();
    export let items = " ";
    export let activeItem =" ";

    const onKey = () => {

    }
</script>

<div class="tabs">
    <ul>
        {#each items as value}
        <li on:keypress={onKey} on:click={()=>{dispatcher("tabChanger", value)}}>
            <div class:active={value === activeItem}>{value}</div>
        </li>
        {/each}
    </ul>

</div>

<style>
    .tabs {
        margin-bottom: 30px;
    }

    ul{
        display: flex;
        justify-content: center;
        padding: 0;
        list-style-type: none;
    }

    li{
        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif ;
        margin: 0 16px;
        font-size: 20px;
        font-weight: 900;
        color:whitesmoke;
        cursor: pointer;
    }

    li:hover {
        padding-top: 10px;
        transition: 0.5s;
    }

    .active {
        color: red;
        border-bottom: 2px solid red;
        padding-bottom: 8px;
    }
</style>