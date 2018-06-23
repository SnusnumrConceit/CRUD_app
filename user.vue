<template>
    <td v-show="!this.isEditing">
        {{ user.lastName}}
    </td>
    <td v-show="this.isEditing">
        <input type="text" 
                :value="this.user.lastName"
                v-model="this.user.lastName">
    </td>
    <td v-show="!this.isEditing">
        {{ user.firstName}}
    </td>
    <td v-show="this.isEditing">
        <input type="text" 
                :value="this.user.firstName"
                v-model="this.user.firstName">
    </td>
    <td v-show="!this.isEditing">
        {{ user.middleName}}
    </td>
    <td v-show="this.isEditing">
        <input type="text" 
                :value="this.user.middleName"
                v-model="this.user.middleName">
    </td>
    <td v-show="!this.isEditing">
        <button class="btn btn-outline-warning"
                type="button"
                @click="edit(index)">
            Изменить
        </button>
        <button class="btn btn-outline-danger" 
                type="button"
                @click="delete(index)">
            Удалить
        </button>
    </td>
</template>