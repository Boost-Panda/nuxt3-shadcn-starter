<template>
    <div class="flex justify-center flex-col items-center min-h-screen bg-background">
        <form @submit.prevent="handleSubmit" class="w-full max-w-md p-6 bg-card rounded shadow-md">
            <h1 class="text-2xl font-semibold text-foreground mb-6 text-center">Upload Food </h1>
            <div class="mb-4">
                <label for="file-upload" class="block text-sm font-medium text-foreground mb-2">Choose Image</label>
                <input type="file" id="file-upload" @change="handleFileChange"
                    class="block w-full text-foreground border border-border rounded px-3 py-2 cursor-pointer focus:outline-none" />
            </div>
            <div v-if="preview" class="mb-4">
                <img :src="preview" alt="Image Preview" class="max-w-full h-auto rounded border border-border" />
            </div>
            <Button type="submit" class="float-right">Submit</Button>
        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            file: null,
            preview: null
        };
    },
    methods: {
        handleFileChange(event) {
            const file = event.target.files[0];
            if (file) {
                this.file = file;
                this.preview = URL.createObjectURL(file);
            }
        },
        handleSubmit() {
            // Handle form submission logic
            alert('Image submitted!');
        }
    }
};
</script>

<style scoped>
/* You can add custom styles here if needed */
</style>