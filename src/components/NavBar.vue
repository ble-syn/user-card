<template>
  <div>
    <h1>Users</h1>
  </div>
  <nav>
    <form action="">
      <input
        type="text"
        name="search-user"
        id="search"
        placeholder="Search users"
      />
      <img class="search" src="/images/search.png" alt="search-icon" />
    </form>
    <ul class="nav-links">
      <li v-for="NavLink in NavLinks" :key="NavLink">
        <a :href="NavLink.link">{{ NavLink.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return {
      NavLinks: [
        {
          name: "Reputation",
          link: "/reputation",
        },
        {
          name: "New Users",
          link: "/new-users",
        },
        {
          name: "Voters",
          link: "/voters",
        },
        {
          name: "Editors",
          link: "/editors",
        },
        {
          name: "Moderators",
          link: "/moderator",
        },
      ],
    };
  },
};
</script>
<style scoped>
.logo h1 {
  font-weight: bolder;
  text-transform: capitalize;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 20px 0;
}
form {
  position: relative;
  width: 40%;
}
.search {
  height: 30px;
  position: absolute;
  left: 10px;
  top: 15px;
}
input {
  padding: 20px 0 20px 40px;
  border-radius: 5px;
  border: 1px solid #ccc;
  width: 100%;
}
input:focus {
  outline: gray;
}
input::placeholder {
  font-weight: 600;
}

ul {
  list-style: none;
  padding: 0;
}
.nav-links {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 25px;
}

a {
  text-decoration: none;
  color: #333;
  font-weight: 500;
  transition: all 0.3s ease-out;
}
.nav-links li a:hover {
  cursor: pointer;
  background-color: #849fff;
  color: white;
  padding: 10px 8px;
  border-radius: 5px;
}
@media screen and (max-width: 767px) {
  nav {
    flex-direction: column-reverse;
    align-items: baseline;
  }
  form{
    width: 100%;
    margin-top: 20px;
  }
}
</style>
