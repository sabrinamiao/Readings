# Vue.js (and Vuex) bug squasher cheatsheet

## v-show on template

### When you are using v-show, Vue is changing the CSS display property. The template tag in Vue does not actually create an element. Use v-if on the template tag or change the template tag into an element (div, section etc)

## Why is the ref element undefined

### Most likely you are trying to access an element that is not being rendered due to being nested somewhere within an ancestor element that has v-if directive that evaluates to false

### 1. Change the v-if to v-show

### 2. Wait until the v-if evaluates to true, then access and start using the ref element

## Why isn't my list updating? I added an item in Vuex

### If you are trying to update an an array in Vuex, using methods like push and shift won't do the trick. You need to provide a new array, otherwise it won't be able to render properly

```javascript
// WRONG

const mutations = {
  updateArray (state, todo) {
    state.list.push(todo)
  }
}

// CORRECT

const mutations = {
  addTodo (state, todo) {
    state.list = [...state.list, todo]
  }
}
```

## Are you targeting the correct property: Updating a property in Vuex state

### 1. Better naming

### 2. Try to avoid nesting unless it is necessary or suits the situation and double

### 3. Check if the path to the property is correct
