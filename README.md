# Array-forEach-map-reduce-filter
how can we use method of array those are forEach, map, reduce and filter


// Complete the below questions using this array:
const array = [
  {
    username: "john",
    team: "red",
    score: 5,
    items: ["ball", "book", "pen"]
  },
  {
    username: "becky",
    team: "blue",
    score: 10,
    items: ["tape", "backpack", "pen"]
  },
  {
    username: "susy",
    team: "red",
    score: 55,
    items: ["ball", "eraser", "pen"]
  },
  {
    username: "tyson",
    team: "green",
    score: 1,
    items: ["book", "pen"]
  },
];
//Create an array using forEach that has all the usernames with a "!" to each of the usernames
const userNameEks = [];
const userNameForEach = array.forEach (list  => {
         userNameEks.push(list.username + "!");
          });
  console.log ("forEach" , userNameEks);
//Create an array using map that has all the usernames with a "? to each of the usernames
const mapArray = array.map ( list =>  list.username + "?" );
  console.log("map", mapArray);

//Filter the array to only include users who are on team: red
const filterArray = array.filter (list => list.team === "red");
  console.log("filter" , filterArray);
//Find out the total score of all users using reduce
const reduceArray = array.reduce ((acc , list ) => {
  return acc + list.score;
} , 0 );
  console.log("reduce", reduceArray);
// (1), what is the value of i// i is index that mean is first 0,1,2,3,4,5
// (2), Make this map function pure:
const arrayNum = [1, 2, 4, 5, 8, 9];
const newArray = arrayNum.map((num, i) => num * 2 );
	console.log(newArray);

//BONUS: create a new list with all user information, but add "!" to the end of each items they own.
// const newList = {};
const newList = array.map (list  =>{
  list.items = list.items.map(item => {
     return item + "!"});
  return list ;
} );
  console.log(newList);
