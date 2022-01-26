<script>
    let todo = '';
    import { addTodo,deleteTodo,toggleTodoCompleted } from "../stores/todoStore";
    const handleSubmit = () => {
        addTodo(todo);
        todo = "";
        console.log("submitting");
    }
</script>

<form class="my-6" on:submit|preventDefault={handleSubmit}>
    <div class="flex flex-col text-sm mb-2">
        <label class="font-bold mb-2 text-gray-800" for="todo">Todo</label>
        <input type="text" name="todo" placeholder="Wacha doing" bind:value={todo} class="appearence-none shadow-sm border border-gray-200 p-2 focus:outline-none focus:border-gray-500 rounded-lg">
    </div>
    <button type="submit" class="bg-blue-500 w-full shadow-sm rounded  hover:bg-blue-600 text-white py-2 px-4">Submit</button>
</form>