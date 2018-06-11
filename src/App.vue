<template>
  <div id="app">
    <header>
      <div class="navbar">
        <p class="navbar-item selected">My Tasks</p>
        <p class="navbar-item">In Progress</p>
        <p class="navbar-item">Completed</p>
      </div>
    </header>
    <content>
      <todoedit></todoedit>
      <todolist></todolist>
    </content>
    
  </div>
</template>

<script>
import todo from './components/todo'
import todoedit from './components/todo-edit'
import todolist from './components/todo-list'
export default {
  name: 'App',
  components: {
    todoedit,
    todolist
  }
}
</script>

<style lang='scss' scoped>
@import './assets/all.scss';
@import './assets/helpers/_variables.scss';


header {
  width: 100%;
  background-color: $color-blue-light;
  height: 76px;
  @include flex();
  
  .navbar {
    @include flex(space-around);
    width: $width-content;

    .navbar-item {
      @include flex();
      text-align: center;
      width: 160px;
      font-size: $fz-title;
      color: $color-blue;
      padding: 21px 0;
      line-height: 28px;
      margin: 0;
      border-bottom: 5px solid $color-blue-light;
      &.selected {
        border-bottom-color: $color-blue;
        color: $color-white;
      }
      &:hover {
        cursor: pointer;
      }
    }
  }
}
content{
  @include flex(center,flex-start);
  // border: 1px solid red;
  width: $width-content;
  margin: 0 auto;
  height: auto;
  flex-direction: column;
}
</style>
