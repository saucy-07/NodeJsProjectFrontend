<template>
  <table>
    <tr>
      <th>User ID</th>
      <th>First Name</th>
      <th>Last Name</th>
      <th>Age</th>
      <th>Gender</th>
      <th>User Role</th>
      <th>Email Address</th>
      <th>Password</th>
      <th>Profile Picture</th>
      <th>Actions</th>
    </tr>
    <tr v-for="(user, index) in this.users" :key="index">
      <td>{{ user.userID }}</td>
      <td>{{ user.firstName }}</td>
      <td>{{ user.lastName }}</td>
      <td>{{ user.userAge }}</td>
      <td>{{ user.Gender }}</td>
      <td>{{ user.userRole }}</td>
      <td>{{ user.emailAdd }}</td>
      <td>{{ user.userPwd }}</td>
      <td>{{ user.userProfile }}</td>
      <td>
        <button class="edit">Edit</button
        ><button @click="deleteUser(user.userID)" class="delete">
          Delete
        </button>
      </td>
    </tr>
  </table>
  <router-link to=""><button class="add-product-btn">Add User</button></router-link>
</template>

<script>
import axios from "axios";
import { ref } from "vue";

export default {
  name: "AddUserView",

  data(){
    return {
    users: []
  }
  },

  mounted(){
        this.getUsers();
    },
    methods: {
        getUsers(){
            axios.get('https://node-fullstack.onrender.com/users').then(res => {
                this.users = res.data.results
                console.log(this.users)
            })
        },
        deleteUser(userID){
            console.log(userID)
            axios.delete(`https://node-fullstack.onrender.com/users/${userID}`).then(res => {
             this.getUsers();
            })
        },
    }
};
</script>

<style scoped>
table, th, td {
  border: 1px solid black;
}
table{
    width: 99%;
    margin: 10px auto 10px auto;
    background-color: black;
}
th{
    background-color: orangered;
}
td{
    background-color: white;
    width: 15%;
    text-align: center;
}
.delete, .edit{
    cursor: pointer;
    height: 40px;
    width: 90%;
    margin: 5px 5px 5px 5px;
    border: none;
    box-shadow: rgba(0, 0, 0, 0.4) 0px 2px 4px, rgba(0, 0, 0, 0.3) 0px 7px 13px -3px, rgba(0, 0, 0, 0.2) 0px -3px 0px inset;
}
.edit{
    background-color: deepskyblue;
}
.edit:hover{
    background-color: dodgerblue;
}
.edit:active{
    background-color: rgb(0, 84, 219);
}
.delete{
    background-color: orange;
}
.delete:hover{
    background-color: darkorange;
}
.delete:active{
    background-color: rgb(255, 106, 0);
}
.add-product-btn:hover{
    background-color: rgb(76, 252, 0);
}
.add-product-btn:active{
    background-color: rgb(0, 205, 0);
}
.add-product-div{
    justify-content: center;
    align-content: center;
    margin: auto auto 10px auto;
    width: 100%;
    text-align: center;
}
.add-product-btn, .add-user-btn{
    cursor: pointer;
    justify-content: center;
    margin: 0 auto 0 auto;
    width: 100px;
    border: none;
    box-shadow: rgba(0, 0, 0, 0.4) 0px 2px 4px, rgba(0, 0, 0, 0.3) 0px 7px 13px -3px, rgba(0, 0, 0, 0.2) 0px -3px 0px inset;
    background-color: rgba(4, 255, 0, 0.936);
    height: 40px;
}
</style>