<template>
  <img src="/img/Umbra-1.png" alt="Umbra" />
  <div class="container">
    <h1>Umbra</h1>
    <p>A game about <span style="font-weight: bold">shadows</span>.</p>

    <div class="card">
      <h2>2023 Game of the Year</h2>
      <p>
        Umbra is showcased in the 2023 and 2024 Year-End Showcases of UBC Game
        Development Club and was awarded the Game of the Year title in 2023.
      </p>
    </div>

    <div class="card">
      <h2>Release Date</h2>
      <p>
        Umbra is actively under development. The planned Early Access release
        date is around early 2025. Come back later for more updates!
      </p>
    </div>

    <div class="card">
      <h2>Team Members</h2>
      <ul>
        <li v-for="(member, ind) in members" :key="ind">
          {{ member.name }} - {{ member.roles.join(", ") }}
        </li>
      </ul>
      <h3>Previous Members</h3>
      <ul>
        <li v-for="(member, ind) in pastMembers" :key="ind">
          {{ member.name }} - {{ member.roles.join(", ") }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
const members = ref([
  {
    name: "William Zhou",
    roles: ["Team Lead", "Programming", "Music"],
  },
  {
    name: "Bailey Brantingham",
    roles: ["3D Modeling", "Programming"],
  },
  {
    name: "Alexandria Vido",
    roles: ["3D Modeling"],
  },
  {
    name: "Xue Huang",
    roles: ["Art"],
  },
  {
    name: "Litong",
    roles: ["Art"],
  },
  {
    name: "Eric Guzman Skotnitsky",
    roles: ["Programming"],
  },
  {
    name: "Ryan Bui",
    roles: ["Programming"],
  },
  {
    name: "Diana Wan",
    roles: ["Programming"],
  },
  {
    name: "Allen Chiang",
    roles: ["Story"],
  },
]);

const pastMembers = ref([
  {
    name: "Emma Greville",
    roles: ["Art", "Programming"],
  },
  {
    name: "Kaitlyn Russell",
    roles: ["Art"],
  },
  {
    name: "Dean Yang",
    roles: ["Programming"],
  },
]);
</script>

<style lang="scss" scoped>
img {
  width: 100%;
  max-height: min(80vh, calc(100vh - 220px));
  object-fit: contain;
}
</style>
