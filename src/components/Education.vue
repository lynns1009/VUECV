<script lang="ts">
import Vue from 'vue';
import { Component } from 'vue-property-decorator';
import { education } from '../assets/cv';

@Component({ name: 'education' })
export default class extends Vue {
    public education = education;
}
</script>

<template>
    <v-flex xs12 md8>
        <div class="title font-weight-regular md-4">Education</div>
        <br>
        <v-card v-for="e in education" :key="e.institution" class="md-8">
            <v-container fluid grid-list-lg>
                <v-layout row>
                    <v-flex xs12>
                        <div class="subheading" v-html="e.institution"></div>
                        <div class="body-2 font-weight-regular" v-html="e.degree"></div>
                        <div class="body-2 font-weight-regular">{{e.years}}</div>
                        
                    </v-flex>
                </v-layout>
            </v-container>
        </v-card>
    </v-flex>
</template>

<style lang="less" scoped>
.expand {
    position: absolute;
    bottom: 0;
    right: 0;
}
</style>

