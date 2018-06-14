<template>
    <v-container>
        <v-layout>
            <v-flex>
                <v-card>
                    <v-card-text>
                        <v-form 
                            @submit.prevent="add"
                        >
                            <v-text-field 
                                label="Nome da tarefa"
                                v-model="name"
                            >
                            </v-text-field>
                        </v-form>
                        <v-list>
                            <v-list-tile
                            v-for="(item,index) in items"
                            :key="item"
                            >
                                <v-list-tile-content>
                                    <v-list-tile-title
                                        v-text="item" 
                                    >
                                    </v-list-tile-title>
                                </v-list-tile-content>
                                <v-list-tile-action>
                                    <v-btn
                                        @click="remove(index)" 
                                        icon=""
                                    >
                                        <v-icon color="red">
                                            delete
                                        </v-icon>
                                    </v-btn>
                                </v-list-tile-action>
                            </v-list-tile>
                        </v-list>
                        
                    </v-card-text>
                </v-card>
            </v-flex>
        </v-layout>

        <v-btn
            fixed
            bottom
            right
            fab
            @click="add"
            color="red"
        >
            <v-icon color="white">add</v-icon>
        </v-btn>

    </v-container>
</template>

<script>
export default {
    data() {
        return {
            name:'',
            items:[]
        }
    },
    methods: {
        add() {
            if (this.name !== '') {
                this.items.push(this.name)
                this.name=''
            }
        },
        remove(index) {
            this.items.splice(index, 1)
        }
    }
}
</script>