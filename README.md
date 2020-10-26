const express = require('express');
const app = express();
const port = process.env.PORT || 8000 ;

app.get("" , (req,res) => {
    res.send("This is my home page");
})

app.get("/about" , (req,res) => {
    res.send("You can copy and paste this code by time by time and i have commnted this in the last");
})

app.get("*" , (req,res) => {
    res.send("Opps! Page Not Found")
})

app.listen(port , () => {
    console.log(`listening to the port at ${port}`)
})

// app.get("" , (req,res) => {
//    res.send('index');
// })
