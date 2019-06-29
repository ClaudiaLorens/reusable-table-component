<template>
    <div>
        <table>
            <tr>
                <th class="truncate" v-for="(headerTable, i) in tableHeaders" :key="`headerTable-${i}`">{{headerTable}}</th>
            </tr>
            <tr v-for="(expense, i) in tableList" :key="`expense-${i}`">
                    <td class="truncate tooltip" v-for="(property, index) in properties" :key="`property-${index}`">
                        {{expense[property]}}
                        <span>{{expense[property]}}</span>
                    </td>

                    <td><slot></slot></td>
            </tr>
        </table>
    </div>
</template>

<script>
export default {
    components: {},
    props: {
        tableList: Array,
        tableHeaders: Array,
        properties: Array
    },
    computed: {},
    data() {
       return {
       };
    },
    watch: {},
    mounted() {

    },
    methods: {
    }
};
</script>

<style>
    table {
        width: 100%;
        border-spacing: 1rem;
        border-collapse: collapse;
    }

    td, th {
        border-bottom: 1px solid #182E49;
        padding: 1rem;
    }

    th {
        text-align: left;
    }

    tr:first-of-type  {
        background-color: #24A68C;
    }

    .truncate {
        max-width: 2rem;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
    }

    tr:not(:first-child):hover {
        background-color: rgb(230, 233, 232);
    }

    /* Tooltip */
    .tooltip span {
        display: none;
        color: rgb(225, 222, 222);
        text-decoration: none;
        padding: 1rem;
        word-break: break-all;
        max-width: 10rem;
        white-space: normal;
    }

    .tooltip:hover span {
        display: block;
        position: absolute;
        background-color: rgb(43, 42, 42);
        border: 1px solid rgb(43, 42, 42);
        margin: 2px 10px;
    }

    /* Tooltip triangle */
    .tooltip span:before{
        content:'';
        display:block;
        width:0;
        height:0;
        position:absolute;
        border-left: 8px solid transparent;
        border-right: 8px solid transparent;
        border-bottom: 16px solid rgb(43, 42, 42);
        top:-11px;
    }


</style>
