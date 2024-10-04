<template>
  <div class="container mx-auto p-4">
    <h1 class="text-2xl font-bold mb-4">Chocolate Websites and Ratings</h1>
    <ul>
      <li
        v-for="chocolate in chocolates"
        :key="chocolate.id"
        class="mb-4 p-4 border rounded shadow"
      >
        <h2 class="text-xl font-semibold">{{ chocolate.name }}</h2>
        <p>
          Website:
          <a :href="chocolate.website" target="_blank" class="text-blue-500 hover:underline">{{
            chocolate.website
          }}</a>
        </p>
        <p>Rating: {{ chocolate.rating }} / 5</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ChocolateList',
  data() {
    return {
      chocolates: [
        { id: 1, name: 'Lindt', website: 'https://www.lindt.com', rating: 4.8 },
        { id: 2, name: 'Godiva', website: 'https://www.godiva.com', rating: 4.5 },
        { id: 3, name: 'Ghirardelli', website: 'https://www.ghirardelli.com', rating: 4.7 },
        { id: 4, name: "Hershey's", website: 'https://www.hersheys.com', rating: 4.2 }
      ]
    }
  }
}
</script>

<style scoped>
/* Additional styles if needed */
</style>
