<template>
    <div id="list">
        <div>Lista:</div>

        <ul id="example-1">
            <li v-for="item in items" :key="item.message">
                {{ item }}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "List",
    data() {
        return {
            items: [
                '...'
            ]
        }
    },
    created() {
        this.fetchApiData()
    },
    methods: {
        fetchApiData() {
            fetch("http://127.0.0.1:5000/list", {
                "method": "GET"
            })
                .then(response => {
                    if (response.ok) {
                        return response.json()
                    } else {
                        alert("Server returned " + response.status + " : " + response.statusText);
                    }
                })
                .then(response => {
                    this.items = response;
                })
                .catch(err => {
                    console.log(err);
                });
        }
    }
}
</script>

<style scoped>
#list {
    margin: auto;
    text-align: left;
    max-width: 1024px;
    padding: 20px;
    background: #4d4c4c;
}

#list ul {
    padding-inline-start: 0;
}

#list li {
    list-style-type: none;
    padding: 5px;
    background: #242021;
    margin: 5px;
}
</style>
