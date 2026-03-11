# base26
Mongoose schema practice
const mongoose = require("mongoose");

// Define schema
const fruitSchema = new mongoose.Schema({
    name: String,
    score: Number,
    review: String
});

// Create model
const Fruit = mongoose.model("Fruit", fruitSchema);

// Create and loop instances immediately
[
  new Fruit({ name: "Apple", score: 3, review: "Crisp and delicious." }),
  new Fruit({ name: "Banana", score: 5, review: "Sweet and creamy." })
].forEach(fruit => console.log(fruit.name));
