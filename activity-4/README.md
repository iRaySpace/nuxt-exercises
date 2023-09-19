# Activity 4

Objectives:
- Learn how to update existing todo and submit to Spring Boot

Instructions:
- Add Edit `<button>` on every `<li>` elements
- On `<script>`, add `selectTodo: function (todo) {}`
```html
<script>
export default {
    data: function () { ... },
    methods: {
        selectTodo: function (todo) {

        },
    },
};
</script>
```
- On `data`, add `todoId`, and set `this.todoId` on `selectTodo` using `todo` data
- Don't forget to add `@click` on Edit `<button>` element `<button @click="selectTodo(todo)"></button>`
- In order to update todo, use `fetch("<PUT todo link>", { method: "PUT" })` and add `updateTodo: function () {}` 
```javascript
updateTodo: function () {
    fetch('<PUT todo link>', {
        method: 'PUT',
        body: JSON.stringify({
            id: this.todoId,
            title: this.todo,
        }),
    });
}
```
- Re-write `@click` to handle both add and update ToDo `<button>Submit</button>`

Acceptance Criteria:
- Has Edit button
- Can still create data using POST `/todo`
- Can edit data using PUT `/todo`
