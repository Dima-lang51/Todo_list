<template>
  <div class="home">
    

    <list-tasks v-if="$store.state.tasks.length" />
    <no-tasks v-else />

    <button-done-sorting 
      v-if="$store.state.sorting"
    />
  </div>
</template>

<script>

//import FieldAddTask from '@/components/Todo/FieldAddTask.vue' способ плдключения выбран другой через require


export default {

  components: {
    'list-tasks' : require('@/components/Todo/ListTasks.vue').default,
    'no-tasks' : require('@/components/Todo/NoTasks.vue').default,
    'button-done-sorting' : require('@/components/Todo/ButtonDoneSorting.vue').default
  }
};
</script>



    ButtonDoneSorting