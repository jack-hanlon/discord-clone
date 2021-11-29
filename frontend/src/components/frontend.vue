<template>


  <div id="rooms-container">
    <h1>Cool Rooms</h1>
    {{rooms}}
  </div>


</template>


<script>

export default {
  name: "frontend",
  data: () => ({
    rooms: getRooms()
  }),
  props: {

  },
  methods: {
    async getRooms() {
      let response = await fetch('http://127.0.0.1:8000/api/rooms/')
      let rooms = await response.json()
      return rooms
    }


  }


</script>
