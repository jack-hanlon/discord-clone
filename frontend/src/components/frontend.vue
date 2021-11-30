<template>


  <div id="rooms-container">
    <h1>Cool Rooms</h1>
    <div>{{rooms}}</div>
  </div>


</template>


<script>

export default {
  name: "frontend",
  data: () => ({
    rooms: {},
  }),
  props: {
    updateRooms: Array
  },
  methods: {
    async getRooms() {
      let response = await fetch('http://127.0.0.1:8000/api/rooms/')
      let rooms = await response.json()
      let tmp = []
      for(let i = 0; i < rooms.length; i++){
        tmp[i] = rooms[i].name
      }
      return this.rooms = tmp

    }
  },
  created(){
    this.getRooms();
  }
}

</script>
