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
                            <v-img height="200px" src="https://img.freepik.com/free-vector/healthty-restaurant-menu_1142-847.jpg?t=st=1739955197~exp=1739958797~hmac=a12b925b3dc8f4f1dc83128d7433d736ff957304e30b92490031b7a0321fa481&w=740" cover ></v-img>

                            <v-card-text>{{ item.price }}
                            </v-card-text>
                        </v-card>
                        </v-card></v-col></v-row></v-container></v-card></v-container>
</template>

<script setup>
const menuItems = [
    {
        name: "French fries",
        price: 200,
        description: "A crip,flat bowled shaped french fries",
        size: "Large",
        offers: "None",
        image: "https://unsplash.com/photos/a-basket-of-french-fries-sitting-on-top-of-a-wooden-table-ChXHveqrb28?utm_content=creditShareLink&utm_medium=referral&utm_source=unsplash"
    },
    {
        name: "Sausage",
        price: 50,
        description: "Higly seasoned minced meat sausages",
        size: "None",
        offers: "None",
        image: "https://unsplash.com/photos/sausage-on-black-round-pan-cSxpCQrRlo8"
    },
    {
        name: "Pizza",
        price: 2000,
        description: "Classic pizza amd burnt cheeze ontop",
        size: "Large",
        offers: "None",
        image: "https://www.freepik.com/free-psd/delicious-pepperoni-pizza-slices-ready-eat_412272976.htm#fromView=search&page=1&position=34&uuid=e02efeb2-f34a-4f8a-b01d-c16fdfc887bf&query=pizza"
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
        image: "https://www.istockphoto.com/photo/vegan-tacos-wraps-tex-mex-food-with-beans-avocado-roast-cauliflower-and-vegetables-gm1452503427-488854032?utm_campaign=srp_photos_bottom&utm_content=https%3A%2F%2Funsplash.com%2Fs%2Fphotos%2FTaccos&utm_medium=affiliate&utm_source=unsplash&utm_term=Taccos%3A%3Avideo-affiliates%3Aexperiment"
    },
    {
        name: "Cocktail",
        price: 100,
        description: "A fusion of spirits,flavour and the artisty of human touch",
        size: "Large",
        offers: "None",
        image: "https://images.unsplash.com/photo-1572590016064-3e6ae9c04947?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fENvY2t0YWlsfGVufDB8fDB8fHww"
    }
   
]
</script>