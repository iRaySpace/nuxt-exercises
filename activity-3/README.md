# Activity 3

Objectives:
- Learn how to use `<input>` and bind input using `v-model` 
- Submit binded input to Spring Boot backend

Instructions:
- Add `todo` on `return {}` for the input bind
```html
<script>
export default {
    data: function () {
        return {
            todos: [],
            todo: "",
        };
    },
};
</script>
```
- Add `<input type="text" v-model="todo">`, `v-model` will bind the input to `todo`, this means that every input changes, it will update `todo`
- Add `<button>Submit</button>`
- On `<script>`, add `addTodo() {}`
```html
<script>
export default {
    data: function () {
        return {
            todos: [],
            todo: "",
        };
    },
    methods: {
        addTodo: function () {

        },
    },
};
</script>
```
- Add new ToDo, by using `fetch("<POST todo link>", { method: "POST" })` and `this.todo` value
```javascript
addTodo: function () {
    fetch('<POST todo link>', {
        method: 'POST',
        body: JSON.stringify({
            title: this.todo,
        }),
    });
}
```

Acceptance Criteria:
- Has input field and submit
- Save data using POST `/todo`
