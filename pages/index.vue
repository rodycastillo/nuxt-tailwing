<template>
  <div>
    <div class="m-2 rounded-sm">
      <div>
        <TitleApp />
      </div>
      <div class="p-1">
        <div class="relative flex items-center">
          <div class="absolute right-0 mr-2 h-full flex items-center">
            <button
              @click="addTask"
              class="bg-purple-400 hover:bg-blue-600 h-10 w-10 rounded-full focus:outline-none text-lg text-white font-bold"
            >
              +
            </button>
          </div>
          <input
            v-model="title"
            class="p-4 border-2 focus:outline-none rounded-full border-gray-300 w-full"
            type="text"
          />
        </div>
      </div>
      <Card
        class="m-1"
        v-for="(item, index) in task"
        :item="item.state"
        :title="item.title"
        :key="index"
        @update="item.state = true"
        @delete="deleteTask(i)"
      />
      <div class="bg-red-200 p-5 text-center m-2" v-show="this.task.length < 1">
        Ingrese Tareas
      </div>
    </div>
  </div>
</template>

<script>
import Card from "../components/Card.vue";
import TitleApp from "../components/TitleApp.vue";
export default {
  components: { Card, TitleApp },
  data() {
    return {
      task: [],
      title: ""
    };
  },
  methods: {
    addTask() {
      this.task.push({ title: this.title, state: false });
      this.title = "";
    },
    deleteTask(p) {
      this.task.splice(p, 1);
    }
  }
};
</script>
