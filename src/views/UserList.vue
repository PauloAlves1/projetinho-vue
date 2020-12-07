<template>
    <div class="container">
        <h1>Lista de usuarios</h1>
        <b-table striped hover :items="userList"></b-table>
    </div>
</template>

<script>
export default {
    name: 'UserList',
    data() {
        return {
            userList: [
                {
                    email: 'pikachu@hotmail.com',
                    name: 'pikachu',
                    lastName: 'raiozo'
                },
                {
                    email: 'charizard@hotmail.com',
                    name: 'charizard',
                    lastName: 'fogaço'
                },
                {
                    email: 'charmander@hotmail.com',
                    name: 'charmander',
                    lastName: 'foguinho'
                },

            ]
        }
    }

}
</script>