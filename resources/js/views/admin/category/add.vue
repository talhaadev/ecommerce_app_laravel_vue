<template>
    <div>
      <!-- Page Heading -->
      <h1 class="h3 mb-4 text-gray-800">Add Category</h1>
         <form class="user" @submit.prevent="register">
            <div class="form-group row">
            <div class="col-sm-6 mb-3 mb-sm-0">
                <label>Title</label>
                <input
                type="text"
                class="form-control form-control-user"
                id="exampleFirstName"
                placeholder="Title"
                v-model="title"
                />
            </div>
            <div class="col-sm-6">
                <label>Slug</label>
                <input
                type="text"
                class="form-control form-control-user"
                id="exampleLastName"
                placeholder="Seo Url"
                v-model="slug"
                />
            </div>
            </div>
            <div class="form-group">
                <label>Description</label>
            <textarea
                type="description"
                class="form-control form-control-user"
                id="exampleInputEmail"
                placeholder="Description"
                v-model="description"
            ></textarea>
            </div>
            <div class="form-group row">
            <div class="col-sm-6 mb-3 mb-sm-0">
                <label>Image</label>
                <input
                type="file"
                class="form-control form-control-user"
                id=""
                placeholder="Image"
                v-on="image"
                />
            </div>
          
            </div>
            <LoadingButton
            text="Add Category"
            v-bind:isLoading="isLoading"
            />
        </form>
    </div>
  </template>
  
  <script>

import LoadingButton from "../../../components/LoadingButton";

export default {
  name: "category",
  components: {
   
    LoadingButton,
  },
 
  
};
</script>