<template>
    <div id="allmenu">
        <div class="container">
            <div class="row">
                <h2 class="headline-2">All Menu</h2>
                <div class="line"></div>
                <div class="d-flex justify-content-around align-items-center flex-wrap mt-5">
                    <div class="col-md-4 mt-5" v-for="card in cards" :key="card.id">
                        <div class="card card-menu">
                            <img :src="card.image" class="card-img-top" alt="Card Image">
                            <div class="card-body">
                                <h5 class="card-title">{{ card.title }}</h5>
                                <p class="card-text">{{ card.description }}</p>
                                <a :href="card.link" class="btn btn-primary">Learn More</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
       </div>
     </div>
   </template>
   
   <style>
   .headline-2 {
     padding-top: 100px;
     font-size: 62px;
     font-weight: 700;
     text-align: center;
   }

   .card-menu {
    width: 400px;
    height: 600px;
   }
 </style>
 

   <script>
       export default {
         data() {
           return {
             cards: [
               {
                 id: 1,
                 title: 'Card 1',
                 description: 'This is card 1 description.',
                 link: '#'
               },
               {
                 id: 2,
                 title: 'Card 2',
                 description: 'This is card 2 description.',
                 link: '#'
               },
               {
                 id: 3,
                 title: 'Card 3',
                 description: 'This is card 3 description.',
                 link: '#'
               },
               {
                 id: 4,
                 title: 'Card 4',
                 description: 'This is card 3 description.',
                 link: '#'
               },
               {
                 id: 5,
                 title: 'Card 3',
                 description: 'This is card 3 description.',
                 link: '#'
               },
               {
                 id: 6,
                 title: 'Card 3',
                 description: 'This is card 3 description.',
                 link: '#'
               }
             ]
           };
         }
       };
   </script>