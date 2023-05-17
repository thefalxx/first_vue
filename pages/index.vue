<template>
<div>
    <h1 class="text-xl font-bold mb-2">Notes</h1>
    <p class="mb-4">built with nuxt 3</p>
    <ul class="border shadow divide-y">
      <li v-for="note of filteredNotes" :key="note.id">
        <NuxtLink :to="`${note.id}`" class="flex flex-col hover:bg-gray-50 p-3">
          <span class="font-bold text-lg">{{ note.title }}</span>
          <span>completed: {{ note.completed }}</span>
        </NuxtLink>
      </li>
    </ul>
  </div>
</template>

