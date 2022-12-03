<template>
  <div class="user-container">
    <div class="card" v-for="user in users" :key="user">
      <div class="user-img">
        <img :src="user.src" alt="" />
      </div>
      <div>
        <h3>{{ user.name }}</h3>
        <p class="location">{{ user.location }}</p>
        <div class="tag-cont">
          <p class="tag" v-for="tag in user.tags" :key="tag">{{ tag }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "UsersData",
  data() {
    return {
      users: [
        {
          name: "Lelah Nichols",
          location: "Troy, ML",
          src: "/images/ayo.jpg",
          tags: ["clothes", "stem"],
        },
        {
          name: "Jesus Weiss",
          location: "Fort Worth, TX",
          src: "/images/erik.jpg",
          tags: ["headset", "gagdet", "speed", "winter"],
        },
        {
          name: "Annie Rice",
          location: "Austin, TX",
          src: "/images/omid.jpg",
          tags: ["road", "mountain", "trip", "earth", "nature"],
        },
        {
          name: "Robert Brower",
          location: "Cincinnati, OH",
          src: "/images/timothy.jpg",
          tags: ["maintenace", "gears", "frames", "repairs"],
        },
        {
          name: "Amy Campbell",
          location: "Warrior, AL",
          src: "/images/houcine.jpg",
          tags: ["music", "disks"],
        },
        {
          name: "Anthony S. Morin",
          location: "Lyndhurst NJ",
          src: "/images/radu.jpg",
          tags: ["vintage", "electric"],
        },
      ],
    };
  },
};
</script>

<style scoped>
img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.user-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  align-items: center;
  justify-content: center;
  gap: 15px;
  margin-top: 50px;
}

.user-img {
  max-width: 80px;
  width: 100%;
  height: 80px;
  border-radius: 50%;
  overflow: hidden;
}

.card {
  padding: 25px 20px;
  border-radius: 10px;
  display: flex;
  gap: 10px;
  height: 180px;
  background-color: #fafcff;
  cursor: pointer;
  transition: box-shadow border 0.3s all;
}
.card:hover {
  border: 1px solid #ccc;
  box-shadow: 0 0 11px rgba(33, 33, 33, 0.2);
}
.location {
  margin: 5px 0;
  font-weight: 500;
  font-size: 14px;
}
.tag-cont {
  display: flex;
  flex-wrap: wrap;
}
.tag {
  border: 1px solid #ccc;
  color: #849fff;
  border-radius: 15px;
  padding: 2px 7px;
  text-align: center;
  margin: 2px;
  font-weight: 500;
  font-size: 12px;
}
</style>
