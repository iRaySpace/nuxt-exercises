# Activity 2

Objectives:
- Learn how to retrieve data from the Spring Boot backend
- Learn how to display the data retrieved

Instructions:
- Make a `/components/TodoList.vue` with the initial file structure
```html
<template>
</template>

<script>
export default {

};
<script>
```
- Make a static list using `<ul>`, and `<li>` elements
- On `export default {}`, add `mounted: function ()`, 

Read more: [mounted()](https://vuejs.org/api/options-lifecycle.html#mounted)
```html
<script>
export default {
    data: function () {
        return {
            todos: [],
        };
    },
    mounted: function () {

    }
};
</script>
```
- Call the GET `/todo` using `fetch('<GET todo link>')`
- Set the result to `this.todos`
- Use `<.. v-for="todo in todos"><..>` in order to show todos from `todos`

Acceptance Criteria:
- Displays `/todo` data