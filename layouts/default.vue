<template>
  <v-app>
    <v-container>
      <v-layout column>
        <v-flex>
          <v-card flat>
            <v-card-content>
                <v-card-text>
                  <h1>Matheus Constantino Valino</h1>
                  <h2>Projetos</h2>
                  <ol>
                    <li>
                      <nuxt-link to="/">Home</nuxt-link>
                    </li>
                    <li>
                      <nuxt-link to="/tarefas">Tarefas</nuxt-link>
                    </li>
                  </ol>
                </v-card-text>
            </v-card-content>
          </v-card>
        </v-flex>
        <v-flex>
          <nuxt>
            
          </nuxt>
        </v-flex>
      </v-layout>
    </v-container>    
  </v-app>
</template>