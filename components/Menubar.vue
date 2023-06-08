
<template>
    <div class="card">
        <Toolbar>
            <template #start>
                <p>Start</p>
            </template>

            <template #end>
                <Button class="flex justify-content-center flex-wrap card-container w-4rem border-round m-2 Login">Login</Button>
                <Button severity="success" class="flex justify-content-center flex-wrap card-container w-4rem border-round m-2 Registrar">Registrar</Button>
                <Button icon="pi pi-times" severity="danger" />
            </template>
        </Toolbar>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const items = ref([
    {
        label: 'Update',
        icon: 'pi pi-refresh'
    },
    {
        label: 'Delete',
        icon: 'pi pi-times'
    },
    {
        label: 'Vue Website',
        icon: 'pi pi-external-link',
        command: () => {
            window.location.href = 'https://vuejs.org/';
        }
    },
    {
        label: 'Upload',
        icon: 'pi pi-upload',
        command: () => {
            this.$router.push('fileupload');
        }
    }
])
</script>

<Style>


</Style>