<template>
 <v-container>
        <v-card color="green" >
            <v-card-title>
                <div class="text-h3">Our Menu</div>
            </v-card-title>
        </v-card>
    </v-container>

    <v-container>
        <v-card class="mx-auto" elevation="24" color = "purple">
            </v-card>
        </v-container>
                <v-row ></v-row>
                    <v-col cols="12" md="4"></v-col>
                        <v-card></v-card>
                        <v-container>
        <v-card class="mx-auto" elevation="24">
            <v-container>
            <v-row>
                <v-col cols="12" md="4" v-for="item in menuItems":key=item>
                    <v-card>
                        <v-card color="black">
                            <v-card-item>
                                <v-card-title>{{ item.name }}</v-card-title>

                                <v-card-subtitle>{{ item.description }}</v-card-subtitle>
                            </v-card-item>
                            <v-img height="300px" :src="item.image" cover ></v-img>

                            <v-card-text>{{ item.price }}
                                <v-btn variant="tonal"height="36" min-width="100"@click="addToOrder(item)">Order</v-btn>
                            </v-card-text>
                        </v-card>
                        </v-card></v-col></v-row></v-container></v-card></v-container>

<v-container>
        <v-card color="blue" >
            <v-card-title>
                <div class="text-h6">Current order: {{totalOrderAmount}}</div>
            </v-card-title>
        </v-card>
    </v-container>
    <v-container>
        <v-card class="mx-auto" elevation="24">
            <v-container>
                <v-row>
                    <v-col cols="12" md="4" v-for="item in orderItems" :key=item>
                        <v-card color="yellow">
                            <v-card-item>
                            <v-card-title>{{ item.name }}</v-card-title>
                            <v-card-subtitle>{{ item.description }}</v-card-subtitle>
                            </v-card-item>
                            <v-img height="200px" :src="item.image" cover ></v-img>
                            <v-card-text>{{ item.price }}</v-card-text>
                        </v-card>
                        </v-col>
                </v-row>
            </v-container>
        </v-card>
    </v-container>


</template>

<script setup>
const menuItems = [
    {
        name: "French fries",
        price: 200,
        description: "A crip,flat bowled shaped french fries",
        size: "Large",
        offers: "None",
        image: "/public/french fries.jpg"
    },
    {
        name: "Sausage",
        price: 50,
        description: "Higly seasoned minced meat sausages",
        size: "None",
        offers: "None",
        image: "/public/Sausages.jpg"
    },
    {
        name: "Pizza",
        price: 2000,
        description: "Classic pizza amd burnt cheeze ontop",
        size: "Large",
        offers: "None",
        image: "/public/Pizza.jpg"
    },
    {
        name: "Burgers",
        price: 350,
        description: "Best juicy,flame-grilled patty of ground beef burger",
        size: "Large",
        offers: "None",
        image: "https://img.freepik.com/free-photo/view-delicious-burgers-with-buns-cheese_23-2150887917.jpg?uid=R188095139&ga=GA1.1.833928439.1739952656&semt=ais_hybrid"
    },
    {
        name: "Taccos",
        price: 400,
        description: "A soft flour tortilla filled with seasonal beef",
        size: "Large",
        offers: "None",
        image: "/public/Taccos.jpg"
    },
    {
        name: "Cocktail",
        price: 100,
        description: "A fusion of spirits,flavour and the artisty of human touch",
        size: "Large",
        offers: "None",
        image: "https://www.culinaryhill.com/wp-content/uploads/2018/11/paloma-cocktail-LR-02-Culinary-Hill.jpg"
    }
   
]
//manage the current state of the order
var orderItem = []
var totalOrderAmount = 0

function calculateTotalAmount(price){
    totalOrderAmount += price
}

function addToOrder(item){
    orderItems.push(item)
    calculateTotalAmount(item.price)
}
</script>