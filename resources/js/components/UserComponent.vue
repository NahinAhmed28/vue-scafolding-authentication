<!--<template>-->
<!--    <div class="container">-->
<!--        <div class="row justify-content-center">-->
<!--            <div class="col-md-8">-->
<!--                <div class="card">-->
<!--                    <div class="card-header">User Component</div>-->

<!--                    <div class="card-body">-->
<!--                        I'm an user component.-->
<!--                    </div>-->
<!--                </div>-->
<!--            </div>-->
<!--        </div>-->
<!--    </div>-->
<!--</template>-->

<!--<script>-->
<!--export default {-->
<!--    mounted() {-->
<!--        console.log('Component mounted.')-->
<!--    }-->
<!--}-->
<!--</script>-->
<template>
    <div class="container">
        <div class="row mt-5">
            <div class="col-md-12">
                <div class="card">
                    <div class="card-header">
                        <h3 class="card-title">Users Table</h3>
                    </div>
                    <!-- /.card-header -->
                    <div class="card-body table-responsive p-0">
                        <table class="table table-hover">
                            <tbody>
                            <tr>
                                <th>ID</th>
                                <th>Name</th>
                                <th>Email</th>
<!--                                <th>Type</th>-->
                                <th>Registered At</th>
<!--                                <th>Modify</th>-->
                            </tr>
                            <tr v-for="user in users" :key="user.id">
                                <td>{{ user.id }} </td>
                                <td>{{ user.name }} </td>
                                <td>{{ user.email }} </td>
                                <td>{{ user.created_at }} </td>
                            </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
                <!-- /.card -->
            </div>
        </div>
    </div>
</template>

<script>

export default {


    data() {
        return {
            users: []
        }
    },
    methods: {

        loadUsers() {
            axios.get('/get_all_users').then((res)=>{
                this.users = res.data
            }).catch((err) => {
                console.log(err)
            });
        },
        // createUser() {
        //     this.form.post('api/user');
        // }
    },
    created() {
        this.loadUsers();
    }
}
</script>
