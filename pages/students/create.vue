<template>
    <div class="mt-5 mx-5">
        <h1>Student create page</h1>
        <div class="card">

            <div class="card-header">
                <h4>
                    Add Student <NuxtLink to="/" class="btn btn-danger float-end">Back</NuxtLink>
                </h4>
            </div>
            <div class="card-body">
                <div v-if="isLoading">
                    <loading :title="isLoadingTitle"/>
                </div>
                <div v-else>
                    <form @submit.prevent="saveStudent">
                    <div class="mb-3">
                        <label for="">Name</label>
                        <input type="text" v-model="student.name" class="form-control" name="" id="">
                    </div>
                    <div class="mb-3">
                        <label for="">Course</label>
                        <input type="text" v-model="student.course" class="form-control" name="" id="">
                    </div>
                    <div class="mb-3">
                        <label for="">Email</label>
                        <input type="text" v-model="student.email" class="form-control" name="" id="">
                    </div>
                    <div class="mb-3">
                        <label for="">Phone</label>
                        <input type="text" v-model="student.phone" class="form-control" name="" id="">
                    </div>
                    <div class="mb-3">
                        <button type="submit" class="btn btn-primary">Save</button>
                    </div>

                </form>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "studentCreate",
    data() {
        return {
            student: {
                name: '',
                course: '',
                email: '',
                phone: '',
            },
            isLoading: false,
            isLoadingTitle: 'Loading'
        }
    },
    methods: {
        saveStudent() {
            this.isLoading = true;
            this.isLoadingTitle = "Saving";
            // alert("Submit data successfully")
        }
    }
}
</script>