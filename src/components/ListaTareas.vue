<template>
    <table class="table">
        <thead>
            <tr>
                <th scope="col">Id</th>
                <th scope="col">Nombre</th>
                <th scope="col">Categoria</th>
                <th scope="col">Estado</th>
                <th scope="col">Número</th>
                <th scope="col">Acciones</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="(tarea, index) in tareas" :key="index">
                <th scope="row">{{tarea.id}}</th>
                <td>{{tarea.nombre}}</td>
                <td>{{tarea.categoria}}</td>
                <td>{{tarea.estado}}</td>
                <td>{{tarea.numero}}</td>
            </tr>
        </tbody>
    </table>
</template>

<script>
import {mapState} from 'vuex';

export default {
    computed: {
        ...mapState(['tareas'])
    }
}
</script>