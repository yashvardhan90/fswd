<script>
    import TodoItem from "$lib/todo-item.svelte";
    
    const title = "Todo";
</script>

<svelte:head>
    <title>{title}</title>
</svelte:head>

<style>
    .todos {
        width: 100%;
        max-width: 42rem;
        margin: 4rem auto 0 auto;
    }

    .new {
        margin: 0 0 0.5rem 0;
    }

    .new input {
        font-size: 28px;
        width: 100%;
        padding: 0.5rem 1em 0.3rem 1em;
        box-sizing: border-box;
        border-radius: 8px;
        background: rgba(255, 255, 255, 0.05);
        text-align: center;
    }

    .todos :global(input) {
    border: 1px solid transparent;
    }

    .todos :global(input:focus-visible) {
    box-shadow: inset 1px 1px 6px rgba(0, 0, 0, 0.1);
    border: 1px solid #ff3e00 !important;
    outline: none;
    }
</style>

<div class="todos">
    <h1>{title}</h1>

    <form action="" method="" class="new">
        <input type="text" name="text" aria-label="Add a todo" placeholder="+ tap to add a todo">
    </form>

    <TodoItem />
    <TodoItem />
</div>