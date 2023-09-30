<template>
    <div class="table">
        <table>
            <thead>
                <tr>
                    <!-- headers -->
                    <th :key="heading.id" v-for="heading in headings">
                        {{ heading }}
                    </th>
                </tr>
            </thead>
            <tbody>
                <!-- rows -->
                <tr v-for="(row, rowIndex) in rows" :key="rowIndex">
                    <td v-for="(cell, cellIndex) in row" :key="cellIndex">
                        {{ cell.content }}
                    </td>
                </tr>
                
            </tbody>
        </table>
    </div>
</template>

<script>
    export default {
        name: "TableComponent",
        props:{rows:Array},
        data(){
            return{
                headings:["Problem", "Justification", "Solution"]
            }
        }
    }
</script>